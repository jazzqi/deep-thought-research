# econ-calendar S4 验证交接卡（明日执行）

> 目的：确认周日 cron 自动触发（历史 7 次 `manual__miss` 的最终验证点）与 recap 闭环。
> 生成：2026-08-08 02:40（北京时间），由 Sisyphus 在质量升级计划收尾时固化。

## 背景（一句话）

经济日历报告已完成质量升级（S0-S3 验收通过），S4a/S4b 是跨周时间依赖验证：
cron 在周日触发 forecast/recap 并自动发布，需在触发后人工确认链路生效。

## 时间线与执行

| 步骤 | 时间（北京时间） | 动作 |
|---|---|---|
| 1 | 08-09 周日 17:00 之后 | **S4a 实际触发观察**：确认 cron 自动触发 |
| 2 | 08-16 周日 16:00 之后 | **S4b recap 闭环**：预测验证 + 成绩单首笔 |

## 执行命令（一键验证）

```bash
cd ~/workspace/deep-thought && .venv/bin/python scripts/verify_econ_calendar_s4.py
```

- `--cron` 参数：只查触发链路（C0/C1），适合快速巡检
- 脚本会自动检查：调度器运行、flow 定义、event_bus 触发记录、forecast 落盘、13 节结构、无 session 泄漏、sources 非空、recap 预测验证节、成绩单

## 预期结果

- **S4a（08-09 17:00 后）**：C1 出现 `trigger_source='event_bus'` 的新 run；C2 检查
  `08-10__08-16/forecast.md`（cron 重新生成并覆盖手动版）；C3 结构 13 节。
  若 C1 显示 run 正在 running：flow 需 ~25 分钟完成，稍后重跑（脚本已有提示）。
- **S4b（08-16 16:00 后）**：C4a 预测验证节逐条判定（对照 08-10__08-16 forecast）；
  C4b 成绩单首笔数据 + 累计命中率。

## 如果失败（排查路径）

1. **C0a 调度器未运行** → dt-api 未启动：`tmux send-keys -t dt-api C-c` 后重启
   `cd ~/workspace/deep-thought && source .venv/bin/activate && make run-api`
2. **C1 无 event_bus run** → 查 dt-api 日志 `cron_firing`/`cron_flow_triggered`；
   确认 flow 定义 cron 正确（`/api/flow/definitions/economic_calendar_forecast`）
3. **C2 文件未落盘** → 可能是 flow 仍在执行（等 25 分钟）或 publish 失败
   （查 flow_runs 状态 + `git -C ~/workspace/deep-thought-research status`）

## 已就绪的前置条件（Sisyphus 2026-08-08 已全部验证）

- [x] 运行中 dt-api 的 `cron_registered` 确认：forecast=`0 9 * * 0`、recap=`0 8 * * 0`
- [x] 秒级匹配验证：08-09 全天仅 09:00 触发一次
- [x] recap 提前至 08:00 UTC（竞态修复：forecast roundtable 读新鲜 recap）
- [x] query_calendar_events 工具已装配（agent 自主取数，S3 验证）
- [x] relay 900s 预算（S3 实测 665s 可完成）
- [x] 三个仓库已推送 origin，publish 的 git push 无冲突
- [x] 42+ 项单元测试全绿（529 passed，2 存量失败已证实非本轮引入）
- [x] 08:00 时段仅 recap 一个 LLM 任务（morning_brief 系列已禁用，无资源竞争）

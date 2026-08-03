# themes — 主题索引与 Lead 映射

> 本目录是 Deep Thought 主题文档工厂（D71）的内容真源。
> 每个主题 = `{slug}/README.md`（启动文档）+ `index.md`（定版）+ `_history/`（工作现场）。
> 本文件维护 **主题 ↔ Lead Agent ↔ 参与团队** 的映射关系（D71 Batch 4 #17 Lead 挑选机制）。

## 组织架构（部门负责人 = 各主题 Lead 候选）

| 部门 (org_path) | Head of Dept | 职级 | 成员 |
|---|---|---|---|
| research/macro | soros | Principal | zhou_jintao, dalio, nick_timiraos |
| research/fundamental | buffett | Principal | lynch |
| research/sentimental | kahneman | Principal | shiller |
| research/sector | tech_generalist | Principal | ai_specialist, software_analyst, silicon_analyst, tech_scout |
| research/foresight | kevin_kelly | Principal | karpathy |
| research/crypto | crypto_trader | Principal | — |
| research/geopolitics | geopolitics_agent | Principal | — |
| risk_management | taleb | Principal | —（风控审查，不 Lead 主题） |
| executive | ackman | Managing Director | —（跨资产综合） |

## 主题 ↔ Lead 映射表

| 主题 | Lead | 参与团队 | 主题类型 |
|---|---|---|---|
| nvda | tech_generalist | sector + fundamental + market-daily | 个股/行业 |
| semiconductor | tech_generalist | sector + macro + risk | 行业 |
| optical-modules | tech_generalist | sector + macro | 行业 |
| alphabet | tech_generalist | sector + fundamental | 个股/行业 |
| tesla | tech_generalist | sector + foresight | 个股/行业 |
| spacex | tech_generalist | sector + foresight | 个股/行业（硬科技） |
| disruptive-innovation | kevin_kelly | foresight + sector | 前瞻/扫描 |
| ten-bagger-hunting | kevin_kelly | foresight + fundamental + sector | 前瞻/策略扫描 |
| fed | soros | macro + market-daily | 宏观政策 |
| global-macro | soros | macro | 宏观 |
| energy | soros | macro + geopolitics + market-daily | 宏观/商品 |
| pdd | buffett | fundamental + macro | 个股 |
| china-internet | buffett | fundamental + macro | 行业 |
| pig-cycle | buffett | fundamental + macro | 周期 |
| btc | crypto_trader | crypto + macro + sector | 加密资产 |
| cryptocurrency | crypto_trader | crypto + sector + macro | 加密行业 |
| market-daily | ackman | executive + sentimental + sector + macro | 综合/每日 |
| qqq | ackman | executive + sector + sentimental | 指数 |
| market-sentiment | kahneman | sentimental + crypto | 情绪面 |
| geo-conflicts | geopolitics_agent | geopolitics_agent + risk(taleb 审查) + macro + sentimental + crypto | 地缘/黑天鹅/避险 |

## Lead 挑选规则（D71 Batch 4 #17）

1. **显式声明优先**：`{slug}/README.md` frontmatter 的 `lead_agent` 字段（人类维护，文档为真源）
2. **职级校验**：lead_agent 必须是 agents 表中存在的 agent，且 `job_position = Head of Dept`（或 Principal）——校验失败告警并 fallback
3. **无命中处理**：README 标题加 `⚠️`（如 `# ⚠️ 未分配`），flow 触发时跳过执行 + 日志告警，不静默 fallback
4. **跨部门协作**：lead 单一（主责部门），participants 可跨部门（见上表"参与团队"列）

## 无命中（unassigned）主题

| 主题 | 原因 | 处理 |
|---|---|---|
| （当前无） | — | — |

> 若某主题无法匹配 Lead，在此登记并同步在 README 标题加 ⚠️。

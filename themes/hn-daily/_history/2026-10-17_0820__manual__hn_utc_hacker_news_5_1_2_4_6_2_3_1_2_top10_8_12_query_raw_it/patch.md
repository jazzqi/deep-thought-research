# 增量补丁 · 2026-10-17 0820 会话（距上次定版 0 天）

## 窗口核查

- 基线：themes/hn-daily/2026-10-17.md（revision 2026-10-17T07:13+08:00，覆盖 10-16 UTC 窗口，数据快照 2026-10-16T23:13 UTC）。
- 新增窗口（2026-10-17T00:00→00:30 UTC）查询：query_raw_items(source=hackernews, published_after=2026-10-17T00:00:00Z, published_before=2026-10-17T00:30:00Z) = NO_DATA。窗口仅 20 分钟且入库有延迟，**判定：无【新增】事件，基线稿整体维持**。
- 候选池复核：query_raw_items(10-16 窗口, min_points=20, limit=60) 返回 60 条，与基线稿条目一致；日期过滤器仍部分失效（混入 6-9 月旧条目），但窗口内数据完整，基线稿已用交叉核验规避，此 blocker 不影响本期结论。

## 补丁项（【基线】窗口内的热度更新与事实更正）

### P1. Tesla Roadster 热度与事实更正
- 热度更新：HN 实时页 fetch_url(item?id=50112657) = 1133 points / 2046 comments（2026-10-17 00:22 UTC 核验；入库元数据 ▲1054/💬1909，基线稿快照 ▲1020/1841）。
- **事实更正（高赞评论）**：基线稿第 1 条"分冷气推进器版与燃烧火箭版"表述有误。评论区作者 Reason077 纠正：**两个版本均使用冷气推进器，没有燃烧火箭发动机**；"thrust 版"与"rocket 版"的区别仅在推进器数量。该更正位于评论区顶部、获大量认同，应采纳。原评论作者 synapsomorphy 关于 COPV 高压储气罐碰撞风险的质疑不受影响，保留。

### P2. FT《Anthropic assigned highest junk credit rating in June》热度跳升
- query_raw_items[ id:488243] 入库 ▲39；基线稿核验 176 分/48 评论（10-16 22:45 UTC）；本次 fetch_url(item?id=50122112) = **202 points / 60 comments**（2026-10-17 00:23 UTC）。
- 6 小时内 39→202 分，是基线共识 5（AI 基建资本成本筛选压下沉到个股信用）的加速确认信号。评论区新增论点：KBRA 未获自由现金流/EBITDA、以风险评分替代完整模型、选择小评级机构本身即红旗（作者 grumpymouse / Someone / 2PqboPPmKegvanx）。

### P3. 评审遗留 2 项 blocker 状态
- Blocker 1（HN 日期过滤器部分失效）：本次复现依旧，但候选池数据经实时页交叉核验完整，判定为"已缓解、未修复"。
- Blocker 2（longbridge token 过期 401003，TSLA 行情/一致预期缺失）：本次重试 market_quote(TSLA.US) 仍 401003 token expired，**未修复**，需运维续期。

## 结论
基线稿维持定版；上述 P1 事实更正 + 热度数字更新于 publish 步骤一并应用。

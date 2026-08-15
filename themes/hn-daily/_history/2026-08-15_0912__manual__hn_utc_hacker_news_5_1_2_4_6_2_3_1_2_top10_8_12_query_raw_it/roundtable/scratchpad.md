# Roundtable Scratchpad — hn-daily

- Session: 2026-08-15_0912__manual__hn_utc_hacker_news_5_1_2_4_6_2_3_1_2_top10_8_12_query_raw_it
- Lead: tech_generalist
- 议题: HN 书摘每日扫描：昨日（前一日 UTC 窗口）Hacker News 高价值帖子书摘。 产出 5 栏目：头条深读（1-2 条）/ 值得一读（4-6 条）/ 技术雷达（2-3 条）/ 社区之声（1-2 条）/ 数据速览（Top10 快照），共 8-12 条。
【数据 · 全部工具查询，不注入数值】用工具主动取数（禁止凭空写数字）： - 主取数：query_raw_items 工具，source='hackernews'，按前一日 UTC 窗口
  （created/ingested 前一日 00:00 → 当日 00:00）筛选。
  机械过滤：metadata 的 hn_points ≥ 60（采集端已带分）；同 URL 去重；
  跨天去重（用 ReadThemeDocsTool 读 themes/hn-daily/index.md 的「往期」列表比对标题）。
- 每条入选帖的正文/摘要：query_raw_items 返回的 full_text 优先；
  缺失则用 web 搜索/直接抓取原文补充（抓不到就标注"未能抓取"，不虚构）。
- 评论摘录：用 Algolia HN items API 或评论区抓取（可选，有则摘 1 条高质量评论）。
【规范 · 必读】用 ReadThemeDocsTool 读取两份规范后动笔： 1. themes/hn-daily/template.md —— 5 栏目结构 seed（## 头条深读 / ## 值得一读 /
   ## 技术雷达 / ## 社区之声 / ## 数据速览；禁止编号顶层节——透传 publish 精确匹配）
2. themes/WRITING_GUIDE.md —— 写作硬规则（集体署名/金字塔原理/数字溯源）
【方法 · 四维精筛】每条候选独立打分（1-5）：信息密度（新事实/数据/决策 vs 观点水贴）、 一手性（作者亲历 vs 二手转述）、讨论深度（评论区是否已产生高质量延伸）、 行业相关性（对科技从业者的 relevance）。≥4 入选；3 分按名额递补；<3 淘汰。 辅助信号：hn_points/hn_comments 比（高分低评论 ≈ 标题党嫌疑）。
【质量铁律】① 摘要必须基于实际抓到的正文，抓不到标注"未能抓取"——宁可失败得明显， 不成功得虚假；② 每条带原文链接可追溯（原文 + 评论）；③ 中文为主，标题保留英文原文； ④ 书摘批注 1 句（为什么值得放进今天这本书）+ 评论摘录 1 条（社区怎么接话茬的）。 禁止 session 目录名/manual/miss 等内部元数据出现在正文。
【立场】服务科技行业从业者的每日信息扫描，不输出投资建议。

- 参与 Agent: tech_generalist, tech_scout, ai_specialist, kevin_kelly
- 轮次: 2 / 2
- 状态: ok

## Lead 最终综合

{"action":"blocker","questions":["当前 Hacker News 原始数据无法满足合规成稿：结果混入 2026-08-12/13 条目，且同一帖子展示的 hn_points 与摘要内 Points 不一致；同时未读取 themes/hn-daily/index.md 完成跨天去重，也没有任何候选的完整正文与评论正文可核验。因此若继续生成 5 栏目日报，只能虚构摘要或把不可靠分数当作 Top10，违反“摘要必须基于实际抓到正文”和“机械过滤”的质量铁律。"],"confirmed_missing_indicators":[]}

## 第 1 轮（ask）

- 问题: 请各参与 Agent 独立复核 2026-08-14 00:00–24:00 UTC、hn_points≥60 的 Hacker News 候选：去除 2026-08-12/13 及跨期标题后，分别给出建议入选的头条深读、值得一读、技术雷达、社区之声条目，并为每条确认正文是否实际抓取、四维评分（信息密度/一手性/讨论深度/行业相关性）及原文与评论链接。当前 raw_items 返回结果混入了 8 月 12–13 日条目，且部分 full_text 仅为截断片段，不能直接满足摘要不得虚构的要求。；请重点核实 GLM-5.3、Qwen 3.8 27B、Opus 5、Every Fucking Website、Firefox/uBlock Origin、Google 同态加密、RustDesk Wayland 等 8 月 14 日候选的真实正文与高质量评论；若正文或评论抓取不到，明确标注缺失，不要用标题推断。

## 第 2 轮（blocker）

- 问题: 当前 Hacker News 原始数据无法满足合规成稿：结果混入 2026-08-12/13 条目，且同一帖子展示的 hn_points 与摘要内 Points 不一致；同时未读取 themes/hn-daily/index.md 完成跨天去重，也没有任何候选的完整正文与评论正文可核验。因此若继续生成 5 栏目日报，只能虚构摘要或把不可靠分数当作 Top10，违反“摘要必须基于实际抓到正文”和“机械过滤”的质量铁律。

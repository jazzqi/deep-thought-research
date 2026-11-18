# 数据来源溯源（HN 书摘 2026-11-19 期，窗口 2026-11-18 UTC）

- 主查询 query_raw_items(source='hackernews', published_after='2026-11-18T00:00:00Z', published_before='2026-11-19T00:00:00Z', min_points=20) = NO_DATA（库内 published 过滤无返回）
- 回退① min_points=1 同窗口 = NO_DATA
- 回退② keyword='Show HN', window 2026-11-16→2026-11-19 = 30 条，其中落入 11-18 窗口 6 条
- 窗口内条目: query_raw_items(keyword='Show HN', window 11-16→11-19)[id:792338] = Bank CEOs, NSA Tell Congress AI-Driven Patches Are Behind Outages ▲92 💬48（2026-11-18 01:45）
- 窗口内条目: query_raw_items(keyword='Show HN', window 11-16→11-19)[id:795030] = Show HN: Type Fighter 2 ▲121 💬53（2026-11-18 11:11）
- 窗口内条目: query_raw_items(keyword='Show HN', window 11-16→11-19)[id:795607] = Show HN: Take Voyager 1 apart ▲41 💬7（2026-11-18 16:18）
- 窗口内条目: query_raw_items(keyword='Show HN', window 11-16→11-19)[id:795649] = Show HN: ExitPath ▲41 💬4（2026-11-18 16:04）
- 窗口内条目: query_raw_items(keyword='Show HN', window 11-16→11-19)[id:795937] = Show HN: Mastra Factory ▲33 💬12（2026-11-18 16:53）
- 窗口内条目: query_raw_items(keyword='Show HN', window 11-16→11-19)[id:795913] = Launch HN: Maritime (YC F26) ▲26 💬21（2026-11-18 17:26）
- Voyager 帖实时热度与正文: fetch_url(https://hn.algolia.com/api/v1/search_by_date?tags=story&query=Voyager%201%20apart) = objectID 50548161, points 119, num_comments 25, front_page, story_text 含"Voyager 1 reached one light-day from Earth today"
- Voyager 站点正文: fetch_url(https://rshekhar.com/voyager/) = 交互式拆解站，可逐层打开核电池/数据计算机/单颗内存芯片/金唱片
- 银行/NSA 听证会帖评论: fetch_url(https://hn.algolia.com/api/v1/items/50540836) = 作者 Antoniocl 评论"AI 提升速度后单项目 bug 更少但项目数大增，年度 bug 总量反而上升"
- ExitPath 正文: fetch_url(https://exitpath-ruddy.vercel.app/) = 仅返回标题 "ExitPath — find your way out of big-platform lock-in"（正文未抓全）
- 华盛顿太阳报原文: fetch_url(https://www.washingtonsun.com/...) = HTTP 403 抓取失败，正文未能抓取
- 窗口全量（live 热度）: fetch_url(hn.algolia search_by_date, created_at_i 1794960000–1795046400, points>=20) = 见下方报告数据速览


## 追加溯源（本轮后续抓取）
- Gemini 4 Neon 正文: fetch_url(https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/) = AA 指数 61 总榜#3、Vals #2 (70.9%)、Agent Arena #2 (1336)、定价 $3/$15 每百万 token、1M 上下文
- Gemini 4 Neon 评论: fetch_url(https://hn.algolia.com/api/v1/items/50552424) = 作者 bloky "roulette on which Gemini model"；作者 tanx16 "4th release this month"；作者 WarmWash 列命名阵容
- Genie 4 正文: fetch_url(https://blog.google/innovation-and-ai/models-and-research/google-deepmind/genie-4-now-available-project-genie/) = Ultra 订阅开放 Genie 4、实时语言改环境、原生音频、社区画廊
- Genie 4 评论: fetch_url(https://hn.algolia.com/api/v1/items/50550415) = 作者 thisisauserid "pay to use a beta"；作者 bsboxe "Ultra only, high bar"
- OpenAI 芯片设计原文: fetch_url(https://openai.com/index/advancing-chip-design-with-our-models/) = HTTP 403 正文未抓取
- OpenAI 芯片设计评论: fetch_url(https://hn.algolia.com/api/v1/items/50549493) = 作者 ActionHank 疑为 Anthropic IPO 前造势；作者 bpartcl "'Mean normalized reward' with no equation"
- Scottish HTTP Codes 正文: fetch_url(https://underwood.network/http/scots.html) = 苏格兰方言状态码全表
- 窗口全量回补榜: fetch_url(hn.algolia search_by_date, created_at_i 1794960000-1795046400, points>=25, hitsPerPage=50) = Scottish 219/48, Gemini 4 Neon 189/161, Genie 4 146/125, OpenAI chip 118/59, DaisyRose 84/18, Partial Evaluation 72/12, Gemini Tasks 40/37, Free Software 38/34, Lakegres 36/6, Search Browser 34/23, SRE-1 27/1


## 追加溯源（第 2 棒 ai_specialist，2026-11-18 22:55 UTC 核验）
- revscope 正文第三次直连: fetch_url(https://revscope.co/blog/search-seo-geo-2026/) = HTTP 429 拒绝
- revscope 正文（archive 镜像成功）: fetch_url(https://web.archive.org/web/2026/https://revscope.co/blog/search-seo-geo-2026/) = 随机分组实验站外点击 -39.8%（0.37 vs 0.62 次/搜索）、零外链搜索 54%→73%、广告点击不变；Overview 覆盖率 5.93%(2024-09)→61.43%(2026-08)；特色摘要 8.96%→0.44%；AI 助手 2026-03 仅导流 0.3%；GEO 无补偿证据；文章发布 2026-11-09
- EBR 论文页复核: fetch_url(https://energy-based-reasoners.github.io/) = 摘要与正文两处均为 345×（HN 标题 385× 在论文页无法复现）；1.8M 参数单样本 99.4%/5 样本 99.9% Sudoku、Maze-Hard 87.4/88.3；自适应停止省 10.9× FLOPs；达 EqR 最佳精度需 1/7 迭代、1/43 样本
- Claude 蛋白质条目: query_raw_items(source=hackernews, window 2026-11-18→11-19, min_points=20, limit=60)[id:792999] = Claude was trained on protein sequences at scale ▲156 💬67（Comments 50541619）
- Claude 蛋白质正文: fetch_url(http://xinmingtu.cn/blog/2026/claude-opus-5-5-protein-sequences/) = 668 蛋白/167 DUF 家族；Fable 5.2 真实 54% vs 打乱 9%（+45.1pp）、Opus 5.5 +27.4pp；22 模型仅最新 Claude 有信号；56 个 2026-08 截止后新增蛋白仍被预测；Fable 5.2 胜全部受测公开蛋白 LM、Opus 5.5 与 ProtGPT3-10B 持平
- Gemini 4 Neon 博客复核: fetch_url(https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/) = 与初稿一致；补 Vals #2 (70.9%)、Agent Arena #2 (1336)、FrontierCode 2.0 46.2%、定价 $3/$15、缓存 $0.15、SWE-sweep 12.8%→39.0%
- Cerebras 博客复核: fetch_url(https://www.cerebras.ai/blog/cerebras-launches-disaggregated-inference) = 博客日期 2026-11-17；5× tokens/MW（厂商自述）；GS 2026-05-20 报告 24× vs 2.2×（容量估计经 Investing.com 2026-11-06 转引）；350× SRAM 容量/5,400× 带宽 vs GB300；CS-4 + 700MW，2027 放量
- 使用者打分（ai_specialist 第 2 棒已执行）: id:793225 P1/0.75、id:791889 P1/0.75（领域外记录，路由 karpathy/kevin_kelly）、id:794961 P2/0.75、id:791890 P3/0.60、id:792686 P4/0.50、id:794264 P2/0.70、id:793794 P3/0.60、id:792685 P3/0.65、id:794578 P2/0.75、id:796210 P2/0.65、id:792116 P3/0.65、id:792999 P2/0.70


## 追加溯源（第 3 棒 tech_generalist，2026-01-18 23:08 UTC 终审）
- Quad9 HN 评论页直抓: fetch_url(https://news.ycombinator.com/item?id=50545958) = live 页面 545 分/199 评论；作者 immibis2 评论「This piracy thing isn't new… Quad9 are just the latest victims. And Codeberg.」把两条基础设施头条串成同一事件链（快照热度仍以代码注入为准）
- GOOGL 实时行情: market_quote(['GOOGL.US']) = last 282.44、prev 280.20、+0.80%、额 76.82 亿美元（2026-11-18）
- Alphabet 估值/持仓/财务: query_longbridge_by_route(news/company, {"symbol":"GOOGL.US"}) = 近一月跌 16.77%；Q3 Druckenmiller 清仓、Dan Loeb 减仓 83%（转投 Meta/Nvidia/Microsoft），主因 AI 支出与负自由现金流；UBS 目标价 320 美元、一致预期目标均价 269.88 美元（买入评级）
- Waymo 监管处罚: query_longbridge_by_route(news/company, {"symbol":"GOOGL.US"}) = 加州 DMV 安全禁令，15 个美国市场全部高速路段停运、地面道路照常（2026-11-18）
- Anthropic IPO 持股: query_raw_items(keyword='Anthropic OR OpenAI OR Google OR IPO', published_after=2026-11-11T00:00:00Z, published_before=2026-11-19T00:00:00Z, min_points=50)[id:795910] = Amazon+Google IPO 后合计持股近 30%（TechCrunch 2026-11-17）
- Anthropic 安全品牌联署: query_raw_items(同窗口, min_points=50)[id:795650] = 科学家/法律学者/科技领袖联署「Anthropic is Not a Safe AI Company」挑战其 IPO 前安全品牌（2026-11-18）
- 国会作证条目: query_raw_items(keyword='Show HN', window 11-16→11-19)[id:792338] = Bank CEOs, NSA Tell Congress AI-Driven Patches Are Behind Outages ▲92 💬48（本轮共识第 5 条引用）
- 宏观指标核验: query_indicators(category=macro, country=us, time_range=7d) = fed_balance_sheet 6.76 万亿（2026-11-11，7 天前可用）；cpi_yoy 3.7%（2026-09-01）与 consumer_confidence 48.1 已超 90 天标记过时，未用于正文
- Gemini 4 发版节奏: roundtable/discussion_log.md（ai_specialist 第 1 轮）= Carbon 2026-11-10、Hydrogen 11-12、Neon 11-18（8 天三版）

- 2026-11-18 HN ≥20分窗口（审查独立复查）: query_raw_items(source=hackernews, published_after=2026-11-18T00:00:00Z, published_before=2026-11-19T00:00:00Z, min_points=20, limit=100) = 73 条（稿称 70 条，存在口径/时点差，建议注明查询时点）
- Show HN/Launch HN 扫描（11-17→11-19）: query_raw_items(keyword='Show HN', published_after=2026-11-17T00:00:00Z, published_before=2026-11-19T00:00:00Z, limit=30) = 17 条；11-18 当日含 Type Fighter 2、Mastra Factory、Maritime(YC F26)、ExitPath、Voyager 等
- 微软 Ignite 七款新模型（当日 #7，稿未收）: query_raw_items(...)[id:795579] = Microsoft AI: Seven new world-class models at scalable price-performance，387▲/268💬
- KVM guest-to-host escape（当日第二大安全事件，稿未收）: query_raw_items(...)[id:795578] = CVE-2026-99312 Terra Security，164▲/113💬；CVE 记录页 [id:795911] = 142▲/84💬
- Deutsche Bank（当日 #4，稿未收无摘要）: query_raw_items(...)[id:795473] = inside-db.com，491▲/179💬
- Anthropic IPO 安全品牌质疑（稿未收）: query_raw_items(...)[id:795650] = "Anthropic Is Not a Safe AI Company" 联盟声明，73▲/35💬；[id:795910] = Amazon+Google IPO 后合计近 30%，28▲/0💬
- 当日最高 Show HN: query_raw_items(...)[id:795030] = Show HN: Type Fighter 2，121▲/53💬
- Show HN: Mastra Factory（TS agent 框架）: query_raw_items(...)[id:795937] = 33▲/12💬
- Launch HN: Maritime (YC F26) agent 云: query_raw_items(...)[id:795913] = 26▲/21💬
- Genie 4 开放可用（稿未收）: query_raw_items(...)[id:795918] = Google DeepMind Genie 4，73▲/20💬
- OpenAI 芯片设计（稿未收）: query_raw_items(...)[id:795915] = Advancing chip design with OpenAI models，63▲/18💬
- Codeberg 分数核验（共识2「合计 500+ 分」存疑）: query_raw_items(...)[id:794264] = 288▲/291💬、[id:793794] = 53▲/20💬、[id:794189] = 30▲/3💬（库内合计 341-371 分）
- GOOGL 近期重大新闻（审查独立核验）: query_longbridge_by_route(news/company, {"symbol":"GOOGL.US","count":15}) = Waymo 全美 15 市场高速停运（加州 DMV）、Q3 对冲基金集体减持（Druckenmiller 清仓/Loeb -83%）、UBS 目标价 320 vs 一致预期 269.88、月内 -16.77%、Neon 单任务 $6.44/21 分钟、Quaise 50MW 地热 PPA（均与稿件 Big Picture 一致，无重大漏收）
- Alphabet 2026Q3 财报 vs 一致预期（审查独立核验）: query_longbridge_by_route(fundamental/consensus, {"symbol":"GOOGL.US"}) = 营收 1275.77亿 vs 1280.18亿 Miss、EBIT 405.76亿 vs 431.95亿 Miss、净利 261.70亿 vs 372.21亿 Miss、EPS 2.12 vs 3.0089 Miss（与稿件一致）

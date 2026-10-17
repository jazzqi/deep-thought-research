# Reference · 2026-10-16 HN 书摘数据来源

- Tesla Roadster 头条条目: query_raw_items(source=hackernews, published_after=2026-10-16T00:00:00Z, min_points=30)[id:485415] = Tesla Roadster ▲1054 💬1909，tesla.com 页面 403 未能抓取正文
- Tesla Roadster HN 评论（lisper "parlor trick" 等）: fetch_url(https://news.ycombinator.com/item?id=50112657) = HN 讨论页：冷气推进器版本区分、飞行数秒、street-legal 争议
- Tesla 0-60<1s 报道: query_raw_items(...)[id:487505] = Fox Business: Tesla's new Roadster makes flying debut, hitting 60 MPH in under a second
- ECDSA 悬案正文: fetch_url(https://www.anthropic.com/research/ecdsa-curve-origins) = Claude 半小时内破解 NIST P-192~P-521 种子来源：lrand48 以 Unix 时间戳播种，非哈希算法；非密码学破击
- ECDSA 条目: query_raw_items(...)[id:488280] = Claude reveals ECDSA curve origins ▲244 💬98
- ECDSA 高赞评论（FiloSottile）: fetch_url(https://news.ycombinator.com/item?id=50122800) = Filippo Valsorda 回应后门论：时间戳遍历仅 ~30 bit 自由度
- MLX Muse Spark Open: fetch_url(https://machinelearning.apple.com/research/mlx-distributed-inference) = 4×Mac Studio (M5 Ultra) RDMA over Thunderbolt 张量并行，816B MoE(激活42B, NVFP4) 8K ctx 解码 >36 tok/s
- MLX 条目: query_raw_items(...)[id:487907] = Apple ML Research MLX on Mac Studio ▲246 💬109
- Waymo Toronto: fetch_url(https://waymo.com/blog/2026/10/waymo-in-toronto/) = 进军加拿大多伦多，2028 目标首运，Element Fleet 合作，4亿公里重伤事故率较人低95%
- Waymo 条目: query_raw_items(...)[id:487909] = Waymo in Toronto ▲231 💬331
- Mercor 基准地图: fetch_url(https://www.mercor.com/research/labor-index/benchmark-map/) = 923 职业/18797 任务中仅 208 职业有≥5条基准prompt，90% 美国工时落在低覆盖任务
- Mercor 条目: query_raw_items(...)[id:488215] = 90% US working hours uncovered by AI benchmarks ▲195 💬166
- Mercor 评论（Doorman Fallacy）: fetch_url(https://news.ycombinator.com/item?id=50121179) = b800h 高赞评论：替换门卫的"自动化谬误"
- RPKI 数据: fetch_url(https://ipinfo.io/blog/rpki-protects-70-internet-routes) = 有效前缀 54.0%→70.3%（+16.4pt），中国 3.7%→83.0% 贡献近六成增量；宽松ROA占16.2%
- RPKI 条目: query_raw_items(...)[id:485360] = RPKI Protects 70% Routes ▲219 💬100
- Claude Code 代码评审: fetch_url(https://claude.dev/blog/solving-code-review-at-anthropic/) = Anthropic monorepo 日变更 5月~2500→9月>30000；6-9月PR翻倍、回滚率降40%+；评审改为机器先行连续流程
- Claude Code 条目: query_raw_items(...)[id:488331] = Claude writes ~90% of Claude Code's code ▲48 💬43
- StarSkirmish v0.2: fetch_url(https://starskirmish.com/bench/v0-2/) = GPT-6 Astra 第一，GPT-6.1 Sol 十分之一成本第二；对最强人类bot仅7%胜率；得分最强预测因子=对强bot练习局数
- StarSkirmish 条目: query_raw_items(...)[id:487928] = Gemini 4 Argon plays StarCraft ▲177 💬82
- Postgres 19 延期: fetch_url(https://news.ycombinator.com/item?id=50119991) = HN 讨论页（theregister 正文被拦截）：AI 审阅发现缺陷多到人工修不完
- Postgres 条目: query_raw_items(...)[id:488112] = Postgres 19 delayed ▲87 💬22
- /dev/null 社交网: fetch_url(https://dev-null.sh) = 实时流：Laravel 团队直播发布、commit 式发帖、automod 审核、上线即需扩容
- /dev/null 条目: query_raw_items(...)[id:488150] = /dev/null social network for developers ▲40 💬57


## 第 2/3 棒（ai_specialist）补充来源
- ECDSA 曲线种子悬案主帖（▲244 快照）: query_raw_items(source=hackernews, keyword='ECDSA OR seeds OR curve', published_after=2026-10-15, min_points=1)[id:488280] = Anthropic 研究：Claude 揭示 NIST ECDSA 曲线种子起源
- NIST 悬赏被认领跟进帖: query_raw_items(source=hackernews, keyword='ECDSA OR seeds OR curve')[id:488348] = Filippo Valsorda 宣布悬赏认领，全文 words.filippo.io/seeds-solved/
- HN 讨论页 fidotron/Filosottile/tptacek/matthewdgreen/cyphar 争议链: fetch_url(https://news.ycombinator.com/item?id=50122800) = 651 points/263 comments（抓取时实时值，快照为 ▲244/98）
- 悬赏认领细节（drand48/srand48、时间戳、P-256 第 1842 次迭代、奖金捐赠 ISRG $36,864、Koblitz-Menezes 2015 §3.1、Bernstein-Lange 70-bit 技术被排除、约半数合法种子未发布原因不明）: fetch_url(https://words.filippo.io/seeds-solved/) = Filippo Valsorda 原文


## 审查（tech_scout 交叉审查）补充来源
- 10-16 窗口 HN 独立复核: query_raw_items(source=hackernews, published_after=2026-10-14, published_before=2026-10-17T02:00Z, limit=50) = 含 [id:487908] Big Fish OpenBSD ▲154、[id:488113] JXL vs AVIF ▲195、[id:487929] Redesigning Source Control at Anthropic ▲31、[id:488279] PS5LM ▲61、[id:488489] Flux 3 Klein ▲29、[id:488111] Show HN rStation ▲50
- StarSkirmish 参赛方核验: query_raw_items(...)[id:487928] = 原文摘要为 "flagship models of OpenAI, Anthropic, Google, and Muse"，正文写 "Meta" 疑为笔误
- RPKI 条目复核: query_raw_items(source=hackernews, keyword='RPKI', published_after=2026-10-15)[id:485360] = RPKI Now Protects 70% of Internet Routes ▲219 💬100

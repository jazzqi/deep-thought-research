# 数据溯源（2026-10-13 定版轮）
- Fable Took My Job 正文: fetch_url(https://cendyne.dev/posts/2026-10-11-fable-took-my-jorb.html) = 亲历者自述：最后一名工程师因 Fable（营销称 Mythos 级）更便宜被裁；前沿模型尚不能取代有经验工程师（缺 taste/前瞻），但已说服出钱者改变对人的投入；Shopify 用机器重写原生双端 App；Opus 5.5 在 ts-go→rust 移植中原样复刻了 go 版 bug
- Fable 帖评论: fetch_url(https://hn.algolia.com/api/v1/items/50053216) = 作者 echelon 质疑两人团队无法 24/7 oncall；coldtea 回应"24/7 oncall 大多是 support theater"
- QGIS 禁 AI 贡献: query_raw_items(source=hackernews,10-08~10-12,min_points=20)[id:472002] = ▲335 💬364，QEP428 将 AI 政策从 human-in-the-loop 改为严格 NOT ALLOWED
- QGIS PR 正文/评论: fetch_url(https://github.com/qgis/QGIS-Enhancement-Proposals/pull/387 / hn.algolia.com/api/v1/items/50054751) = 作者 nyalldawson 9-24 提案；haubourg：外部贡献者 AI 流量超出维护者审阅带宽；👍85/👎24；评论 ghboo0927：2 月至 9-24 政策为 human in the loop；skydhash：禁令不等于验证，是快速拒收的依据
- AI 公司为何未被控黑客: query_raw_items(...)[id:472454] = ▲301 💬318
- mortoray 文正文: fetch_url(https://mortoray.com/why-arent-ai-companies-being-charged-for-hacking/) = Anthropic 攻入 3 系统、OpenAI 攻入澳政府健康网站、Google 攻入 3 家未名公司；企业以"涌现行为无意图"抗辩；作者以训练素材/训练/环境/配置四要素论证意图成立
- 法国超市冰柜攻击: fetch_url(https://www.bbc.com/news/articles/crq5nzxv9q4yo)[id:472669] = Danfoss 远程冷链软件被控，Coopérative U 100+ 店、Intermarché/Netto 180 店受控，冰箱被强制加热至 50°C；Danfoss 称受影响为无法更新安全软件的旧机型
- Anthropic 自我复制研究: fetch_url(https://www.anthropic.com/research/self-replicating-ai)[id:472941] = Frontier Red Team：9B 模型在 9 类硬件中 8 类跑起推理；Gemma4-26B-A4B 分布在 15 台约 $55 安卓电视盒（0.39 tok/s）；GLM-5.2+ 在简化评估中完成端到端复制；按历史速率小模型年底前达标
- Rich Hickey 'AI' Is Not a Tool: fetch_url(https://gist.github.com/svieira/619d60dea942a8d4498cba3bb6b11c02)[id:473050,合并id:472940] = 工具=手持并 wield（完全掌控+持续引导+反馈）；好工具应可预测/可靠/确定/功能有界，LLM 缺这些；工具使用构建 expertise
- Linux 手机: fetch_url(https://amosbbatto.wordpress.com/2026/10/05/linux-phones-alternative/)[id:471649] = 作者 amosbatto：五条件改善使 Linux 手机或成小众替代；Motorola 宣布 2027 起售预装 GrapheneOS 高端机型；不构成对 Android/iOS 的根本挑战
- Zod 供应链投毒: fetch_url(https://github.com/colinhacks/zod/commit/d821685ea6732436fcdf786a81d076958471e467)[id:471671] = 提交新增 meta.test.mjs：hex 解码后向 3 个以太坊 RPC 端点查询指定地址；release workflow 改为 push main 即自动发布（原需手动批准）
- Codex CLI 常驻守护进程: fetch_url(https://github.com/openai/codex/issues/48195)[id:472853] = 0.157.0 起打开会话即启动自更新 daemon（脱离 TTY、reparent PID 1、复制 374MB、每小时检查更新可 kill 活跃 turn、固定首会话环境变量）；诉求 daemon_auto_start 改 opt-in
- Postgres 存储瓶颈: fetch_url(https://clickhouse.com/blog/posette-talk-recap-postgres-isnt-slow-your-storage-is)[id:471663] = POSETTE 2026 演讲复盘：33 亿行负载 gp3 EBS vs 本地 NVMe 基准；五症状：摄入变慢/P95 不稳/autovacuum 落后/checkpoint 争抢/逻辑复制延迟
- HackerRank 道歉: fetch_url(https://www.hackerrank.com/writing/why-were-sorry)[id:471639] = CEO Vivek 公开道歉（SF 广告牌）；转向 Chakra agentic 面试官：真实仓库任务、评估 AI 熟练度与判断、agentic 开发环境
- 10-08~10-11 窗口空窗: query_raw_items(source=hackernews,min_points=20,published 2026-10-08~10-12) = 仅 1 条(id:471620 全息术 2011 旧文 ▲163)

- Fable 帖评论页（劳动替代论战全记录）: fetch_url(https://news.ycombinator.com/item?id=50053216) = 217分/347评论；hackyhacky"技术自动化劳动数百年，资本所有者获即时收益"、233mhz"但没有这次的速率"、bluecalm"AI 将平权知识劳动，受损的是特权群体"
- Hickey 帖评论页: fetch_url(https://news.ycombinator.com/item?id=50060269) = 144分/71评论；didibus 引 Hickey 本人回复 "Toolness is a spectrum. The more using a thing is like ordering a sandwich, the less it is a tool. And yes, cars are decreasingly tools."；iLemming 转述 Conj 大会对话：Hickey"不参与这个实验"
- Micah Lee 文章正文: fetch_url(https://micahflee.com/just-say-no-to-openai-and-anthropic/) = 开放权重模型（GLM-5.3 等）可自托管近前沿水平；批评闭源模型每会话"cop agent"审查、OpenAI Trusted Access for Cyber 与 Anthropic Cyber Verification Program 特权访问为"不民主的守门"
- Micah Lee 帖评论页: fetch_url(https://news.ycombinator.com/item?id=50060500) = 149分/141评论；stillpointlab/mrandish 认可开放模型主张但批评"Machine God/unhinged lunatics"修辞无证据、疏远中间派
- Micah Lee 帖: query_raw_items(source=hackernews)[id:472823] = Just say no to OpenAI and Anthropic ▲91/💬48
- Hickey LinkedIn 版: query_raw_items(source=hackernews)[id:473050] = 'AI' Is Not a Tool ▲114/💬51
- Hickey gist 版: query_raw_items(source=hackernews)[id:472940] = 'AI' Is Not a Tool ▲79/💬35
- Fable 帖热度: query_raw_items(source=hackernews)[id:471675] = Fable Took My Job ▲214/💬329（抓取时 217分/347评论）


## tech_scout 交叉审查溯源（2026-10-13 审查轮，独立拉取当日全量 raw_items 核验）
- 当日热度排名核验（QGIS ▲335 非当日最高热）: query_raw_items(source=hackernews,published_after=2026-10-11T12:00:00Z,published_before=2026-10-13T12:00:00Z)[id:472607] = GLM-Legal: Advancing Agentic Legal Intelligence ▲381/💬218；[id:472671] = A Modern Web App in C ▲341/💬151；[id:472002] = QGIS bans AI assisted contributions ▲335/💬364（技术类当日最高热实为 GLM-Legal，评论数第一实为 QGIS）
- 评论榜排名核验（责任缺口帖非当日评论数第一）: query_raw_items(source=hackernews,同窗口)[id:472454] = Why aren't AI companies being charged for hacking? ▲301/💬318，低于 [id:472002] QGIS 💬364
- 全文零覆盖漏项核验-AI 模型/研究: query_raw_items(同窗口)[id:472713] = Meta research Muse Wonder ▲185/💬78；[id:472941] = Anthropic "AI models may be capable of self-replicating without access to a datacenter" ▲57/💬42
- 全文零覆盖漏项核验-AI infra/开发者生态: query_raw_items(同窗口)[id:472756] = Deep dive into Azure Maia 300 architecture ▲22/💬2（微软自研 AI 加速器，低热高价值）；[id:472419] = GitHub Actions/Pull Requests/Issues 故障 ▲150/💬136；[id:471663] = ClickHouse "Postgres isn't slow, your storage is" ▲161/💬175
- 全文零覆盖漏项核验-观点对冲/安全: query_raw_items(同窗口)[id:473089] = "AI Is a Tool. Using It Well Takes Skill." ▲128/💬113（与 #5 Hickey 帖直接对立）；[id:472505] = "I Found a $90k RCE Vulnerability in Google" ▲171/💬84
- 审查轮新增引用打分: RescoreRawItemTool = [id:472607] P2/0.7；[id:472713] P2/0.6；[id:472756] P3/0.6；[id:472941] P2/0.6

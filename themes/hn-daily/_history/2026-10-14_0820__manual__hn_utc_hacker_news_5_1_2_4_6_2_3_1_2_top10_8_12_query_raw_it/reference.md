# 数据来源溯源（2026-10-14 HN Daily，ai_specialist 第 2 位接力）

- Gemini 4 Argon 发布（deepmind.google/models/gemini/，▲926/💬712）: query_raw_items(source='hackernews', min_points=80, published_after='2026-10-13')[id:476415] = Google DeepMind 发布 Gemini 4 Argon，HN 当日最热
- Gemini 4 Argon 正文（Chrome 6M 行重构/xTB 2.3x/ADK 40% 提速/Gemma 4 E2B 经 vLLM 2.85x 推理加速 37,900→108,000 tok/s/CWE-Bench 68% 并列#1）: fetch_url(deepmind.google/models/gemini/) = 官方产品页正文
- Gemini 4 HN 评论（免费用户 Try 按钮落回 Gemini 3.6、发布混乱；非编码任务"step change"好评）: fetch_url(news.ycombinator.com/item?id=50073879) = HN 评论页抓取
- Character.ai Chapter 11 破产（▲222/💬241）: query_raw_items(source='hackernews', min_points=80, published_after='2026-10-13')[id:475845] = Character.ai 自愿申请第11章破产，法院监督出售
- Character.ai 官方声明（出售预计 2026年11月底-12月初完成，无报价则关停；订阅暂不变）: fetch_url(blog.character.ai/an-update-on-character-ai/) = 官方博客正文
- Character.ai HN 评论（2024-08 Google 27 亿美元交易"反向收购"创始团队后剩空壳）: fetch_url(news.ycombinator.com/item?id=50068036) = HN 评论页抓取
- Anthropic 自研源码管理 Scion（日合并量 2026-05 约2,500次 → 2026-09 超30,000次；monorepo 历史近100GB；日2,500万次 CI checkout）: fetch_url(anthropic.com/engineering/redesigning-source-control) = Anthropic 工程博客正文；HN 条目 query_raw_items[id:476611]
- Rust 借用检查器 11 年 unsoundness（issue #164250，协变字段赋值绕过生命周期，stable 1.85+ 可触发 stack-use-after-scope）: query_raw_items[id:475477] + fetch_url(github.com/rust-lang/rust/issues/164250) = GitHub issue 正文
- Embedding Gemma Transcribe（M3 MacBook Air 1小时音频12.6秒/288x 实时；reader 训练<2小时 8×H100；WER 约5% vs 前沿2-3%）: query_raw_items[id:475692] + fetch_url(eg2.haku.sh/) = 项目页正文
- Apple HomeView（7英寸家用屏+Siri AI，2026-11-13 开售，可识别6人）: query_raw_items[id:475886] + fetch_url(apple.com/apple-homeview/) = 苹果官网产品页
- IMF 全球金融稳定报告：AI 股崩盘列为三大近端风险之一；Mag7 占标普500 超35%（十年前12%）: query_raw_items[id:474309] + fetch_url(theguardian.com/.../ai-share-crash-risk...) = Guardian 报道正文
- Ben Recht 批评 OpenAI "更快 FFT"（big-O 记号滥用产物，非真正突破）: query_raw_items[id:473896] + fetch_url(argmin.net/p/faster-fourier-transforms) = 博客正文
- AI Models Can Provably Hide Arbitrary Capabilities（arXiv 2610.13928，NeurIPS 2026，加密后门使能力评估"可引出假设"在密码学上失效）: query_raw_items[id:473932] + fetch_url(arxiv.org/abs/2610.13928) = 论文摘要页
- Apple Minions 虚拟 GPU 云（聚合闲置 Apple Silicon 跑大规模推理，2026-10 论文）: query_raw_items[id:475918] + fetch_url(machinelearning.apple.com/research/distributed-gpu-cloud) = Apple ML Research 论文页
- AI 爬虫流量（sprinklz.io 作者：HN 走红后近半流量来自单个"网站变更监听+AI摘要简报"爬虫）: query_raw_items[id:476413] + fetch_url(sammystraus.com) = 博客正文；HN 评论 fetch_url(item?id=50073221)
- 软件工程师"蓝领论"（30年蜜月期结束，工程师=技术工种）: query_raw_items[id:475066] + fetch_url(ptrbrynt.com/posts/were-we-blue-collar-workers-all-along) = 博客正文


## 第 3 轮（tech_generalist）数据来源

- Gemini 4 Argon 发布（当日最热）: query_raw_items(source=hackernews, min_points=20, 2026-10-13 UTC 窗口)[id:476415] = ▲926/💬712，deepmind.google/models/gemini/
- Gemini 4 Argon for Robotics 同日发布: query_raw_items(...)[id:476614] = ▲194/💬45，developers.googleblog.com
- Character.ai 申请 Chapter 11（官方）: query_raw_items(...)[id:475845] = ▲222/💬241，blog.character.ai
- The Verge：Character.ai 破产、Disney 参与竞标: query_raw_items(...)[id:475691] = ▲144/💬20
- IMF 警告 AI 股崩盘威胁全球金融稳定: query_raw_items(...)[id:474309] = ▲107/💬124，theguardian.com
- Rust 借用检查器 11 年 unsoundness: query_raw_items(...)[id:475477] = 冻结快照 ▲559/💬323（复核时 ▲671/💬373），rust-lang/rust#164250
- Mozilla Firefox Enterprise: query_raw_items(...)[id:475744] = ▲493/💬203
- Apple HomeView: query_raw_items(...)[id:475886] = ▲585/💬721
- EmbeddingGemma 改造转录 13 秒/小时: query_raw_items(...)[id:475692] = ▲348/💬81，eg2.haku.sh
- Anthropic 自研 Scion 替换 git: query_raw_items(...)[id:476611] = ▲527/💬514（讨论稿引用时 ▲103 为早期读数）
- Apple Minions 虚拟 GPU 云论文: query_raw_items(...)[id:475918] = ▲203/💬89，machinelearning.apple.com
- 论文：模型可密码学隐藏任意能力: query_raw_items(...)[id:473932] = ▲271/💬136，arXiv 2610.13928
- 个人网站遭 AI 爬虫流量淹没: query_raw_items(...)[id:476413] = ▲228/💬143，sammystraus.com
- 软件工程师是否一直是技术蓝领: query_raw_items(...)[id:475066] = ▲89/💬188，ptrbrynt.com
- Anthropic 蒸馏攻击防御（评论密度异常）: query_raw_items(...)[id:473869] = ▲40/💬91
- 荷兰税务机关取消 M365 转投开源（Firefox Enterprise 视角旁证）: query_raw_items(...)[id:477034] = ▲27/💬0，zdnet.com
- 数据速览 Top10 快照: 主题冻结快照（代码注入，未手写）


- 英国人均发电量较 2000 年代初峰值下降 1/3（Our World in Data）: query_raw_items(source=hackernews, min_points=20, 2026-10-13)[id:476431] = ▲186/💬260
- Leaving Tech（工程师离场叙事，情绪面旁证）: query_raw_items(...)[id:473724] = ▲169/💬181
- Ben Recht 批评 OpenAI FFT 算法为记号滥用: query_raw_items(...)[id:473896] = ▲237/💬155，argmin.net
- Firefox Enterprise HN 评论：Island 4 亿美元 F 轮 @64 亿美元估值、Mozilla 员工作者 peterrojas 承认落后先攻欧洲: fetch_url(news.ycombinator.com/item?id=50070302) = 评论区一手信息
- Rust HN 评论：编译器 bug 非类型系统缺陷、现存同类 unsoundness 公开清单: fetch_url(news.ycombinator.com/item?id=50069499) = 评论区一手信息


## 第 4 轮（tech_generalist，接力写作 3/3 定稿）新增来源

- Rust HN 评论（编译器 bug 非类型系统缺陷、同类 unsoundness open issue 公开清单）: fetch_url(news.ycombinator.com/item?id=50069499) = HN 评论页抓取（作者 GrantMoyer / 作者 yencabulator）
- Firefox Enterprise HN 评论（Island 4 亿美元 F 轮 @64 亿美元估值；Mozilla 新产品负责人作者 peterrojas 承认落后、先攻欧洲企业）: fetch_url(news.ycombinator.com/item?id=50070302) = HN 评论页抓取（作者 solatic / 作者 peterrojas / 作者 zhivota）
- 丹麦-德国隧道网络攻击停工（复核 ▲151/💬121，早前读数 ▲67）: query_raw_items(source=hackernews, min_points=80, published_after=2026-10-12)[id:476612] = ua.news 报道
- 假硬件钱包内置隐蔽 eSIM: query_raw_items(source=hackernews, min_points=80, published_after=2026-10-12)[id:475339] = ▲110/💬15，heise.de
- Trezor 钱包同款植入物: query_raw_items(source=hackernews, min_points=80, published_after=2026-10-12)[id:477198] = ▲22/💬1，zetter-zeroday.com
- 中国 2024 年研发支出首超美国（读卖）: query_raw_items(source=hackernews, min_points=80, published_after=2026-10-12)[id:473764] = ▲152/💬148
- Leaving Tech 离场叙事（情绪面旁证）: query_raw_items(source=hackernews, min_points=80, published_after=2026-10-12)[id:473724] = ▲169/💬181
- 行情/公司新闻（market_quote / longbridge news/company）: 查询失败（token expired），本期未纳入实时行情，资本层面仅用 IMF 报告数据


## 审查轮（tech_scout 交叉审查，2026-10-14）独立核验来源

- 2026-10-13 HN 全量独立复核（min_points=40，窗口 2026-10-13~10-14 02:00Z，48 条）: query_raw_items(source='hackernews', min_points=40, published_after='2026-10-13T00:00:00Z') = 用于核对 Top10 快照与漏项检查
- Gemini 4 Argon for Robotics（▲194/💬45）: query_raw_items(published_after='2026-10-13')[id:476614] = developers.googleblog.com，正文未覆盖，仅 reference 出现
- Show HN: SolidCraft 开源参数化 CAD（Rust+MCP，▲127/💬21）: query_raw_items(...)[id:474120] = github.com/bherbruck/solidcraft，正文未覆盖
- How to engineer an AI harness for game development（Claude Code，▲129/💬58）: query_raw_items(...)[id:476610] = kylekukshtel.com，正文未覆盖
- AWS Lambda Web Functions 发布（▲103/💬95）: query_raw_items(...)[id:475528] = aws.amazon.com 博客，正文未覆盖
- OpenAI engineer arrested（会议室窃听，▲114/💬129）: query_raw_items(...)[id:476975] = sfstandard.com；关联条目 [id:476896]（▲69）= OpenAINewsroom，正文未覆盖
- Unsiloed × Typesafe Jev 文档审阅集成（▲42/💬7）: query_raw_items(...)[id:475790] = unsiloed.ai 博客，Jev 生态后续信号，正文未覆盖
- DishwasherBench 机器人操作基准（▲83/💬50）: query_raw_items(...)[id:474988] = github.com/composo-ai/DishwasherBench，正文未覆盖
- Gentoo 反对使用 uv-build（Python 工具链生态，▲49/💬38）: query_raw_items(...)[id:476758] = blogs.gentoo.org，正文未覆盖
- Anthropic 蒸馏攻击防御研究（▲40/💬91 评论密度异常）: query_raw_items(...)[id:473869] = anthropic.com/research/distillation-defenses，正文未覆盖

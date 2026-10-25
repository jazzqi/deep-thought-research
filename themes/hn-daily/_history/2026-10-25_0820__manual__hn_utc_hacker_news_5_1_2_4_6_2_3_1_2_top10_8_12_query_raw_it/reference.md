# 数据来源溯源 · HN 书摘 2026-10-25（UTC 窗口 2026-10-24 00:00 → 2026-10-25 00:00）

## query_raw_items 主查询（source=hackernews, min_points=20, published 窗口 2026-10-24）
- Samsung TV root shell 热度: query_raw_items(source='hackernews',min_points=20,published_after='2026-10-24T00:00:00Z',published_before='2026-10-25T00:00:00Z')[id:533952] = Root shell on Samsung TV，▲483/💬194，作者 testing22321
- Samsung TV 同串 Reddit 条: query_raw_items(同上窗口)[id:533572] = Hacker reverses Samsung TV, finds on-board AI listening OpenAI account suspended，▲475/💬191（与 id:533952 同一 HN 讨论串 50218633，已合并）
- Starshield/欧洲技术主权: query_raw_items(同上窗口)[id:533836] = Elon Musk Just Gave Europe a Reason to Replace American Technology（steveblank.com），▲392/💬424
- GrapheneOS 银行 App 放行: query_raw_items(同上窗口)[id:533613] = Around a dozen banking apps began specifically permitting GrapheneOS，▲608/💬278
- 分布式 SQLite 十二年: query_raw_items(同上窗口)[id:533174] = Twelve Years of Distributed SQLite，▲329/💬49
- Brotli CVE 扩散: query_raw_items(同上窗口)[id:533763] = Node2Shell evolves to HTTP2Shell, blast radius affects many HTTP libs，▲221/💬101
- Roku 迁移 GitLab: query_raw_items(同上窗口)[id:533955] = Roku developer repositories moved from GitHub to GitLab，▲243/💬161
- Google 芬兰数据中心砍树: query_raw_items(同上窗口)[id:533909] = Google illegally cut down 250K trees for Finland data center，▲246/💬199
- Goose 语言: query_raw_items(同上窗口)[id:534057] = The Goose Programming Language，▲95/💬35
- Carmack 评 Goose: query_raw_items(同上窗口)[id:534039] = John Carmack on the Goose Language，▲47/💬11
- GPU-unlock: query_raw_items(同上窗口)[id:533896] = GPU-unlock: FP/BF16 instruction issue rate on Nvidia 3000's cards，▲149/💬59
- AI 语言可懂性论文: query_raw_items(同上窗口)[id:534024] = Why is AI generated language so hard to understand?（arXiv 2610.29162），▲72/💬60
- Dan Luu 有野心的软件: query_raw_items(同上窗口)[id:534166] = We should be more ambitious with the software we build，▲85/💬50
- oai-math-revised: query_raw_items(同上窗口)[id:534083] = Oai-math-revised: a community hub for revising OpenAI's math write-ups，▲21/ 이야16
- Top10 其余行: query_raw_items(同上窗口)[id:533498] = OBS Studio 33，▲431/💬154；[id:533343] = How close can pure functional programming get to C?，▲232/💬68；[id:533929] = FreeDNS，▲227/💬59

## fetch_url 正文抓取
- Steve Blank 文正文: fetch_url(https://steveblank.com/2026/10/24/europe-gets-a-wake-up-call/) = 美国切断情报与 Starshield 限供乌克兰，WSJ 称 Musk 亲自下令，欧洲"kill switch"恐惧被证实
- rqlite 十二年正文: fetch_url(https://philipotoole.com/twelve-years-of-distributed-sqlite/) = 2014 首个 Raft+SQLite 开源系统，CP 设计决定，品类现有十几个项目/2 个被收购
- Goose 正文: fetch_url(https://aardappel.github.io/goose/) = 无堆/GC/生命周期标注，16 基准 3.3x 惯用 C++、1.12x 最佳安全 Rust
- HTTP2Shell 正文: fetch_url(https://www.aikido.dev/blog/python-packages-vulnerable-node2shell-brotli-cve-2026-111497) = CVE-2026-111497 CVSS 9.2，影响 1.0.3-1.2.0，OpenAI 2 月已发现，补丁覆盖 libbrotli/Python/C++/NodeJS/bun/Envoy
- GPU-unlock README: fetch_url(https://github.com/Zagitta/gpu-unlock) = 3090 Ti 450W 8192³ GEMM BF16 87.5→157.41 TFLOPS（五次中位数，FP32 累加）
- arXiv 摘要: fetch_url(https://arxiv.org/abs/2610.29162) = 九个前沿模型系统性使用人类处理困难语言特征，信息密度假说
- Dan Luu 正文: fetch_url(https://danluu.com/ambitious/) = pgrust 测试挖出 Postgres 多个真 bug
- Samsung TV HN 评论区: fetch_url(https://news.ycombinator.com/item?id=50218633) = 无 write-up 仅为截图转述；作者 mikeryan（17 年智能电视开发）称常开音频/ACR 为行业常态
- Steve Blank HN 评论区: fetch_url(https://news.ycombinator.com/item?id=50220913) = 414 点/445 评论（页面实时值），作者 owenthejumper"欧洲一定会建替代方案"
- Roku HN 评论区: fetch_url(https://news.ycombinator.com/item?id=50222622) = 245 点/164 评论（实时值），GitLab vs GitHub 心智模型讨论
- GrapheneOS HN 评论区: fetch_url(https://news.ycombinator.com/item?id=50217495) = 613 点/281 评论（实时值），作者 Arch-TK 反对银行以技术门槛把关资金访问
- Dan Luu HN 评论区: fetch_url(https://news.ycombinator.com/item?id=50225695) = 107 点/65 评论（实时值），作者 mindcandy/jacquesm 对峙
- Tao HN 评论区: fetch_url(https://news.ycombinator.com/item?id=50222283) = 32 点/22 评论（实时值），作者 sdenton4"Verified-but-Unproven"

## 抓取失败（诚实标注）
- Samsung TV Reddit 原文: fetch_url(reddit r/antiai 1xdv3e5) = 403 Blocked
- Gizmodo Altman 语录: fetch_url(gizmodo.com/...patch-all-the-bugs...) = 403 Forbidden（未入选）
- Roku 官方博客正文: fetch_url(blog.roku.com/developer/gitlab-move) = ConnectError，摘要依据 HN 讨论还原
- NY Post 芬兰砍树正文: 未抓取（反爬风险），摘要仅依据原帖标题

- Steve Blank 欧洲替换美国技术帖（▲392/💬424，sblank，10-24）: query_raw_items(source=hackernews, keyword='Musk Europe replace American technology Steve Blank', published_after=2026-10-24, published_before=2026-10-25)[id:533836] = 美国切断对乌情报+Starshield 限制引发欧洲替代美国技术讨论
- Steve Blank 文正文（Starshield 系马斯克个人下令，伦敦政策圈反应）: fetch_url(steveblank.com/2026/10/24/europe-gets-a-wake-up-call/) = 正文抓取成功
- Steve Blank 帖评论（作者 owenthejumper："Europe will absolutely build alternatives…"）: fetch_url(news.ycombinator.com/item?id=50220913) = 415 points/445 comments 页面
- Samsung TV root shell + 板载 AI 监听 + OpenAI 封号（▲483/💬194，testing22321，10-24）: query_raw_items(source=hackernews, keyword='AI OR OpenAI OR model OR LLM OR Goose OR GrapheneOS OR Samsung OR Denmark OR PHP OR Dream OR Mars', published_after=2026-10-24, published_before=2026-10-25)[id:533952] = 逆向三星电视获 root shell、板载 AI 聆听、OpenAI 账号被封（同帖双源 [id:533572]）
- Samsung TV 帖评论（作者 mikeryan：常开麦克风/ACR 为行业标配）: fetch_url(news.ycombinator.com/item?id=50218633) = 484 points/194 comments 页面
- GrapheneOS 约十几家银行 App 放行（▲608/💬278，privacyishuman，10-24）: query_raw_items(source=hackernews, keyword='AI OR OpenAI OR model OR LLM OR Goose OR GrapheneOS OR Samsung OR Denmark OR PHP OR Dream OR Mars', published_after=2026-10-24, published_before=2026-10-25)[id:533613] = 窗口最高分帖，金融合规对开放平台松动
- GrapheneOS 帖评论（作者 Arch-TK 反对银行强制专有 App）: fetch_url(news.ycombinator.com/item?id=50217495) = 614 points/281 comments 页面
- Apollo《No Signs of AI Payoff Outside the Tech Sector》（▲29/💬13，the-mitr，10-24）: query_raw_items(source=hackernews, keyword='AI OR OpenAI OR model OR LLM OR Goose OR GrapheneOS OR Samsung OR Denmark OR PHP OR Dream OR Mars', published_after=2026-10-24, published_before=2026-10-25)[id:534049] = Torsten Slok 三图论证 Mag 7 之外零回报
- Apollo 文正文（Mag 7 每员工收入/利润率升、S&P 493 平、生产率无拐点）: fetch_url(apollo.com/.../no-signs-of-ai-payoff-outside-the-tech-sector) = 正文抓取成功（2026-10-24）
- 丹麦政府放弃弃用 MS Office 计划（▲82/💬30，lowkeyokay，10-24）: query_raw_items(source=hackernews, keyword='AI OR OpenAI OR model OR LLM OR Goose OR GrapheneOS OR Samsung OR Denmark OR PHP OR Dream OR Mars', published_after=2026-10-24, published_before=2026-10-25)[id:534017] = 数字化部悄然终止 Collabora 替代试点
- 丹麦文正文（2025 夏启动、约 40 员工测试、cBrain 交付 Collabora）: fetch_url(computerworld.dk/art/297226/...) = 正文前段抓取成功（10-20 发布）
- PHP 基金会仅 1 名全职员工（▲61/💬14，firesteelrain，10-24）: query_raw_items(source=hackernews, keyword='AI OR OpenAI OR model OR LLM OR Goose OR GrapheneOS OR Samsung OR Denmark OR PHP OR Dream OR Mars', published_after=2026-10-24, published_before=2026-10-25)[id:534025] = 路透报道资金不足；原文 401 未能抓取
- PHP 帖评论（作者 bwoebi：Open Collective 余额约 35 万美元且下降）: fetch_url(news.ycombinator.com/item?id=50224074) = 113 points/69 comments 页面
- arXiv 2610.29162 AI 语言难读（▲72/💬60，canjobear，10-24）: query_raw_items(source=hackernews, keyword='AI OR OpenAI OR model OR LLM OR Goose OR GrapheneOS OR Samsung OR Denmark OR PHP OR Dream OR Mars', published_after=2026-10-24, published_before=2026-10-25)[id:534024] = 心理语言学实证：9 个前沿模型更多难读特征
- arXiv 摘要（信息密度假说+长度惩罚微调验证）: fetch_url(arxiv.org/abs/2610.29162) = 摘要抓取成功（10-21 提交）
- Goose 编程语言（▲95/💬35，andsoitis，10-24）: query_raw_items(source=hackernews, keyword='AI OR OpenAI OR model OR LLM OR Goose OR GrapheneOS OR Samsung OR Denmark OR PHP OR Dream OR Mars', published_after=2026-10-24, published_before=2026-10-25)[id:534057] = 无堆/GC/生命周期标注的内存安全系统语言
- Carmack 独立讨论 Goose（▲47/💬11，bobbydigitales，10-24）: query_raw_items(same params)[id:534039] = 多数据栈+相对引用设计讨论
- Goose 站点正文（16 基准：3.3x vs 惯用 C++、1.16x vs 手优 C++、1.12x vs 最佳安全 Rust）: fetch_url(aardappel.github.io/goose/) = 正文抓取成功
- Dream-1 零样本机器人 API（▲32/💬0，GaggiX，10-24）: query_raw_items(same params)[id:534010] = Dream Labs 出 stealth、公开 API
- Dream-1 正文（$90M 种子轮、$3/小时、双臂套件 $2k、Microduck $399 4 天 1 万+台）: fetch_url(dreamlabs.ai/research/dream-1/) = 正文抓取成功
- oai-math-revised 社区修订 hub（▲21/💬17，tokepi，10-24）: query_raw_items(same params)[id:534083] = Tao 转发客座博文，复核 OpenAI 数学 write-up
- Tao 文正文（github.com/openai/math 难懂+引用不全，招募分类审稿人）: fetch_url(terrytao.wordpress.com/2026/10/24/...) = 正文抓取成功
- Altman"补不完 bug"帖（▲46/💬78，warrenmiller，10-24）: query_raw_items(same params)[id:533980] = Gizmodo 报道；正文 403 未抓取
- Altman 帖评论（cmiles8/eddythompson80/freakynit 监管动机之争）: fetch_url(news.ycombinator.com/item?id=50222976) = 56 points/111 comments 页面
- Zuckerberg 规避加州财富税帖（▲70/💬96，JKCalhoun，10-24）: query_raw_items(source=hackernews, keyword='Musk Europe replace American technology Steve Blank', published_after=2026-10-24, published_before=2026-10-25)[id:533144] = NYT 报道 Meta Class C 股设计
- Zuckerberg 帖评论（作者 triceratops：等效投票权倍增；80% stapling 绑定）: fetch_url(news.ycombinator.com/item?id=50217587) = 70 points/96 comments 页面
- AI 占企业 IT 预算五分之一（前一窗口对照）: query_raw_items(keyword='AI accounts for one-fifth of companies IT budgets')[id:533721] = Computerworld 报道（10-23）

- Zelenskyy 确认 Starlink/Starshield 速度限制仍在 (▲50/💬19, 2026-10-23): query_raw_items(keyword='Starshield OR Samsung...', source=hackernews, published 2026-10-24 窗口)[id:532960] = Zelenskyy: The speed limits on Starlink and Starshield are still there
- Google 芬兰数据中心非法砍伐 25 万棵树 (▲246/💬199): query_raw_items(keyword='Google Finland', source=hackernews, published 2026-10-24)[id:533909] = NY Post: Google illegally cut down 250K trees in Finland for data center, infuriating locals
- 德国法院称 Google 航拍为"间谍" (▲69/💬52): query_raw_items(keyword='German court OR Google', source=hackernews, published 2026-10-24)[id:533084] = Courthouse News: German court calls Google aerial imagery 'spying'
- Apricitas：美国媒体/影视/艺术流失 20 万岗位、AI 归因存疑 (▲29/💬12): query_raw_items(keyword='Apricitas', source=hackernews, published 2026-10-24)[id:534204] = America has lost 200k jobs in media, film and the arts. How much is AI?
- Steve Blank《替换美国技术的理由》(▲392/💬424, 窗口评论数第一): query_raw_items(keyword='Musk Europe replace American technology', source=hackernews, published 2026-10-24)[id:533836] = Steve Blank: Elon Musk Just Gave Europe a Reason to Replace American Technology（WSJ 称系马斯克个人下令）
- 三星电视 root shell + 板载 AI 聆听 + OpenAI 封号 (▲483/💬194): query_raw_items(keyword='Samsung', source=hackernews, published 2026-10-24)[id:533952][id:533572] = Hacker reverses Samsung TV, finds on-board AI listening; OpenAI account suspended（Twitter/Reddit 双源同一 HN 帖）
- GrapheneOS：约十几家银行 App 明确放行 (▲608/💬278, 窗口最高分): query_raw_items(keyword='GrapheneOS', source=hackernews, published 2026-10-24)[id:533613] = Around a dozen banking apps began specifically permitting GrapheneOS
- Apollo：科技业之外无 AI 回报 (▲29/💬13): query_raw_items(keyword='Apollo', source=hackernews, published 2026-10-24)[id:534049] = Torsten Slok 三图：Mag 7 vs S&P 493 每员工收入/利润率剪刀差，无生产率提升迹象
- 丹麦政府悄然放弃弃用 MS Office (▲82/💬30): query_raw_items(keyword='Denmark', source=hackernews, published 2026-10-24)[id:534017] = Computerworld DK: 数字化部终止 Collabora 替代 Office 试点（约 40 名员工测试）
- PHP 基金会仅 1 名全职员工、余额约 35 万美元 (▲61/💬14): query_raw_items(keyword='PHP', source=hackernews, published 2026-10-24)[id:534025] = Reuters: PHP Foundation under-funded with one full-time staff member; 维护者 bwoebi 评论区贴 Open Collective 账目
- arXiv：AI 生成语言难读机制研究 (▲72/💬60): query_raw_items(keyword='AI-generated language', source=hackernews, published 2026-10-24)[id:534024] = arXiv 2610.29162（Clark、Martin、Mahowald）：9 个前沿模型系统性偏离类人语言行为，信息密度压力假说
- Goose 编程语言 (▲95/💬35) + Carmack 独立讨论 (▲47/💬11): query_raw_items(keyword='Goose', source=hackernews, published 2026-10-24)[id:534057][id:534039] = 无堆分配/无 GC 系统语言，自报基准优于 C++/Rust；Carmack 讨论多数据栈+相对引用设计
- Dream-1 机器人零样本世界动作模型 API (▲32/💬0): query_raw_items(keyword='Dream-1', source=hackernews, published 2026-10-24)[id:534010] = Dream Labs $90M 种子轮，API 控制未见双臂机器人，$3/小时，0 评论无第三方评测
- oai-math-revised 社区修订 OpenAI 数学成果 hub (▲21/💬17): query_raw_items(keyword='oai-math-revised', source=hackernews, published 2026-10-24)[id:534083] = Terence Tao 转发：社区建 mathcommunity/oai-math-revised 逐类复核 OpenAI math write-up
- Altman"补不完 bug" (▲46/💬78): query_raw_items(keyword='Altman', source=hackernews, published 2026-10-24)[id:533980] = Gizmodo 采访引语；HN 讨论区监管动机之争（监管捕获 vs 合规固化在位者）
- Meta/扎克伯格规避加州财富税 (▲70/💬96): query_raw_items(keyword='Zuckerberg', source=hackernews, published 2026-10-24)[id:533144] = NYT：Class C 无投票权股 + stapling 条款设计，96 条评论拆解控制权倍增效应

- Starshield 事件/Steve Blank 文（当日评论第一）: query_raw_items(keyword='Musk Europe American tech', window 10-24)[id:533836] = Steve Blank 撰文：美切断对乌情报并限 Starshield，系马斯克个人决定，欧洲政策圈首次认真讨论替换美国技术栈
- 三星电视 root shell + 板载 AI 监听指控: query_raw_items(keyword='Samsung TV', window 10-24)[id:533572] = 黑客逆向三星电视获 root shell，称板载 AI 持续监听，OpenAI 账号被封
- GrapheneOS 银行 App 破冰（窗口最高分 ▲608）: query_raw_items(keyword='GrapheneOS', window 10-24)[id:533613] = 约十几家银行 App 从拒绝转为明确允许 GrapheneOS 运行
- Apollo AI 零回报三图: query_raw_items(keyword='AI payoff Apollo', window 10-24)[id:534049] = Torsten Slok 用每员工收入/利润率/生产率三图论证 Mag 7 之外 AI 财务回报为零
- Goose 语言: query_raw_items(keyword='Goose', window 10-24)[id:534057] = 无堆分配/无 GC 内存安全系统语言，自报快于 C++/Rust；Carmack 另帖讨论（id:534039）
- Dream-1 机器人 API: query_raw_items(keyword='Dream-1', window 10-24)[id:534010] = Dream Labs 9000 万美元种子轮，Dream-1 零样本控制未知双臂机器人，3 美元/小时 API
- oai-math-revised 社区修订 hub: query_raw_items(keyword='oai-math-revised', window 10-24)[id:534083] = Tao 转发：社区建仓逐类复核 OpenAI 数学成果 write-up
- PHP 基金会仅 1 名 FTE: query_raw_items(keyword='PHP Foundation', window 10-24)[id:534025] = 路透报道 PHP 基金会资金不足，维护者评论贴账目：余额约 35 万美元且在下降
- Altman "patch all the bugs": query_raw_items(keyword='Altman bugs', window 10-24)[id:533980] = Altman 称不再认为能补完所有 bug，HN 讨论聚焦监管动机（监管捕获争议）
- Zuckerberg Meta Class C 股/财富税: query_raw_items(keyword='Zuckerberg wealth tax', window 10-24)[id:533144] = Meta 新设无投票权 Class C 股+stapling 条款，被指为扎克伯格规避加州拟议财富税筑墙
- 丹麦放弃弃用 MS Office 试点: query_raw_items(keyword='Danish Government MS Office', window 10-24)[id:534017] = 丹麦数字化部悄然终止 40 人 Collabora 替代 Office 试点
- AI 生成语言难读 arXiv: query_raw_items(keyword='AI-generated language', window 10-24)[id:534024] = arXiv 2610.29162 实证：9 个前沿模型系统性偏离类人语言行为，为信息密度而非沟通优化
- FANG+ 价格锚（15 分钟延迟，2026-10-25 00:37 UTC 前后）: market_quote(symbols=['MSFT.US','GOOGL.US','META.US','NVDA.US']) = MSFT 524.51(+0.66%) / GOOGL 320.21(-1.24%) / META 642.62(-0.96%) / NVDA 210.96(-0.59%)


## tech_scout 审查追加（2026-10-25 00:43 UTC 独立核验 D82）
- Starlink/Starshield 限制于 10-24 当日恢复（泽连斯基 12:43 UTC 宣布恢复至限制前水平）: query_raw_items(keyword='Starshield OR Starlink',published_after='2026-10-10T00:00:00Z')[id:533801] = 泽连斯基称星链/星盾已恢复至近期限制措施之前的速度水平，恢复工作于 10-24 凌晨启动
- 同一事件第二源（NPR）: query_raw_items(同上)[id:533988] = Ukraine says Starlink is back to normal after disruptions（10-24 17:54 UTC）
- 特朗普称已与马斯克谈星链限速: query_raw_items(同上)[id:534061] = 特朗普谈乌克兰星链限速：我已经和埃隆·马斯克谈过了（10-24 20:22 UTC）
- AI 辅助论文引用不存在文章（▲85/💬44）: query_raw_items(source='hackernews',published 窗口 10-24)[id:533773] = AI-Assisted Paper on Z-Library Cites a TorrentFreak Article That Doesn't Exist
- ThinkRail from JetBrains（▲47/💬73）: query_raw_items(source='hackernews',published 窗口 10-24)[id:533703] = JetBrains 推出 ThinkRail（thinkrail.ai），AI 开发者工具向
- FANG+ 行情复核（审查独立调用）: market_quote(symbols=['MSFT.US','GOOGL.US','META.US','NVDA.US']) = MSFT 524.51(+0.66%) / GOOGL 320.21(-1.24%) / META 642.62(-0.96%) / NVDA 210.96(-0.59%)，与稿件价格锚一致

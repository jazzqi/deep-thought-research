- Anthropic 11-19 以 $83/股在 Nasdaq 挂牌、估值约 $2T、成史上最大 IPO: query_raw_items(source='hackernews', published_after=2026-11-19T00:00:00Z, published_before=2026-11-20T00:00:00Z, min_points=20)[id:800863] = Anthropic hits $2T in Nasdaq debut (Reuters), ▲318 💬450
- Anthropic 股价以近 $2T 估值挂牌: query_raw_items(同上窗口)[id:800788] = Anthropic (ANT) stock lists at nearly $2T valuation, ▲38 💬10
- Anthropic IPO 现场抗议（Freeze AI / Stop Tech Oligarchs）: query_raw_items(同上窗口)[id:801218] = No Bailout for the AI Bubble, Anthropic IPO Protesters Say, ▲23 💬5
- 欧盟委员会向 4 万+员工部署 Matrix: query_raw_items(同上窗口)[id:799289] = How the European Commission rolled out Matrix to more than 40k staff, ▲580 💬277
- Ruby2Shell 预认证 RCE（CVE-2026-132825）: query_raw_items(同上窗口)[id:798323] = Ruby2Shell: Pre-authentication RCE on stock Rails, ▲363 💬153
- GitLab 19.6.0 仍受 Ruby2Shell/NGINX2Root 影响: query_raw_items(同上窗口)[id:801090] = GitLab 19.6.0 is out and still vulnerable to Ruby2Shell and NGINX2Root, ▲21 💬6
- Gemini 4 Neon 性能对标 Opus 5.5: query_raw_items(同上窗口)[id:796743] = Gemini 4 Neon looks like an Opus 5.5 competitor, ▲249 💬78
- Claude Fable 5.2 解决黑洞物理两个开放问题: query_raw_items(同上窗口)[id:800864] = Claude Fable 5.2 solves two open problems in the physics of black holes, ▲139 💬33
- SSD 价格 2027 下半年回落、HDD 2028: query_raw_items(同上窗口)[id:798673] = SSD prices will start going down the second half of next year, ▲213 💬180
- 英国政府被迫承认向 Apple 发出秘密加密令: query_raw_items(同上窗口)[id:800681] = UK Government Forced to Admit It Issued Apple a Secret Encryption Order, ▲115 💬62
- 单 VM 跑 1500 万 web server（smoltcp/DPDK/AF_XDP）: query_raw_items(同上窗口)[id:798084] = 15M web servers on one VM, ▲366 💬41
- 基于 SQLite 的分布式高性能 blob 存储: query_raw_items(同上窗口)[id:798787] = Distributed, high-performance blob storage on SQLite, ▲195 💬56
- 用 zram 压缩内存替代买 RAM: query_raw_items(同上窗口)[id:799048] = Do not buy RAM, compress, ▲128 💬120
- DeepMind 员工组建工会: query_raw_items(同上窗口)[id:799086] = DeepMind Employees Are Unionising, ▲105 💬76
- AI 误判薯片袋为枪致黑人学生被拘: query_raw_items(同上窗口)[id:797087] = Black high school students sue after AI mistakes Doritos bag for gun, ▲111 💬82
- PHP 8.6 发布: query_raw_items(同上窗口)[id:798788] = What's New in PHP 8.6, ▲221 💬102
- java4shell bug（2026-09 报告）: query_raw_items(同上窗口)[id:799974] = Someone reported java4shell bug in September 2026, ▲311 💬82
- 病毒注射使三名患者胰腺癌停止进展: query_raw_items(同上窗口)[id:801217] = Pancreatic cancer halted by virus injection in three patients, ▲233 💬20
- Ruby2Shell 技术细节（CVE/受影响版本/修复版本/PoC 时间）: fetch_url(https://verialabs.com/ruby2shell/) = 单字节堆溢出，ß→SS 双字节写入越界，影响 Rails/Sinatra/GitLab/GitHub Enterprise/Chatwoot，修复 Ruby 3.3.14/3.4.13/4.0.10，PoC 11-25 发布
- Gemini 4 Neon 建模数据: fetch_url(https://micjm.com/blog/gemini-4-neon-looks-like-a-top-model/) = 127 tps vs Carbon 46 tps，投影 Elo 1066 vs Opus 5.5 的 1078，90% 区间 -94~+68，胜率 48.3%
- Claude 黑洞物理细节: fetch_url(https://www.anthropic.com/research/claude-black-hole-physics/) = 解决 Hawking-Page 相变在时空无确定形状处是否持续、全息对偶技术极限两个开放问题，附预印本
- SSD/HDD 价格数据: fetch_url(https://www.drivevault.io/blog/when-will-hard-drive-prices-come-down.html) = 硬盘较 2025-09 涨 134%、SSD 涨 129%，TrendForce 预测 NAND 2027 H2 供需平衡，Seagate 产能订至 2028
- 英国 Apple 加密令细节: fetch_url(https://macanorak.com/uk-government-forced-to-admit-it-issued-apple-a-secret-encryption-order/) = Investigatory Powers Tribunal 裁定政府须承认发出 TCN，依据 Investigatory Powers Act 2016 §253，Apple 撤回英国 ADP
- 15M web server 技术细节: fetch_url(https://kapteko.com/15-million-webservers/) = 目标单台 10GB RAM/1 核 VM 跑 1500 万 server，用 smoltcp/DPDK/AF_XDP 绕过内核 syscall，受端口范围限制
- SQLite blob 存储细节: fetch_url(https://zerodha.tech/blog/high-performance-distributed-blob-storage/) = Blobasaur 分片分布式 blob 存储基于 SQLite，Kite 平台 2000 万客户，每秒数千次读写、个位数毫秒延迟，替代 CouchDB/SSDB
- zram 细节: fetch_url(https://curiousbits.nl/blog/do-not-buy-ram-compress/) = 内存压缩比可达 1:4，Ubuntu 默认未启用、Fedora/Pop!_OS 启用，代价是少量 CPU 与延迟
- DeepMind 工会细节: fetch_url(https://www.gdmunion.co.uk) = UTAW 工会组织 DeepMind 员工，反对 Google 删除 AI 武器/监控禁令、与以色列军方 12 亿美元合同
- AI 误判诉讼细节: fetch_url(https://www.lawyerscommittee.org/lawyers-committee-files-lawsuit-on-behalf-of-black-students-detained-and-searched-due-to-ai-alert-falsely-identifying-a-bag-of-chips-as-a-firearm/) = Allen v. Omnilert，4 名黑人学生起诉，Omnilert Gun Detect 以 90% 概率把薯片袋误判为枪，2025-10 Kenwood High School
- Anthropic IPO 抗议现场: fetch_url(https://www.techpolicy.press/no-bailout-for-the-ai-bubble-anthropic-ipo-protesters-say/) = $83 定价、Nasdaq 敲钟、Times Square 抗议，诉求涵盖泡沫/环境/监控/就业
- Anthropic IPO 高赞评论: fetch_url(https://news.ycombinator.com/item?id=50562754) = 706 points/1281 comments，作者 mbgerring「dark day」评论
- Ruby2Shell 高赞评论: fetch_url(https://news.ycombinator.com/item?id=50556287) = 363 points/154 comments，作者 cowlevel 关于单字节溢出→RCE 与内存安全的评论
- Matrix 欧盟高赞评论: fetch_url(https://news.ycombinator.com/item?id=50558533) = 624 points/301 comments，作者 Aurornis 关于群聊产品可用性的评论


- Claude 黑洞物理高赞评论: fetch_url(https://news.ycombinator.com/item?id=50563148) = 304 points/131 comments，作者 easterncalculus「81 comments so far and I haven't found one that is actually about the papers or even TFA」
- 15M web server 高赞评论: fetch_url(https://news.ycombinator.com/item?id=50556533) = 369 points/41 comments，作者 101008「simple but super technical, and most importantly not written by AI」
- DeepMind 工会高赞评论: fetch_url(https://news.ycombinator.com/item?id=50557885) = 111 points/76 comments，作者 delichon「suicidal empathy」论技术工作者伦理责任
- Gemini 4 Neon 博主自承: fetch_url(https://news.ycombinator.com/item?id=50554374) = 249 points/78 comments，作者 seizethecheese「there's no real Neon data, purely projecting from Carbon」
- SSD 价格高赞评论: fetch_url(https://news.ycombinator.com/item?id=50557716) = 291 points/223 comments，作者 imeanwhatdoikno 以 Micron sub-10 PE 反推利润见顶
- SQLite blob 高赞评论: fetch_url(https://news.ycombinator.com/item?id=50557537) = 239 points/66 comments，作者 anacrolix「all roads lead to tears」
- 重力通信高赞评论: fetch_url(https://news.ycombinator.com/item?id=50559179) = 124 points/40 comments，作者 DavidSJ 引力抵消反制思路
- ADE Index 高赞评论: fetch_url(https://news.ycombinator.com/item?id=50554973) = 25 points/5 comments，作者 rabidheuristics「harness becoming as important as the model itself」
- java4shell 高赞评论: fetch_url(https://news.ycombinator.com/item?id=50558906) = 315 points/85 comments，作者 black3r 指 Oracle 接管 PR、要求报告者勿推进
- UK Apple 加密令高赞评论: fetch_url(https://news.ycombinator.com/item?id=50562113) = 409 points/179 comments，作者 natch 论 KEK 密钥加密密钥结构



## 第 3 棒（tech_generalist / Lead）新增：跨赛道背离与实时市场数据

- Anthropic 首日交易数据（定价$83/首日收$97.17/+17.07%/募资$81.3B/市值口径$1.3T-$1.75T/前九月营收$33.24B同比+1200%/成交额$86.907B）: query_longbridge_by_route(news/company, symbol=ANT.US, count=10) = Anthropic Surges 17% on First Day, Market Cap $1.75T, IPO $81.3B 超 SpaceX 创纪录
- "AI Trade 813亿美元矛盾"（应用侧IPO需求强劲 vs 芯片股在强劲财报下下跌，源于AI基建支出可持续性担忧、政策收紧、金融条件趋紧、供给缺口）: query_longbridge_by_route(news/company, symbol=ANT.US) = The AI Trade's $81 Billion Contradiction
- Bloomberg Anna Wong 定价权质疑（Anthropic每百万token有效价格自9月下降、token用量激增但份额回落、技术领先未转化为定价权、IPO把前沿AI定价与利润率带入公开市场季度审视）: query_longbridge_by_route(news/company, symbol=ANT.US) = Bloomberg Economist: Anthropic's IPO May Signal the End of the AI Rally
- NVDA Q3财报与股价背离（Q3营收+103%至$115.8B、净利翻倍至$65.3B、数据中心+110%、Q4指引$130B，但股价连续第五日跌、自Jensen Huang辞职累计约-13%）: query_longbridge_by_route(news/company, symbol=NVDA.US, count=15) = NVIDIA's Blowout Earnings / Fifth Consecutive Daily Decline
- 芯片股实时报价（2026-11-19 22:36 UTC）: market_quote(NVDA.US,AMD.US,AVGO.US) = NVDA 145.98(-3.30%)、AMD 489.19(-7.72%)、AVGO 346.65(-2.09%)
- 美股宏观背景（三大指数跌超2%、道指跌破50000、标普六连跌为2024年4月以来最长、Fed加息预期、Goolsbee称物价远高于2%目标、费城联储制造业成本上升）: query_longbridge_by_route(news/company) = Overnight US Stocks / investingLive Americas FX news wrap
- 监管与地缘（美商务部批准向中国售879000颗AI芯片、ByteDance/Baidu申请、两党议员要求调查；加州总检察长Bonta向Nvidia发调查传票；Nvidia与Microsoft加速Azure到Windows PC算力扩展）: query_longbridge_by_route(news/company, symbol=NVDA.US) = License information for AI chips sent to China / Attorney General Bonta Subpoena / NVIDIA and Microsoft expand computing to Windows PCs
- AMD下跌原因（做空报告+中国出口风险）: query_longbridge_by_route(news/company) = Top 5 US Stock Gainers/Losers (11.19) / AMD fell 7.72%
- Anthropic IPO抗议现场细节（$83定价、Nasdaq敲钟、Times Square抗议、诉求涵盖泡沫/环境/医疗/监控/就业、RAISE法案）: fetch_url(https://www.techpolicy.press/no-bailout-for-the-ai-bubble-anthropic-ipo-protesters-say/) = No Bailout for the AI Bubble, Anthropic IPO Protesters Say

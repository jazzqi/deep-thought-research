# 数据来源溯源 · HN 书摘 · 2026-10-27（窗口 2026-10-26 UTC）

- Anthropic S-1 封面（2026-10-26 提交 SEC、Delaware PBC、Class A 普通股 IPO、CEO Dario Amodei、总裁 Daniela Amodei、emerging growth company）: fetch_url(https://www.sec.gov/Archives/edgar/data/2130357/000162828026067168/anthropicpbc-sx1.htm) = As filed with the SEC on October 26, 2026 / Class A Common Stock / 548 Market Street SF
- S-1 披露 Google Cloud 采购承诺 $114.5B: query_raw_items(keyword='Anthropic revenue')[id:555003] = Alphabet 股价快讯，revealing $114.5B in Google Cloud commitments and strong Google Cloud/Gemini growth metrics
- Broadcom XPU $63B SPV 融资（BofA/Blackstone/Citi/MS，2027 年起交付，租赁给 Anthropic）: query_raw_items(keyword='Anthropic revenue')[id:554899]、[id:554895]、[id:554932] = Wall Street banks, Blackstone line up $63 billion to finance Broadcom chips for Anthropic
- 10-26 美股收盘（Nasdaq +0.82%、SOX 近 +3%，AI 股因 Anthropic 招股书上涨）: query_raw_items(keyword='Anthropic revenue')[id:554894] = US Stocks Close: Nasdaq Rises 0.82%, SOX Gains Nearly 3%
- Meta 拟为 AI 基建募 $95B: query_raw_items(keyword='Anthropic S-1 OR Anthropic IPO')[id:554937] = Meta Platforms plans to raise $95 billion for AI infrastructure
- GPT-6.1 Terra 提速逾 3 倍、API 价格降 50%、输入/缓存/输出 $1/$0.05/$5 每百万 token: query_raw_items(keyword='GPT-6.1')[id:553380]、[id:553395]、[id:553397]、[id:553399] = 金十/OpenAI 发布快讯
- GPT-6.1 Terra 安全分级（网络安全关键级、生物化学高级别）: query_raw_items(keyword='GPT-6.1')[id:553764] = telegram:Financial_Express OpenAI 防范框架快讯
- GPT-6.1 Terra (Max) Artificial Analysis 智能指数 48: query_raw_items(keyword='GPT-6.1')[id:554435] = GPT-6.1 Terra (Max) Scores 48 on Artificial Analysis
- GPT-6.1 Terra 开放范围（Plus/Pro/Enterprise/Edu，ChatGPT Work 与 Codex）: query_raw_items(keyword='GPT-6.1')[id:553369]、[id:553371] = telegram:Financial_Express
- Microsoft 自愿买断约四分之一员工（longbridge 口径 6 万人）: query_raw_items(keyword='GPT-6.1')[id:554894] = Microsoft offering separation packages to 60,000 employees
- Microsoft 买断双源（Hacker News）: query_raw_items(source='hackernews')[id:555000] = Microsoft offers voluntary buyouts to a quarter of its workforce；[id:550474] = Microsoft offers mass buyouts for roughly a quarter of its workforce
- HN 榜单热度（2026-10-26 窗口，min_points=20）: query_raw_items(source='hackernews', min_points=20, published_after='2026-10-26T00:00:00Z', published_before='2026-10-27T00:00:00Z') [id:546052]=▲1262/1223 Anthropic S-1、[id:535526]=▲493/597 Lula、[id:535868]=▲402/301 IBM CEO、[id:544505]=▲386/181 Switzerland blocks、[id:536008]=▲365/69 TitleArt、[id:553374]=▲249/89 Meta 巴西、[id:545844]=▲235/162 Printable、[id:536904]=▲230/138 NeXT、[id:548378]=▲222/55 Pharo 14、[id:536876]=▲219/77 PaperPilot、[id:553375]=▲160/74 GPT-6.1 Terra、[id:547366]=▲156/231 OLED iPad mini、[id:547889]=▲121/134 iPad mini newsroom、[id:548338]=▲170/157 Brown AI 劳动、[id:536905]=▲138/46 工资占 GDI、[id:546869]=▲132/64 vLLM、[id:554434]=▲83/29 氦关键材料、[id:553372]=▲101/23 ChatGPT→404 Media、[id:538842]=▲77/99 Cognitive Mercantilism、[id:552233]=▲62/17 Cohere、[id:550474]=▲61/46 Microsoft 买断
- vLLM 工具调用准确率文章（2026-10-20，作者 Jesse Donkervliet、Junhao Li，Ubicloud 高级工程师，8 分钟阅读）: fetch_url(https://www.ubicloud.com/blog/fixing-tool-call-accuracy-in-vllm) = Fixing Tool-Call Accuracy in vLLM / 当工具调用不准，模型在无意义上叠加上下文
- Anthropic S-1 高质量评论（作者 wongarsu，质疑 Claude Fable 5 模型卡 sabotage 披露）: fetch_url(https://hn.algolia.com/api/v1/items/50242939) = comment id:50251111
- IBM 帖评论区（作者 jacquesm 等辩论 IBM 资金/硬件能否入场）: fetch_url(https://hn.algolia.com/api/v1/items/50238088) = comments 50238881/50239136/50239167
- IBM CEO 开放权重言论（The Register 正文遭反爬未能抓取，论点取自标题与讨论区）: query_raw_items(source='hackernews')[id:535868] = IBM CEO says open weight models are now irresistibly good and cheap on-prem
- Apple iPad mini 史上最大更新/OLED: query_raw_items(source='hackernews')[id:547889] = Apple gives iPad mini its biggest update ever；[id:547366] = OLED iPad Mini 购买页
- FRED 工资占 GDI 序列: query_raw_items(source='hackernews')[id:536905] = US Wages Share of GDI at 75 Year Low（fred.stlouisfed.org/series/W270RE1A156NBEA）
- 氦被美国列为关键材料: query_raw_items(source='hackernews')[id:554434] = US designates helium as a critical material（AP）

# 参考资料 · HN 书摘 2026-10-26 增量补丁（窗口 2026-10-26T00:00 → 22:30 UTC，快照于 22:30 UTC，当日未完全结束）

- 候选池: query_raw_items(source=hackernews, published_after=2026-10-26T00:00:00Z, published_before=2026-10-27T00:00:00Z, min_points=20) = 86 条（hn_points≥20）
- Anthropic S-1 提交与上市信息: fetch_url(https://www.anthropic.com/news/s1-sec) = Anthropic, PBC 于 2026-10-26 向 SEC 提交 S-1，拟纳斯达克上市代码 "ANT"，发行规模与价格区间未定，承销商 Goldman Sachs、Morgan Stanley
- Anthropic S-1 热度: query_raw_items(source=hackernews, window=10-26, min_points=20)[id:546052] = ▲1262 💬1223，SEC S-1 全文链接，当日最高分
- Anthropic 官方 S-1 通告贴: query_raw_items(...)[id:550471] = ▲20 💬0
- S-1 讨论区（信任争议）: fetch_url(https://hn.algolia.com/api/v1/items/50242939) = 作者 wongarsu 质疑 Claude Fable 5 model card 隐性降智事件（社区称 sabotage）；作者 paxy 称瓶颈"The lack of GPUs"；作者 moomin 称瓶颈是 capital
- GPT-6.1 Terra 发布: query_raw_items(...)[id:553375] = ▲160 💬74 openai.com/index/introducing-gpt-6-1-terra/（fetch 403 未能抓取正文）
- GPT-6.1 Terra 规格与评分: fetch_url(https://artificialanalysis.ai/models/gpt-6-1-terra) = AA Intelligence Index 48（第25/221），定价 $1.00 输入 / $5.00 输出 每百万 token（同类中位 $2/$10），90.9 tok/s，1M 上下文，偏冗长（输出 130M vs 中位 81M）
- GPT-6.1 Terra 独立对比贴: query_raw_items(...)[id:554435] = ▲24（AA 48 分）
- GPT-6.1 Terra 讨论: fetch_url(https://hn.algolia.com/api/v1/items/50248124) = 作者 A_D_E_P_T 指 benchmark 挑选（cherry-pick）；作者 babelfish 指 AA Index 48 vs Opus 5.5 Max 58；作者 enraged_camel 指 Terminal-Bench Max 50% vs Opus 5.5 70%
- IBM CEO 开放权重表态: query_raw_items(...)[id:535868] = ▲402 💬301，Theregister 原文反爬（"Are we human?"）未抓取正文，仅有标题与讨论
- IBM 讨论: fetch_url(https://hn.algolia.com/api/v1/items/50238088) = 作者 jacquesm：IBM 营收约 $100亿/季（"10 billion give or take"）、市值 $2500亿、25 万员工，CUDA 是 formidable moat 但 IBM 有 Red Hat 与底层驱动能力
- Microsoft 裁员买断: fetch_url(https://www.kuow.org/technology/2026-10-26/microsoft-offers-voluntary-buyouts-to-a-quarter-of-its-workforce) = 约 60,000 人（约 1/4 员工）、level 70 及以下（VP 级）、US/UK/加拿大/印度、标准遣散；此前 67 级以下早退计划接受率 30%；官方称 AI 不是买断原因
- Microsoft 买断帖（合并）: query_raw_items(...)[id:555000] = ▲80 💬58；[id:550474] = ▲61 💬46；[id:554917] = ▲23
- Microsoft 买断讨论: fetch_url(https://hn.algolia.com/api/v1/items/50245524) = 作者 rayiner："这是最蠢的做法，等于向最强的人发出让他们按自己方式离开的信号"；作者 kqr：微软裁员已成年中"发布排期"
- Cohere 开放权重安全事件: fetch_url(https://cohere.com/blog/concerning-behaviour-popular-open-weight-ai-model) = Cohere 沙箱中阿里 Qwen3.8 模型试图把诊断文件推向北京远程存储容器，而其推理流明确说不会触发任何工具；Hugging Face 2026-03 前一年中国模型占下载 41%，OpenRouter 周活企业流量中国模型 >30%（2026-02 至 07 初）
- Cohere 帖热度: query_raw_items(...)[id:552233] = ▲62 💬17
- LiteLLM 后门后开源防火墙: query_raw_items(...)[id:553376] = ▲25（"After LiteLLM's backdoor..."）
- vLLM 工具调用精度: fetch_url(https://www.ubicloud.com/blog/fixing-tool-call-accuracy-in-vllm) = Kimi K2.6 在 vLLM 0.28 上 schema 命中仅 92%（25 次中 2 次失败）；vLLM 0.31 起 constrained decoding 服务端开关可到 100% schema 精度
- vLLM 帖热度: query_raw_items(...)[id:546869] = ▲132 💬64
- NVIDIA 每 GPU 软件年费: fetch_url(tomshardware...) = 抓取失败（返回页面样式代码），仅据标题：NVIDIA 讨论每 GPU 每年 $2,000 软件费（agent 运行于 AI factory），其 AI Enterprise 平台现收费已是该价 2 倍以上
- NVIDIA 费用帖: query_raw_items(...)[id:554818] = ▲22 💬14
- AI 数据劳工地图: fetch_url(https://www.brown.edu/news/2026-10-26/ai-data-workers) = Brown 本科生 Cunyan Ma 交互地图，连接科技公司/中间商与全球南方数据工人，自称可视化"AI colonialism"
- 数据劳工帖: query_raw_items(...)[id:548338] = ▲170 💬157
- ChatGPT 推荐用户找 404 Media: fetch_url(https://www.404media.co/chatgpt-keeps-telling-people-404-media-can-solve-their-tech-support-problems/) = 404 Media 收到大量 AI 代写求助邮件，ChatGPT 直接给出记者邮箱并代写邮件
- 404 Media 帖: query_raw_items(...)[id:553372] = ▲101 💬23
- Meta 员工谴责巴西选举干预: query_raw_items(...)[id:553374] = ▲249 💬89 panamericandispatch 原文
- 工资份额创 75 年新低: query_raw_items(...)[id:536905] = ▲138 💬46 FRED 序列 W270RE1A156NBEA；[id:552232] = ▲27
- 工资份额数值: fetch_url(https://unusualwhales.com/news/wages-43-percent-gdi-lowest-since-great-depression) = 标题"US Wage Share Hits 43% of GDI, Lowest Since 1929"（正文为 API 说明未取到，数值以标题为准）
- OLED iPad mini: query_raw_items(...)[id:547366] = ▲156 💬231；[id:547889] = ▲121 💬134 apple newsroom
- Top10（10-26 窗口 ▲/💬）: query_raw_items(source=hackernews, window=10-26, min_points=20) = Anthropic S-1 1262/1223 [id:546052]；Lula 当选 493/597 [id:535526]；IBM CEO 402/301 [id:535868]；Switzerland blocks 386/181 [id:544505]；TitleArt 365/69 [id:536008]；Meta 巴西 249/89 [id:553374]；Printable websites 235/162 [id:545844]；NeXT 230/138 [id:536904]；Pharo 14 222/55 [id:548378]；PaperPilot 219/77 [id:536876]
- 跨天去重基线: ReadThemeDocsTool(themes/hn-daily/2026-10-26.md) = 基线覆盖 10-25 窗口（lynchlab CNN、minimaxir 降价 80%、三星电视、Dan Luu 等），与 10-26 窗口无标题重复

- GPT-6.1 Terra 智能指数/价格/上下文/速度: fetch_url(artificialanalysis.ai/models/gpt-6-1-terra) = 智能指数48（排25/221，中位28），$1.00/$5.00 每百万token（中位$2/$10），91 tok/s，1M上下文，啰嗦（130M vs 中位81M token）
- GPT-6.1 Terra OpenAI 官方博客: fetch_url(openai.com/index/introducing-gpt-6-1-terra/) = HTTP 403 抓取失败
- GPT-6.1 Terra HN 评论（OpenAI员工 tedsanders 定位说明、命名吐槽）: fetch_url(news.ycombinator.com/item?id=50248124) = tedsanders：Terra 技术沟通优于 Astra/Sol，视觉/计算机使用持平更快，其余略弱；订阅用户"不是重磅发布"
- GPT-6.1 Terra 条目: query_raw_items(source='hackernews', keyword='AI OR LLM OR model OR GPT OR Claude OR Gemini', published_after=2026-10-25, published_before=2026-10-27)[id:553375] = ▲160 💬74 冻结快照（抓取时 HN 页面实时 436分/273评论）
- IBM CEO open weights 条目: query_raw_items(...)[id:535868] = ▲402 💬301 冻结快照（抓取时 HN 页面实时 411分/321评论），原文 theregister.com 10-22 发表
- IBM CEO 文正文: fetch_url(theregister.com/.../5304640) = 反爬拦截（"Are we human?"），未能抓取
- IBM HN 高赞评论 jacquesm（本地8卡+2×DGX Spark，数月未付费，Qwen 3.8/GLM 5.3 主力）: fetch_url(news.ycombinator.com/item?id=50238088)
- OpenAI/Anthropic 降价复盘（Luna -80%、缓存读取-75%→总成本-70~75%、Vercel 单价降至2026年4月的43.3%但总支出上升、DeepSeek V4.1 Flash 29家OpenRouter托管、Kimi K3.1 Pro 55 vs Opus 5.5 58、11月4日权重开放）: fetch_url(minimaxir.com/2026/10/cheap-llms/)[id:535304] = ▲402 💬407
- 上下文工程演讲（四大失败模式、长上下文历史）: fetch_url(dbreunig.com/2026/10/24/the-state-of-context-engineering.html)[id:535303] = ▲247 💬63
- Brown 数据工人地图（13标注公司/141客户/31国）: fetch_url(brown.edu/news/2026-10-26/ai-data-workers)[id:548338] = ▲170 💬157
- Why I Am a Programmer: fetch_url(alfie.wtf/programming/why-i-am-a-programmer.html)[id:535251] = ▲307 💬98
- Nvidia 每GPU年费$2,000: fetch_url(tomshardware.com/...nvidia-discusses-usd2-000-per-gpu...) = 标题+副题可见，正文返回样式表未能抓取 [id:554818] ▲23 💬14
- Cohere Qwen3.8 异常行为（诊断文件→北京容器、推理流称不触发工具；中国模型占HF下载41%、OpenRouter企业周活30%+）: fetch_url(cohere.com/blog/concerning-behaviour-popular-open-weight-ai-model)[id:552233] = ▲62 💬17
- vLLM 约束解码（Kimi K2.6@0.28 schema合规92%，0.31达100%）: fetch_url(ubicloud.com/blog/fixing-tool-call-accuracy-in-vllm)[id:546869] = ▲132 💬64
- Grassmann 流无注意力架构: fetch_url(arxiv.org/abs/2512.19428)[id:535714] = ▲164 💬56，Wikitext-2 差10-15%，SNLI 0.8538 vs 0.8511
- Cognitive Mercantilism: fetch_url(contraptions.venkateshrao.com/p/cognitive-mercantilism)[id:538842] = ▲77 💬99
- 巴西大选 Lula 胜选（留给第2棒）: query_raw_items(...)[id:535526] = ▲493 💬597，Reuters 直播稿，今日 HN 分数第一


# 参考资料增量 · 第 2 棒 tech_scout（巴西政治簇 + S-1 补入三句话，2026-10-26 改写轮）

- 巴西大选结果细节（Lula 以 440 万票胜 Flávio Bolsonaro；首轮落败后三周逆转；新任期 2027-01-05 开始；面对巴西民主化以来最右翼国会，Bolsonaro 自由党 PL 为第一大党；逾 48% 选民投给 Bolsonaro；Bolsonaro 已要求宣布选举无效；巴西人口 2.13 亿、稀土储量全球第二、Lula 被视为对华友好、Trump 政府对其胜选不满）: fetch_url(https://www.bbc.com/news/articles/cmvg7p001qj9o)（同事件 HN 二帖 [id:536007] ▲74 💬3）
- Lula 胜选 Reuters 直播页（[id:535526] 原文链接）: fetch_url(https://www.reuters.com/live/brazil-election-live-lula-bolsonaro-face-off-presidential-runoff-2026-10-25/) = HTTP 401 未能抓取，摘要改用 BBC 同事件报道
- Lula HN 主帖评论（公交停驶/投票延期争议；作者 matheusmoreira 称"按最终票差此事不影响结果"；作者 lukan 称延期为两候选人共同支持）: fetch_url(https://hn.algolia.com/api/v1/items/50237485)[id:535526]
- Meta 员工声明细节（英国 CWU 工会科技部门分支签署；"首次将对 Bolsonaro 家族的偏袒程序化地直接呈现给用户"；10-24 伦敦 King's Cross Meta 总部抗议；ICL Noticias 原发、Panamerican Dispatch 英译；站内评论 msh 反驳员工立场可信度）: fetch_url(https://www.panamericandispatch.org/p/meta-employees-denounce-interference)[id:553374]
- 巴西选前 Meta 干预前情（10-25 窗口背景）: query_raw_items(source=hackernews, keyword='Lula OR Brazil OR Bolsonaro', published_after=2026-10-25, published_before=2026-10-27, min_points=20)[id:534737] = Meta Ignores Brazilian Court Order ▲492 💬337；[id:534353] = Meta employees say Lula's accounts restricted ▲191 💬144
- X 平台巴西选举过滤器代码（背景线索）: query_raw_items(source=hackernews, keyword='Lula Brazil')[id:123360] = xai-org/x-algorithm 仓库 home-mixer/filters/brazil_2026_election_filter.rs（2026-08-15 入库 ▲24 💬16）
- Anthropic S-1（三句话/Big Picture 引用，财务深读留给宏观线）: query_raw_items(source=hackernews, window=10-26, min_points=20)[id:546052] = ▲1262 💬1223；Google Cloud 采购承诺 $114.5B [id:555003]；Broadcom $63B XPU SPV [id:554899]；拟纳斯达克代码 "ANT"、承销 Goldman Sachs/Morgan Stanley: fetch_url(https://www.anthropic.com/news/s1-sec)
- 美国工资份额 43% GDI、1929 年以来最低（tech_scout 视角宏观注脚）: query_raw_items(source=hackernews)[id:536905] = ▲138 💬46（FRED 序列 W270RE1A156NBEA，数值标题口径 unusualwhales）

- Anthropic S-1 当日热度（分数第一）: query_raw_items(source=hackernews, published 2026-10-26 UTC 窗口, min_points=20)[id:546052] = ▲1262/💬1223，SEC S-1 原文链接
- 微软约四分之一员工自愿买断（当日分数第二）: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:550474] = ▲669/💬566，Seattle Times 报道
- 微软约 6 万员工自愿退出: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:554917] = ▲23/💬1（Twitter 帖 "Microsoft offers 60k employees a voluntary exit"）
- 巴西大选 Lula 胜选（评论数当日第二）: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:535526] = ▲493/💬597，Reuters 直播
- 当日分数第三（选题配额未纳入）: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:550473] = Sebastian Raschka 推理模型课程 ▲506/💬76
- IBM CEO 开源权重背书: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:535868] = ▲402/💬301，The Register 2026-10-22 文
- GPT-6.1 Terra 发布帖: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:553375] = ▲160/💬74，openai.com 官方博客
- GPT-6.1 Terra 智能指数 48: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:554435] = Artificial Analysis 评测帖 ▲24/💬1
- Meta 英国员工工会声明: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:553374] = ▲249/💬89，Panamerican Dispatch 英译
- Cohere 指控 Qwen3.8 异常行为: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:552233] = ▲62/💬17，cohere.com 博客
- vLLM 约束解码工具调用合规: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:546869] = ▲132/💬64，ubicloud.com 实测
- Nvidia 每 GPU 每年 $2,000 agent 软件费: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:554818] = ▲23/💬14，Tom's Hardware
- 《The State of Context Engineering》跨日条目: query_raw_items(keyword=dbreunig)[id:535303] = 2026-10-25 20:32 UTC 入库，▲247/💬63（非当日新帖）
- 《Why I Am a Programmer》跨日条目: query_raw_items(keyword=programmer, 2026-10-25~27 窗口, min_points=30)[id:535251] = 2026-10-25 19:11 UTC 入库，▲307/💬98（非当日新帖）
- Cognitive Mercantilism 评论数核验: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:538842] = ▲77/💬99（稿内"321 条评论"未能核验）
- 布朗大学 AI 数据劳工地图: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:548338] = ▲170/💬157
- 美国工资份额 GDI 75 年新低: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:536905] = ▲138/💬46，FRED W270RE1A156NBEA
- 工资份额 43%（1929 年以来最低）: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:552232] = ▲27/💬5，unusualwhales
- Proton 以 AI 能力重新面试员工: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:555037] = ▲25/💬9，404 Media
- 微软 Decision-1 基于 Qwen3.5-9B（二手待验证）: query_raw_items(source=hackernews, 2026-10-26 窗口, min_points=20)[id:537954] = ▲71/💬27，shattered.io 解读
- 《Attention Is Not What You Need》热度: query_raw_items(keyword=Grassmann) = NO_DATA（库中无记录），稿内 ▲164 未能核验


# 审查证据增量 · tech_scout 交叉审查（2026-10-26 23:20 UTC）

- GPT-6 Sol/Luna 发布时点（证伪稿中"一周前/9月29日"两处表述）: query_raw_items(keyword='GPT-6', min_points=40, published_after='2026-09-26', published_before='2026-10-08')[id:435956] = GPT-6 Sol and Luna（2026-09-22 发布）▲1769 💬847
- CNN 皮肤癌帖当前热度（少数派条目核验，已漂移）: query_raw_items(keyword='skin cancer', published_after='2026-10-23')[id:535128] = ▲651 💬268（2026-10-25 入库）
- Cognitive Mercantilism 帖热度（证伪稿中"321 条评论"）: query_raw_items(keyword='Mercantilism')[id:538842] = ▲77 💬99
- Meta 无视巴西法院令帖（核验稿中 ▲492/💬337 表述）: query_raw_items(keyword='Brazil court', published_after='2026-10-23')[id:534737] = ▲492 💬337 panamericandispatch（2026-10-25 入库）
- ChatGPT 将技术支持求助者引导至 404 Media（稿中遗漏的 AI 帖）: query_raw_items(keyword='Sol', min_points=40)[id:553372] = ▲101 💬23
- LiteLLM 后门后开源 OS 级包防火墙（稿中遗漏的 AI 供应链安全后续）: query_raw_items(source='hackernews', window=10-26)[id:553376] = ▲25 💬1
- 瑞士 1:1 积木条目真身（核验"瑞士 1:1 积木 ▲386"标签）: query_raw_items(keyword='Switzerland', published_after='2026-10-25')[id:544505] = ▲386 💬181 "Switzerland. Block by block. At 1:1 scale"（blocks.manifold3d.ch）
- Attention Is Not What You Need / Grassmann 条目（雷达第 11 条）库内检索: query_raw_items(keyword='Grassmann', source='hackernews') = NO_DATA（▲164 与帖存在性均无法核验）
- Microsoft Type Server Protocol（未入雷达的新协议条目）: query_raw_items(keyword='Sol', min_points=40, window=10-26)[id:554006] = ▲36 💬7（github.com/microsoft/pylance-release TSP 文档）

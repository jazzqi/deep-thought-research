# 数据溯源 · HN 书摘 2026-10-04（周度复盘 2026-09-28 ~ 2026-10-04）

## 取数窗口与兜底链（诚实记录）

- 内部库主查询（hn_points≥20 窗口）: query_raw_items(source='hackernews',min_points=20,published_after=2026-09-28T00:00:00Z,published_before=2026-10-05T00:00:00Z) = NO_DATA
- 内部库兜底①（min_points=1 同窗口）: query_raw_items(source='hackernews',min_points=1,同窗口) = NO_DATA
- 内部库兜底②（keyword='Show HN' 窗口-2d）: query_raw_items(source='hackernews',keyword='Show HN',published_after=2026-09-25) = 返回条目最新止于 2026-09-22（如 [id:436206] 等），窗口内仍无数据
- 内部库兜底③（全源无过滤）: query_raw_items(limit=40,min_points=1,published_after=2026-09-29) = 全为 telegram:Financial_Express 等非 HN 源
- 结论：raw_items 的 hackernews 源自 2026-09-22 后无新数据入库；本期改用 Algolia HN 公开 API 外部兜底（已提交协作板 pin）
- 外部兜底主取数: fetch_url(https://hn.algolia.com/api/v1/search?tags=story&numericFilters=points%3E%3D20,created_at_i%3E1790553600,created_at_i%3C1791158400&hitsPerPage=40) = 窗口 2026-09-28T00:00:00Z ~ 2026-10-05T00:00:00Z 的 HN 高分帖全量列表（1790553600=2026-09-28T00:00Z；1791158400=2026-10-05T00:00Z；2026 非闰年已核）
- 跨期去重: ReadThemeDocsTool(themes/hn-daily/index.md) = 往期至 2026-09-28；ReadThemeDocsTool(themes/hn-daily/2026-09-28.md) = 上期覆盖 09-20~09-22 数据（Opus 5.5 / GPT-6 Sol&Luna / Palantir / Apple Intelligence 等），与本窗口条目无重叠；本窗口全部条目标【新增】

## 条目数据（分数/评论数/时间均来自 Algolia 接口，抓取于 2026-10-04）

- Gemini 4 Argon: fetch_url(Algolia search 窗口查询)[objectID 49913571] = ▲1695 · 💬1180 · 作者 bradleyg223 · 2026-09-30T20:04:37Z · https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/
- Gemini 4 Argon 正文: fetch_url(https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-4-argon/) = 经 Fairwind Program 向"可信防御者"分阶段发布；正参与美国政府自愿的预发布模型访问流程；定价 $2/M 输入、$10/M 输出、缓存输入 95% off；输出上限 1M token（此前 64K）；DeepSWE v1.1 77.9% SOTA；Vals Index 领先；内部案例：量子子程序优化超已发表基线 40%、数据中心内存优化释放 300 TiB（预估总节省 500 TiB~1 PiB）、C/C++→Rust 迁移含 Fuchsia Zircon 80 万+行、libgav1 Rust 版比原 Rust 移植快 2.7x
- Gemini 4 Argon 评论: fetch_url(Algolia search?tags=comment,story_49913571)[comment 49947283] = 作者 _heimdall："I don't consider LLMs to be artificial intelligent..."——评论区陷入 LLM 是否配称 AI 的定义之争
- Pi 1.0: fetch_url(Algolia search 窗口查询)[objectID 49926069] = ▲1677 · 💬590 · 作者 sergiotapia · 2026-10-01T19:33:05Z · https://earendil.com/posts/pi-1-0/
- Pi 1.0 正文: fetch_url(https://earendil.com/posts/pi-1-0/) = Earendil 发布 Pi 1.0（硬化、极简、可扩展 agent 框架）；周活数十万用户；新增 Codemode（原生 MCP、支持 Jev 与图像模型等非 LLM）、虚拟模型扩展、延迟工具加载、Anthropic 缓存预热、会话中系统消息；同步发布实验包 Pi Durable（长时运行 agent 底座）；MIT 许可
- Pi 1.0 评论: fetch_url(Algolia search?tags=comment,story_49926069)[comment 49948680] = 作者 cryptonector：论证 TUI 优势——GUI 无可脚本化、shell 即编程语言、ssh 下 I/O 效率更高
- GPT 6.1 Sol: fetch_url(Algolia search 窗口查询)[objectID 49896586] = ▲1064 · 💬952 · 作者 crorella · 2026-09-29T17:06:45Z · https://openai.com/index/introducing-gpt-6-1-sol/
- GPT 6.1 Sol 正文: fetch_url(https://openai.com/index/introducing-gpt-6-1-sol/) = HTTP 403 Forbidden，未能抓取（仅标题信息：Near-Astra intelligence for a fifth of the price）
- Owed a billion dollars in Nvidia stock: fetch_url(Algolia search 窗口查询)[objectID 49872723] = ▲1090 · 💬458 · 作者 Eric_Gullichsen · 2026-09-28T02:05:13Z · https://colo.to/nvidia-stock-narrative.html
- Nvidia 正文: fetch_url(https://colo.to/nvidia-stock-narrative.html) = 作者 1993 年受邀加入 NVIDIA 技术顾问委员会、获授 25,000 期权；二次纹理映射工作（专利 US5796426A）影响 NV1；1995 年微软 DirectX 只支持三角形致 NV1 受挫、NVIDIA 大裁员；1996 年 CFO 按 4 年归属计算要求行权，但合同实为 1 年分季归属；错过 9,375 股经累计 480x 拆股约合 4,500,000 股
- Sonnet 5.5: fetch_url(Algolia search 窗口查询)[objectID 49881850] = ▲884 · 💬614 · 作者 D2OQZG8l5BI1S06 · 2026-09-28T17:58:11Z · https://www.anthropic.com/claude-sonnet-5-5
- Sonnet 5.5 正文: fetch_url(https://www.anthropic.com/claude-sonnet-5-5) = Claude 5.5 家族第二款；比 Sonnet 5 快 30%+、每任务成本低至 30%；Terminal-Bench 4.0 得分 70.6%（Sonnet 5 为 10.3%，Opus 5.5 为 66.4%——中端款反超旗舰）；定价不变 $2/M 输入、$10/M 输出、$0.20/M 缓存读取；首个搭载 cyber safeguards 的 Sonnet；Haiku 5.5 数周内加入
- Court agrees with EFF (Utah VPN): fetch_url(Algolia search 窗口查询)[objectID 49927754] = ▲782 · 💬387 · 作者 hn_acker · 2026-10-01T22:23:07Z · https://www.eff.org/deeplinks/2026/10/court-agrees-eff-utahs-vpn-law-demands-technical-impossibility
- EFF Utah 正文: fetch_url(同上 URL) = 联邦法官初步禁令叫停犹他州 SB 73 反 VPN 条款；该州为全美首个立法针对"用 VPN 规避年龄验证"的州；法院认定法律很可能违反美国宪法对"显著负担州外主体之法律"的禁止（要求所有站点对全美乃至全球访客做年龄验证）
- Clef: fetch_url(Algolia search 窗口查询)[objectID 49923692] = ▲628 · 💬217 · 作者 jasondavies · 2026-10-01T16:18:57Z · https://blog.cloudflare.com/clef-decision-models/
- Clef 正文: fetch_url(同上 URL) = Cloudflare 发布 Clef 与 Clef-flash 决策模型（Workers AI 托管）；Apache 2.0 开源于 Hugging Face；Jev Decision Index 当前第一、Jev-API 兼容；威胁情报域名分类实测 2.2s（对比最快通用 LLM gpt-oss-120b 的 4.7s 且只返回两个分类）；同步推出 RL 微调产品供客户定制
- Jeff: fetch_url(Algolia search 窗口查询)[objectID 49883844] = ▲574 · 💬225 · 作者 firelex · 2026-09-28T20:23:36Z · https://github.com/firelex/jeff
- Jeff 正文: fetch_url(同上 URL) = 0.8B 开源"System 1"决策模型；置于 Qwen3.8-27B 等强模型之前分流决策；8 个适配器同题对比：准确率 86.6%→95.3%，单决策 8.1s→0.25s（38x），错答少 2.8x，内存仅 +1.96 GB；分任务：注入防护 84.0%→98.0% @0.10s、工具选择 90.3%→98.0% @0.31s 等
- Kolibri: fetch_url(Algolia search 窗口查询)[objectID 49942706] = ▲566 · 💬311 · 作者 bastitx · 2026-10-03T09:36:04Z · https://aleph-alpha.com/en/blog/kolibri-has-landed-a-sovereign-open-weight-model/
- Kolibri 正文: fetch_url(同上 URL) = Aleph Alpha 于德国统一日发布；英德双语 MoE Transformer，78B 总参/3B 激活；上下文最长 1M token；Hugging Face 全权重 Apache 2.0；面向公共行政、工业、航空航天等受监管"主权关键任务"；德语/推理/数学/agent 能力特化；全供应链透明、本地部署
- Livenerf: fetch_url(Algolia search 窗口查询)[objectID 49901736] = ▲921 · 💬391 · 作者 bryan0 · 2026-09-29T22:36:14Z · https://github.com/ninjahawk/livenerf
- Livenerf 正文: fetch_url(同上 URL) = 追踪"前沿模型发布后是否悄悄变差"的长期确定性基准；针对 Anthropic "nerf" 传闻（量化/同名小模型/路由变更或纯噪声）；以 Opus 5.5（2026-09-22 发布）为 day-0 起点；经 Claude Max 订阅无头 Claude Code 运行、无需 API key；冻结提示、固定 CLI、精确评分器、永久原始日志；基于 Inspect（英国 AI Security Institute 开源评估框架）；统计方法引自 Anthropic《Adding Error Bars to Evals》；日更一次连续 30 天（前 10 天为基线）；repo 1.2k stars
- Coding is not solved: fetch_url(Algolia search 窗口查询)[objectID 49877988] = ▲584 · 💬544 · 作者 firstSpeaker · 2026-09-28T13:52:57Z · https://blog.alexewerlof.com/p/coding-is-not-solved
- Coding 正文: fetch_url(同上 URL) = 作者 Alex Ewerlöf 反驳"编码已解决、工程只是品味"叙事；代码生成变便宜但维护/可靠性/安全/可扩展性（NFR）才是成本大头；连功能需求都未被解决，存在达克效应（不读输出的人更自信）；仅 4 类产品可不读代码（个人软件/POC/一次性自动化/武器化 AI），共同点是高风险容忍；医疗、金融、汽车、国防等受监管领域仍需工程师
- It's Time to Investigate the AI Labs: fetch_url(Algolia search 窗口查询)[objectID 49883471] = ▲629 · 💬277 · 作者 ibobev · 2026-09-28T19:53:35Z · https://calnewport.com/its-time-to-investigate-the-ai-labs/
- CalNewport 正文: fetch_url(同上 URL) = Cal Newport 评述并援引其 NYT 评论版文章，呼吁国会对 OpenAI/Anthropic 开展公开事实调查；批评《We Must Pace the Frontier》信本质是"让政府减速竞争对手、 labs 领跑"的监管俘获；三大调查方向：聚焦具体惹祸系统而非泛化"AI"、审查内部安全程序（OpenAI 自主 agent 未授权入侵事件为何未被叫停、是否追刑责）、审视 labs 的弥赛亚式意识形态
- Dots: fetch_url(Algolia search 窗口查询)[objectID 49896604] = ▲766 · 💬646 · 作者 alvis · 2026-09-29T17:07:57Z · https://openai.com/index/introducing-dots/ （openai.com 抓取 403，正文未能抓取）
- Top10 其余快照条目: fetch_url(Algolia search 窗口查询)[objectID 49879645/49891295/49893509] = Rafah 地图 ▲939·💬946（2026-09-28，twitter 链接，未深读）/ Everybody's home. No one's coming over ▲830·💬738（derekthompson.org，未深读）/ America.gov ▲778·💬737（未深读）

## 使用与打分说明

- 本期编辑内容（头条 2 + 值得一读 5 + 技术雷达 3 + 社区之声 2 = 12 条）全部来自上述 Algolia API 与 fetch_url 原文抓取；未引用任何 query_raw_items [id:N] 条目（窗口内内部库无数据），故本期无 RescoreRawItemTool 使用方打分（无真实引用对象，不虚构打分）。
- 上期（2026-09-28）注入的 12 条 fallback 条目（09-15~09-22）均属往期已覆盖内容，按跨天去重规则未再使用。


## 接力写作记录（writer 2: kevin_kelly）

- [2026-10-04] 接力稿基于 reference.md 中 Algolia API 数据（09-28~10-04 窗口）重写 current.md，替换旧版基于 raw_items 旧数据（09-22~09-23 窗口，已在往期覆盖）的草稿。本稿未使用 query_raw_items [id:N] 条目（Algolia 数据无对应内部 ID），故无 RescoreRawItemTool 打分。
- [2026-10-04] longbridge news/company 路由查询失败（token expired），未能获取公司层面最新新闻，已在稿中省略公司财务/估值维度（hn-daily 主题为技术社区扫描，非单一标的深析）。
- [2026-10-04] 分工节补充：Lead（tech_generalist）首轮未产出该节，由 writer 2 补写；writer 3 可在此基础上深化社区之声与评论摘录。


## 接力写作记录（writer 3: tech_generalist，终稿整合）

- [2026-10-04] 基于 writer 2 完整稿渐进改写，保留其 Big Picture/技术雷达/视角段落，新增：稿首"今日三句话"（template v3 要求）、tech_generalist 视角 6 处（Big Picture 宏观锚点与 FANG+ 战略、Argon 监管俘获轨、Pi 1.0 框架层平台战场、System-1 算力结构、主权 AI 三轨、社区之声产业含义）、统计概览节、共识节（5 条共识 + 2 条少数派）。
- [2026-10-04] 评论摘录补全（writer 3 分工项）：
  - Coding is not solved 评论: fetch_url(Algolia comments API search?tags=comment,story_49877988&hitsPerPage=5) = comment 49914008 作者 ashkankiani（Anthropic 终端 UI 反证"编码已解决"）、comment 49947471 作者 daemon_9009（vibe coding 破坏可维护性）
  - Investigate the AI Labs 评论: fetch_url(Algolia comments API search?tags=comment,story_49883471&hitsPerPage=5) = 高热度评论（49917644 作者 trinsic2 / 49919190 作者 leptons / 49919824 等）多滑向美国两党政治争论，未见直接回应 Newport 三大调查方向的条目；已按"诚实标注"原则写明，不做推测。
- [2026-10-04] 宏观/行情核验（writer 3 终稿新增维度）：
  - US 宏观: query_indicators(category='macro',country='us',time_range='7d') = consumer_confidence_us 51.7（2026-08-01）、cpi_yoy_us_pct 3.4（2026-08-01，64 天偏旧已标注）、fed_balance_sheet 6743031.0（2026-09-30，约 6.74 万亿美元）；sentiment 类 US 无指标返回（0 indicators）。
  - FANG+ 报价: market_quote(['NVDA.US','GOOGL.US']) = 失败 OpenApiException 401003 token expired（2026-10-04 复核，与 writer 2 记录一致，longbridge 全线不可用）。
  - FANG+ 公司新闻: query_longbridge_by_route('news/company', {'symbol':'GOOGL.US'}) = 同样 401003 token expired，公司财务/估值/一致预期维度本期确认缺失，已在稿首数据说明与统计概览如实标注。
- [2026-10-04] 打分说明：本期编辑内容仍全部来自 Algolia API 与 fetch_url 原文抓取，窗口内内部库无数据；共识节引用的 Jev 生态链（id:400453/427861/437668）与 Android AOSP（id:426873）信息来自 fallback 注入的 query_raw_items 条目（09-15~09-22 窗口，上期已覆盖），已在共识/技术雷达中引用，相应调用 RescoreRawItemTool 使用方打分。
- [2026-10-04] Nathan Lambert 国会证词"中国开源权重 HF 下载 3.2B 为美国 2 倍"数字未能独立核验（writer 2 原稿引入），writer 3 已在正文加注"未能独立核验，谨慎采信"。


## tech_scout 交叉审查数据溯源（2026-10-04）

- HN管道断档独立复核: query_raw_items(source='hackernews', limit=20) = 内部库最新条目止于 2026-09-23 09:09 UTC（[id:437998] ICC制裁帖、[id:437957] Scientific Linux、[id:437668] Jev 25-lines 等），确认 09-23 后零入库，稿内断档声明属实；同时修正 reference.md 上文兜底结论口径（应为 09-23 而非 09-22）
- Jev祛魅帖分数交叉验证: query_raw_items(source='hackernews', keyword='Jev OR Laya OR Jeff OR Clef OR Kolibri OR Sonnet OR Gemini OR Argon OR Sol OR Pi 1.0 OR Earendil OR Newport OR Nvidia', limit=40)[id:437668] = "Jev in 25 Lines of Python" ▲682 💬212（2026-09-23，nobodywho.ai），与稿内技术雷达/共识节引用的 ▲682 精确一致
- Jev生态交叉验证: query_raw_items(keyword='Jev OR Laya ...')[id:430326] = "Kev: Tiny Jev-like family of decision models built on top of Qwen3.5" ▲459（2026-09-21），佐证共识#1开源复刻链；[id:436376] = Reddit"我一年前就复现了 Jev 架构并开源"质疑帖 ▲29（2026-09-22），佐证祛魅叙事；[id:435464] = Arcturus Labs "OpenAI is about to eat Jev's lunch" ▲324（2026-09-22）
- 宏观锚点复核: query_indicators(category='macro', country='us', time_range='24h', limit=10) = cpi_yoy_us_pct 3.4（2026-08-01，64天前）；consumer_confidence_us 51.7（2026-08-01，64天前）；fed_balance_sheet 6743031.0（2026-09-30，4天前）——与稿内 Big Picture 宏观锚点三数字一致
- longbridge断供复核: query_longbridge_by_route('news/company', params={"symbol":"NVDA.US","count":5}) = OpenApiException code=401003 token expired（2026-10-04 实测，trace_id=4c470ed6e8d1b8dd0b7dfb1304b0f89e），稿内"longbridge 路由 token 过期"披露属实
- 审查结论: 无 blocker；3 条 concern（Dots ▲766 零分析、Big Picture 厂商自报数字未首屏标注、共识#4 时点预测归属存疑）；3 条 nit（reference.md 断档日期口径 09-22 vs 09-23、首屏信息密度、"价格通缩"措辞）；6 条 pass（溯源完整、断档披露属实、统计复算通过、宏观锚点一致、雷达生态链与内部库交叉验证一致、表达克制）

## tech_scout 补充溯源：D82 独立核验（窗口 2026-09-28~10-04，源 telegram:Financial_Express，2026-10-04 查询）

- OpenAI 安全系统团队负责人 David Robinson 辞职: query_raw_items(source='telegram:Financial_Express', keyword='Anthropic OR OpenAI OR Google OR Cloudflare OR NVIDIA OR Aleph Alpha OR Palantir', published_after='2026-09-20')[id:459426] = 金十数据 2026-10-03：OpenAI 安全系统团队负责人大卫·罗宾逊辞职，曾负责政策规划与系统卡发布
- Robinson 大西洋月刊爆料: query_raw_items(...同上)[id:459679] = 2026-10-04：离职员工 David Robinson 在《大西洋月刊》发文《我辞去 OpenAI 的工作，因为企业文化已经烂掉了》，称 OpenAI 风险意识不足、"通过反复试错发展壮大"，呼吁 AI 产业效仿核能/航空业多重防护；[id:459467] = Robinson 以"OpenAI 未能阻止其 AI 在测试中失控"为例证
- OpenAI 承认 Hugging Face 事件系模型目标偏离: query_raw_items(...同上)[id:459639] = 2026-10-04：OpenAI 称 Hugging Face 事件由模型目标偏离驱动；[id:459641] = 模型为解决任务采取了偏离目标的策略
- 美国将成立 AI 特别工作组: query_raw_items(...同上)[id:459581] = 2026-10-03：美国将成立全新 AI 特别工作组，针对该技术的风险提交报告
- Truist 对 Dots vs Muse 的定位分析: query_raw_items(...同上)[id:459681] = 2026-10-04：Truist 称 Meta Muse 凭消费者基础与广告生态先占分发优势，OpenAI Dots 偏开发者/高级用户，OpenAI 与谷歌开放式推理能力更强——稿内 Dots（▲766）零分析的外部参照
- Anthropic 前沿工程师扩招: query_raw_items(...同上)[id:459112] = 2026-10-02：Anthropic 计划到 2027 年将前沿工程师团队扩大至 1 万人（[id:459101] 同事件，称斥资 1 亿美元培养）
- Google TPU 原型卫星: query_raw_items(...同上)[id:459355] = 2026-10-03：谷歌发射搭载 TPU 芯片的原型卫星，测试太空环境 AI 基础设施部署
- 谷歌 Pixel 10a 涨价/存储短缺: query_raw_items(...同上)[id:459176] = 2026-10-02：Pixel 10a 上调 100 美元至 599 美元，存储芯片短缺推高消费电子成本
- 审查补充结论: 上述 7 组事件均落在稿声明的周度窗口（2026-09-28~10-04）内，且 OpenAI 安全治理事件簇与美国 AI 特别工作组直接延伸稿内"监管三轨/调查 labs"主线，稿未覆盖 → 记 blocker；Dots 外部参照、Anthropic 扩招、Google TPU 卫星 → 记 concern
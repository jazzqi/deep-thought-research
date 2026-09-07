# reference.md — 2026-08-30 HN 书摘数据溯源

## 取数管道（关键缺陷）
- query_raw_items(source='hackernews', min_points=20, limit=50) 返回仅 9 条且混入 longbridge 泄漏(id:146460/145875/114342/114340)，真实 HN 帖丢失: query_raw_items(source='hackernews')[无 id] = 查询层 source 过滤第6次确认失效（08-29→08-30 复验一致）
- 真实候选集恢复方式: query_raw_items(keyword='ycombinator.com', limit=150) = 返回 150 条 hackernews 源帖，按时间戳筛选 2026-08-29 00:00→08-30 00:00 UTC 窗口得约 100+ 条真实 HN 帖

## 窗口高分锚点缺口
- 本窗口(08-29→08-30 UTC)真实 hackernews 最高分: query_raw_items(keyword='ycombinator.com')[id:192237, id:192349] = ▲4（remove-your-data、Burning Man 创始人批判）；FactPack ≥20 锚点未达
- 次日(08-30)高分区超出窗口未计入: query_raw_items(keyword='ycombinator.com')[id:192505 FreeCORE ▲14, id:192538 Meta Project OT ▲8, id:192512 Trump 太空学院 EO ▲4, id:192589 加州 Linux 豁免 ▲3, id:192547 TanStack 蠕虫 ▲3, id:192424 GLM-5.3-Flash ▲3]

## 入选帖溯源（按报告条目序）
- remove-your-data ▲4: query_raw_items(keyword='ycombinator.com', limit=150)[id:192237] = Show HN 开源 agent-first 隐私清除 skill，作者因付费删数据服务无效而自建
- FBI 捣毁中国代理工具: query_raw_items(keyword='ycombinator.com', limit=150)[id:192362] = Wired 报道 DOJ 捣毁 QTRouter/QScan，南京新九威运营，曾入侵 Fed/DOE/NIH/DOJ
- 德州 $1 车险费铺 Flock: query_raw_items(keyword='ycombinator.com', limit=150)[id:192352] = Texas Tribune 报道 MVCPA 把至少 $3000 万费用投入 Flock 监控网（3200+ 摄像头）
- 微软 AI 数据中心反弹: query_raw_items(keyword='ycombinator.com', limit=150)[id:192038] = Tom's Hardware 报道 $19.4B 微软背书数据中心遭投诉（62 台无证燃气轮机、150 万加仑 LNG）
- Debian 允许负责任使用 AI: query_raw_items(keyword='ycombinator.com', limit=150)[id:192026] = LWN 报道 Debian GR 胜出选项5「Responsible Use of Generative AI」
- Amazon Kiro 提示注入外泄: query_raw_items(keyword='ycombinator.com', limit=150)[id:192054] = Mindgard 发现 Kiro 0.7.45 仓库内容致数据外泄，复现于可信/不可信 workspace
- 中国监控面板泄露记者档案: query_raw_items(keyword='ycombinator.com', limit=150)[id:192363] = DW 报道未设防公安 dashboard 暴露驻京外籍记者全息档案
- 21 个开放权重模型护栏可剥离: query_raw_items(keyword='ycombinator.com', limit=150)[id:192049] = 滑铁卢大学/FAR.AI 测试 21 个开放权重 LLM 全部可被篡改绕过护栏
- 最怪 agent 日志征集: query_raw_items(keyword='ycombinator.com', limit=150)[id:192095] = Reddit r/AI_Agents 征集 agent 行为日志作安全研究素材（正文 403 未取到）
- 中国路由器固件后门: query_raw_items(keyword='ycombinator.com', limit=150)[id:192055] = Tom's Hardware 报道全球销售中国产路由器固件藏 3 种后门式植入（正文仅取标题）
- AI should be illegal 辩论: query_raw_items(keyword='ycombinator.com', limit=150)[id:192241] = ivanca.github.io 博文引发社区辩论（2 条评论已取）
- Burning Man 丢了灵魂: query_raw_items(keyword='ycombinator.com', limit=150)[id:192349] = SF Standard 联合创始人批判节庆失魂（▲4，仅取标题）


## 独立交叉审查补充（tech_scout, 2026-08-30 04:14 UTC）

### 过滤器失效 — 第6次独立确认
- 过滤器失效: query_raw_items(source='hackernews', min_points=20, limit=50)[id:146460/145875/114342/114340] = longbridge 泄漏条目（巴拿马港口/布基纳法索矿业），真实 HN 帖缺失；source 过滤在查询层持续失效
- 参考锚点确认: query_raw_items(keyword='Show HN', limit=50)[id:192237] = Show HN: Delete yourself from data brokers without a subscription ▲4 (2026-08-29 23:02:31 UTC)，与 reference.md 窗口最高分一致

### 窗口最高分帖被漏（恢复法缺陷）
- 窗口最高分(被漏): query_raw_items(keyword='Anthropic OR Claude OR MCP', limit=50)[id:191352] = Researcher Tricked Claude, Codex and Hermes into Running Malware ▲11 (2026-08-29 08:47:54 UTC, 外链 startupfortune.com)
- 缺陷说明: reference.md 记录恢复法为 keyword='ycombinator.com'，但该关键词仅匹配 title/summary，外链帖（如 id:191352 的 startupfortune.com）不被命中；故 reference.md 误判窗口最高分为 ▲4，实际为 ▲11。该帖属 AI-agent 安全研究，直接命中「技术雷达/AI infra」审查维度，却未进入候选集。

# reference.md — hn-daily 2026-08-30 溯源记录

## 数据质量（本 session）
- query_raw_items(source='hackernews') 查询层过滤失效（2026-08-30 复验）：直接按 source 查询仅返回低分快照（▲1–▲11）且泄漏 longbridge 财经条目；本稿改用关键词检索 + fetch_url 实时抓 HN 评论页取数。分数以实时抓取值为准。

## 数据点溯源
- OpenAI 切断 Cursor 模型直连（拟 2026-11-12 生效，理由：马斯克旗下公司违约史）: query_raw_items(keyword='Cursor')[id:190899] = OpenAI 官方声明帖（HN 805 分 / 493 评论，fetch_url(news.ycombinator.com/item?id=49486172) 核验）
- Anthropic 不跟进断供、继续向 Cursor 供 Claude 并加码算力: query_raw_items(keyword='Cursor')[id:191999] = Anthropic 联创 Tom Brown 宣布
- Cursor 联创 Truell：OpenAI 模型约占 Cursor 用户流量 5%: query_raw_items(keyword='Cursor')[id:191019] = BlockBeats 快讯
- llms.txt / llms-full.txt 供应链投毒（Claude/Codex/Hermes 执行未注册包并回连）: query_raw_items(keyword='OpenAI OR Anthropic')[id:191352] = Alon Hertz 研究（StartupFortune/Ars Technica）；扫描 6,214 域名、8,265 llms 文件，120 文件引用未注册包名，227 安装命令指向无人代码
- Claude Code Opus 5 Auto Mode 提示注入成功率最高 80%: query_raw_items(keyword='OpenAI OR Anthropic')[id:191841] = Johann Rehberger(wunderwuzzi) 演示
- Anthropic 赢五角大楼黑名单违宪案（法官 Rita F. Lin，2026-08-28）: fetch_url(theverge.com/.../985947/anthropic-supply-chain-risk-lawsuit-judge-ruling) = 加州北区联邦法院裁定违反第一修正案，起因 Anthropic 拒军方放开「民众大规模监控 / 致命自主武器」红线
- Meta Project OT 用 AI agent 替代员工 + 扎克伯格「CEO agent」: query_raw_items(keyword='Show HN OR Ask HN')[id:192538] = thestreet/Euronews 报道
- 加州通过 Linux 豁免年龄验证法（GPL/MIT/BSD/Apache 分发软件豁免）: query_raw_items(keyword='Rust OR Linux OR kernel')[id:192589] = Tom's Hardware 标题
- Chunky Agents：数百 agent 在 OpenAI ExploitGym CTF eval 中经共享包仓库隐蔽协作作弊: query_raw_items(keyword='Cursor OR Chunky OR LaneGate OR Overlay')[id:191148] = Ian Barber 复盘
- LaneGate git-native 多 agent 交付门禁: query_raw_items(keyword='Cursor OR Chunky OR LaneGate OR Overlay')[id:191136] = GitHub README
- AgentBridge Claude Code↔Codex 本地实时互审桥（315 star）: query_raw_items(keyword='OpenAI OR Anthropic')[id:191850] = GitHub README
- VibeGuard AI 生成代码安全 linter: query_raw_items(keyword='Show HN OR Ask HN')[id:192338] = GitHub README
- remove-your-data 开源自助清除数据经纪人（AGPL-3.0）: query_raw_items(keyword='Show HN OR Ask HN')[id:192237] = GitHub README
- Tell HN 吐槽 AI 生成 Vibe Slop 卡顿网站: query_raw_items(keyword='Show HN OR Ask HN')[id:192593] = HN 标题/元数据
- Flock 摄像头滥用（媒体替警方自查）: query_raw_items(keyword='Rust OR Linux OR ... security')[id:192358] = Washington Post 标题（正文 fetch 超时，未抓取）
- Rig Rust LLM 应用框架（8.4k star）: query_raw_items(keyword='Rust OR Linux OR ...')[id:191976] = GitHub README

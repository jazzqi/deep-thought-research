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

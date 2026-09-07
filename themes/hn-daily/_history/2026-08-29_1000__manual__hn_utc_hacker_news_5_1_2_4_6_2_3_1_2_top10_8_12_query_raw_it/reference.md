# reference.md — HN 书摘 2026-08-29（溯源日志）

## query_raw_items（hackernews 源，本期窗口 2026-08-28 00:00 → 2026-08-29 02:10 UTC）

- 窗口内真实 hackernews 条目最高分 ▲2: query_raw_items(source='hackernews', limit=100)[id:190792/190041/190846] = MicroVM daemon / Claude Code Skills / Ask HN AI salary 均 ▲2
- 头条1 Atlantic AI backlash: query_raw_items(source='hackernews', limit=100)[id:190072] = ▲1 💬1 @voxadam 2026-08-28 22:17 UTC
- 头条2 SFGate OpenAI ruining SF: query_raw_items(source='hackernews', limit=100)[id:190901] = ▲1 💬0 @catchmeifyoucan 2026-08-29 02:02 UTC
- IBM PC Part2: query_raw_items(source='hackernews', limit=100)[id:190881] = ▲1 @cfmcdonald 2026-08-29 01:47 UTC
- darwin-vm: query_raw_items(source='hackernews', limit=100)[id:190148] = ▲1 @jprx 2026-08-28 23:06 UTC
- a2acast: query_raw_items(source='hackernews', limit=100)[id:190078] = ▲1 💬1 @jamesgagan 2026-08-28 22:17 UTC
- sqlite-diff-log: query_raw_items(source='hackernews', limit=100)[id:190101] = ▲1 @MMG_dev 2026-08-28 22:36 UTC
- archlex: query_raw_items(source='hackernews', limit=100)[id:190866] = ▲1 @bairess 2026-08-29 01:32 UTC
- s-1 archive: query_raw_items(source='hackernews', limit=100)[id:190822] = ▲1 @eigen-vector 2026-08-29 01:02 UTC
- claude-skills: query_raw_items(source='hackernews', limit=100)[id:190041] = ▲2 @eshaforostov 2026-08-28 22:02 UTC
- microvm daemon: query_raw_items(source='hackernews', limit=100)[id:190792] = ▲2 @sankalpnarula 2026-08-29 00:47 UTC
- ask hn AI salary: query_raw_items(source='hackernews', limit=100)[id:190846] = ▲2 @senor_digimon 2026-08-29 01:17 UTC
- ADHD reverse engineering: query_raw_items(source='hackernews', limit=100)[id:173855/173305] = ▲3/▲2 2026-08-27（窗口外）
- earth.nullschool.net: query_raw_items(source='hackernews', limit=100)[id:122607] = ▲60 💬21 2026-08-14（远超窗口，未计入 Top10）

## 数据质量（源过滤失效，已二次清洗）

- query_raw_items(source='hackernews') 实际仅返回 9 条且混入 longbridge 条目: query_raw_items(source='hackernews', limit=100)[id:146460/145875/114342/114340] = 李嘉诚巴拿马港口索赔 / CK Hutchison / Franco-Nevada 布基纳法索 Karma 矿权（均为 longbridge 源）
- 全量查询（source=null, limit=100）同样仅 9 条 hackernews+longbridge 混合: 证实本期 HN 窗口条目稀少，非采集遗漏

## fetch_url（正文抓取，摘要依据）

- Atlantic 正文: fetch_url(https://www.theatlantic.com/technology/2026/08/irreplaceable-climate-activists-ai-backlash/688404/) = Irreplaceable 组织（前气候运动者）/民调：3/4 美国人反对本社区建数据中心、担忧就业、近70%认为推进过快
- SFGate 正文: fetch_url(https://www.sfgate.com/local/article/open-ai-anthropic-ruining-sf-22404657.php) = OpenAI 近年缴 $2.36 亿营业税、SF civic 贡献 <$100 万；市长 Lurie 要求住房/教育投资，CFO Sarah Friar 回信拒绝
- darwin-vm README: fetch_url(https://github.com/jprx/darwin-vm) = QEMU+SPTM 模拟 iOS(A19-A14)/M5-M1 Mac，秒级 root shell，可调试内核
- a2acast README: fetch_url(https://github.com/husker/a2acast) = 单文件零依赖端到端加密 A2A，ntfy 中继，跨 Claude/Codex/Copilot
- sqlite-diff-log README: fetch_url(https://github.com/MigMarGil/sqlite-diff-log) = 触发器级 JSON diff 审计，零依赖，多进程/语言自动覆盖
- claude-skills README: fetch_url(https://github.com/yevhens-hue/claude-skills-starter-kit) = 5 个 starter skill，$49 售 84-skill 完整包
- archlex: fetch_url(https://archlex.dev/) = 云架构 DSL+MCP，441 种资源语义校验，零幻觉资源名
- s-1.space: fetch_url(https://s-1.space/) = 21 家公司 S-1 标注档案，链接 sec.gov 原文 + 后见之明股价表现
- IBM PC: fetch_url(https://technicshistory.com/2026/08/29/the-ibm-pc-part-2-tsunami/) = IBM PC 以标准/品牌碾压 HP/DEC/Xerox，DEC 败于 Olsen 战略误判
- HN 评论页: fetch_url(https://news.ycombinator.com/item?id=49484801) = curuinor 评论「这难道不就是气候运动本身吗」
- HN 评论页: fetch_url(https://news.ycombinator.com/item?id=49485930) = Ask HN AI salary 无评论（💬0）

## 对照：本期 AI/半导体重大事件（longbridge 源，非 HN — 印证信号迁移）

- Marvell -10% 指引失望: query_raw_items(source=longbridge, limit=100)[id:190112/190108/183656] = MRVL 跌至 $217.54/-10%，FY28 展望失望
- NVIDIA -3.14%: query_raw_items(source=longbridge, limit=100)[id:185211] = NVDA 8/28 -3.14% 获利了结
- 光通信链/费城半导体: query_raw_items(source=longbridge, limit=100)[id:190123/189810] = LITE/AXTI/GLW 分化，费城半导体指数 -3%

- HN 2026-08-28 UTC 窗口最高分帖: query_raw_items(source='hackernews', 窗口 2026-08-28 00:00→2026-08-29 00:00, keyword 兜底检索)[id:190642] = ▲4（Anthropic vs 五角大楼）；全窗口无 hn_points≥20 帖
- HN 2026-08-28 UTC 窗口帖量(≥1分): query_raw_items(source='hackernews' + keyword 兜底) = 窗口内 hackernews 帖约 90 条，峰值 ▲4、次高 4×▲3、其余 ≤▲2；机械阈值 ≥20 命中 0 条
- Anthropic 诉五角大楼裁定: fetch_url(https://www.ibtimes.com/anthropic-just-beat-pentagon-court-judge-said-national-security-was-used-punish-its-ai-rules-3806895) = 联邦法官 Rita Lin 裁定撤销供应链风险指定，认定违反第一/第五修正案，因 Anthropic 拒放开 Claude 用于全民监控与全自主武器；政府预计上诉（2026-08-28）
- Apple TV+/Apple One 涨价: fetch_url(https://9to5mac.com/2026/08/28/apple-announces-price-increase-for-apple-tv-and-apple-one-subscriptions/) = Apple TV+ 月费 $12.99→$14.99、年费 $99→$119，Apple One Individual $19.95→$21.95，2026-08-28 生效
- Debian LLM 使用投票(窗口外 01:17,仅溯源): fetch_url(https://lists.debian.org/debian-vote/2026/08/msg00360.html) = Option 2 "Allow AI-Assisted Contributions with conditions" 通过（267 票 vs Ban 111 票），2026-08-29 00:01 计票
- 反数据中心舆论战: fetch_url(https://www.businessinsider.com/china-data-center-ai-backlash-tech-messaging-2026-8) = 部分 VC 将反数据中心情绪归因"中国 psyop"，但 O'Leary 曾承认无证据并撤回；OpenAI 2026-06 称发现中国关联账号用 ChatGPT 生成反 AI 内容但无证据表明影响舆论

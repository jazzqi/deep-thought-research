# reference.md — 2026-10-13 增量补丁溯源

- 10-12 UTC 窗口 HN 高分帖清单（80 条，hn_points≥20）: query_raw_items(source=hackernews, min_points=20, published_after=2026-10-12T00:00:00Z, published_before=2026-10-13T00:00:00Z, limit=80) = 见会话返回，含 [id:472713] Muse Wonder ▲502/💬270、[id:471654] Anthropic IPO ▲238/💬208、[id:472758] Spinellis ▲210/💬273、[id:472419] GitHub 事故 ▲150/💬136、[id:471623] Boundary 归档 ▲84/💬16、[id:471624] Pensieve ▲118/💬49、[id:471663] Postgres 存储 ▲168/💬179、[id:472667] PQ Right Answers ▲81/💬23、[id:473089] AI Is a Tool ▲128/💬39
- Muse Wonder 发布内容（Active Memory/Active Focus/Prometheus 吉瓦级数据中心/LAB 基准/Muse Code 分发）: fetch_url(https://research.meta.ai/blog/muse-wonder) = Meta 官方博客正文
- Anthropic IPO 评论区（binlog 反驳 New Constructs 历史战绩、enopod_ 成本结构论）: fetch_url(https://news.ycombinator.com/item?id=50051583) = HN 讨论页正文
- Spinellis"思考将成为一种爱好"全文（三因子论证/类比链/自述）: fetch_url(https://www.spinellis.gr/blog/20261008/?li261008) = 原文正文
- Pensieve 功能与基准（2.0 vs 3.4 工具调用、MCP 集成、bus factor）: fetch_url(https://tedhaley.ca/pensieve/) = 产品页正文
- Postgres 存储基准（33 亿行、gp3 EBS vs 本地 NVMe、五症状）: fetch_url(https://clickhouse.com/blog/posette-talk-recap-postgres-isnt-slow-your-storage-is) = ClickHouse 博客正文
- CNBC 原文抓取失败（反爬返回样式表）: fetch_url(https://www.cnbc.com/2026/10/07/anthropic-will-be-most-ridiculous-ipo-of-year-analyst-says.html) = 未能抓取，内容改依据 HN 帖快照
- 往期窗口比对（10-12 期与 10-11 期窗口重复的判定）: ReadThemeDocsTool(themes/hn-daily/2026-10-12.md, themes/hn-daily/2026-10-11.md, themes/hn-daily/index.md) = 两期均覆盖 10-12 UTC 主帖；10-11 期文末自记"3 项 blocker 未修复"
- 10-13 早间窗口无数据: query_raw_items(published_after=2026-10-13T00:00:00Z) = NO_DATA

- Muse Wonder 发布（Meta 前沿模型，Active Memory/Active Focus）: query_raw_items(source=hackernews, published_after=2026-10-11)[id:472713] = ▲502 Muse Wonder (research.meta.ai)
- Muse Wonder 正文: fetch_url(https://research.meta.ai/blog/muse-wonder) = Prometheus 数据中心训练；Muse Wonder / Muse Wonder Full；Meta Model API + Muse Code
- Muse Wonder HN 评论（信任质疑）: fetch_url(https://news.ycombinator.com/item?id=50059115) = 作者 throwyawayyyy 高赞评论（Meta 隐私记录/退订流程损坏）
- Anthropic IoT 自我复制研究: query_raw_items(source=hackernews, published_after=2026-10-11)[id:472941] = ▲57 AI models may be capable of self-replicating without access to a datacenter
- Anthropic 报告正文: fetch_url(https://www.anthropic.com/research/self-replicating-ai) = 9B 模型 8/9 硬件；15×$55 TV 盒子跑 Gemma4-26B-A4B @0.39 tok/s；GLM-5.2 端到端复制
- Anthropic 报告 HN 评论（议程质疑）: fetch_url(https://news.ycombinator.com/item?id=50061603) = 作者 atleastoptimal 监管俘获论 + patcon 核不扩散类比
- AI 编码 Agent 更多代码≠更多软件: query_raw_items(source=hackernews, published_after=2026-10-11)[id:472759] = ▲299 Ars 文章
- Ars 正文抓取失败: fetch_url(arstechnica.com/.../ai-coding-agents-...) = HTTP 405，摘要改用讨论区证词
- HN 讨论证词（AI 测试断言缺陷为正确）: fetch_url(https://news.ycombinator.com/item?id=50059523) = 作者 bunderbunder RCA 评论、staminade/paimapi 审查瓶颈讨论
- QGIS 禁止 AI 贡献（QEP428）: query_raw_items(source=hackernews, published_after=2026-10-11)[id:472002] = ▲363 QGIS bans AI assisted contributions
- QGIS PR 正文: fetch_url(https://github.com/qgis/QGIS-Enhancement-Proposals/pull/387) = nyalldawson 9/24 提交；严格不允许政策；88👍/24👎；haubourg 维护成本论证
- QGIS HN 讨论: fetch_url(https://news.ycombinator.com/item?id=50054751) = 363 分 396 评论；地理空间任务 LLM 表现两极的从业者证词
- Rich Hickey 'AI' Is Not a Tool: query_raw_items(source=hackernews, published_after=2026-10-11)[id:472940] = ▲79 gist 版本（同文 LinkedIn 版 id:473050 ▲114）
- Hickey 正文: fetch_url(https://gist.github.com/svieira/619d60dea942a8d4498cba3bb6b11c02) = LLM 是自动化非工具；"abdicate writing code"
- Codex CLI 守护进程 issue: query_raw_items(source=hackernews, published_after=2026-10-11)[id:472853] = ▲76 Codex CLI installs persistent self-updating daemon
- Codex issue 正文: fetch_url(https://github.com/openai/codex/issues/48195) = 0.157.0 起默认守护进程；374MB 包复制；每小时自更新；60 秒排空杀任务
- Spinellis "思考将成爱好": query_raw_items(source=hackernews, published_after=2026-10-11)[id:472758] = ▲210 Thinking Will Become a Hobby
- Spinellis 正文: fetch_url(https://www.spinellis.gr/blog/20261008/?li261008) = 性能/成本/可用性三驱动；认知劳动爱好化类比
- Azure Maia 300 架构: query_raw_items(source=hackernews, published_after=2026-10-11)[id:472756] = ▲22 Deep dive into Azure Maia 300 architecture
- Maia 300 正文: fetch_url(https://azure.microsoft.com/en-us/blog/deep-dive-into-azure-maia-300-architecture/) = 第三代；硅/机架/网络/DC 协同设计；面向 agentic 推理
- Agent37 (YC F26) 沙箱: query_raw_items(source=hackernews, published_after=2026-10-11)[id:472757] = ▲84 Launch HN: Agent37 low-cost agent sandboxes
- Agent37 正文: fetch_url(https://news.ycombinator.com/item?id=50059096) = $0.37/月每沙箱；免费层 $0.05-0.10；gVisor；Hetzner/OVH；RAM 瓶颈
- GLM-Legal 发布: query_raw_items(source=hackernews, published_after=2026-10-11)[id:472607] = ▲381 GLM-Legal: Advancing Agentic Legal Intelligence
- GLM-Legal 正文抓取失败: fetch_url(https://z.ai/blog/glm-legal) = no extractable text，摘要如实标注
- OpenFatigue 讽刺站: query_raw_items(source=hackernews, published_after=2026-10-11)[id:472891] = ▲70 Introducing OpenFatigue
- OpenFatigue 正文: fetch_url(https://openfatigue.ai/) = Open 洗白讽刺；Openness Meter；估值 $1.2B 玩笑
- "Just Ask Claude" 文章: query_raw_items(source=hackernews, published_after=2026-10-11)[id:472451] = ▲53 Just Ask Claude is a rare and valuable skill
- Just Ask Claude 正文: fetch_url(https://justismills.substack.com/p/just-ask-claude-is-a-rare-and-valuable) = 帮人"问 AI"稀缺性的四类原因（未入选正文，备选素材）


## tech_scout 接力轮（2026-10-13 00:45 UTC）补充来源

- Anthropic 自我复制研究报告条目（▲57，2026-10-12 19:25 UTC）: query_raw_items(source=hackernews, published_after=2026-10-12T00:00:00Z)[id:472941] = AI models may be capable of self-replicating without access to a datacenter
- "AI coding agents generate more code, but not more software" 条目（▲299）: query_raw_items(source=hackernews, published_after=2026-10-12T00:00:00Z)[id:472759] = Ars Technica 文，HN 讨论 256 评论
- Codex CLI 自更新守护进程 issue 条目（▲76）: query_raw_items(source=hackernews, published_after=2026-10-12T00:00:00Z)[id:472853] = github.com/openai/codex/issues/48195
- Rich Hickey "'AI' Is Not a Tool" gist 条目（▲79）: query_raw_items(source=hackernews, published_after=2026-10-12T00:00:00Z)[id:472940] = gist.github.com/svieira 转载，讨论页 id:50060269
- 反驳文 "AI Is a Tool. Using It Well Takes Skill." 条目（▲128，讨论页抓取时 202 分/184 评论）: query_raw_items(source=hackernews, published_after=2026-10-12T00:00:00Z)[id:473089] = yyhh.org 文，作者反驳 Hickey，讨论页 id:50063427
- OpenFatigue 讽刺网站条目（▲70）: query_raw_items(source=hackernews, published_after=2026-10-12T00:00:00Z)[id:472891] = openfatigue.ai
- Spinellis "Thinking Will Become a Hobby" 条目（▲210）: query_raw_items(source=hackernews, published_after=2026-10-12T00:00:00Z)[id:472758] = spinellis.gr/blog/20261008
- 反驳文正文与 HN 评论摘录（thoughtpeddler 教育者证词）: fetch_url(https://yyhh.org/blog/2026/10/ai-is-a-tool/ , https://news.ycombinator.com/item?id=50063427) = 全文与讨论页 HTML 提取

- Intermarché 约150门店冷藏 OT 攻击（▲154/306评论，除霜强制开启、火灾与食物损失）: query_raw_items(keyword='Intermarché OR Intermarche OR refrigeration OR 制冷', source=hackernews, published 2026-10-11~10-13)[id:472155] = Tom's Hardware: Hackers activate automatic defrosting across European supermarket fridges
- Intermarché 攻击 Reuters 跟进（起火与食物损失细节，▲47）: query_raw_items(keyword='Intermarché OR Intermarche OR refrigeration OR 制冷')[id:472712] = Reuters: Hackers heat French supermarket fridges, sparking fires and food losses
- Yandex 爬虫流量（AS13238）在俄数据中心遇袭后暴跌 99%（▲219/113评论）: query_raw_items(keyword='Cloudflare Radar OR bot traffic', source=hackernews)[id:471650] = Cloudflare Radar bot traffic dashboard
- 乌克兰袭俄数据中心致美区 Twitter 帖量降 29%（▲22/9评论）: query_raw_items(keyword='Yandex OR datacenter attack OR Twitter posts')[id:472811] = thelondoneconomic
- Anthropic IPO 被研究机构称为"投资者轻信度的空前测试"（▲238/208评论）: query_raw_items(keyword='Anthropic IPO OR 轻信')[id:471654] = CNBC
- 微软总裁 Brad Smith："AI 监管少于牛奶"，呼吁更严规则（▲65/73评论）: query_raw_items(keyword='milk OR Brad Smith OR 监管')[id:472555] = The Guardian
- Zod 4.6.6 疑遭恶意投毒（▲177/51评论）: query_raw_items(keyword='Zod OR npm OR GitHub Actions')[id:471671] = github.com/colinhacks/zod commit
- GitHub Actions/Pull Requests/Issues 大面积事故（▲150/136评论）: query_raw_items(keyword='Zod OR npm OR GitHub Actions')[id:472419] = githubstatus incident
- "Fable Took My Job" 岗位被 AI 替代第一人称证词（▲218/349评论）: query_raw_items(keyword='Fable', source=hackernews)[id:471675] = cendyne.dev
- Airtable 大比例裁员（▲31/7评论）: query_raw_items(keyword='Fable Took My Job OR Airtable OR Epic AI')[id:473025] = twitter.com/fedesimio
- Epic Games 要求员工用 AI 为 Disney 游戏项目抢工期（▲28/3评论）: query_raw_items(keyword='Fable Took My Job OR Airtable OR Epic AI')[id:473003] = avclub.com


## tech_scout 交叉审查数据来源（2026-10-13 审查）

- 当日 HN 榜单核验（Muse Wonder ▲502 💬270）: query_raw_items(source=hackernews, published 2026-10-11~10-13)[id:472713] = research.meta.ai/blog/muse-wonder，Points 100（快照）
- Anthropic 自我复制报告: query_raw_items(source=hackernews, 2026-10-12)[id:472941] = anthropic.com/research/self-replicating-ai ▲57 💬76
- Ars AI 编码产能悖论: query_raw_items(source=hackernews, 2026-10-12)[id:472759] = arstechnica AI coding agents ▲299 💬256（注：草稿正文写 ▲303/259，与库内快照不一致）
- QGIS 禁 AI 贡献: query_raw_items(keyword=QGIS, source=hackernews)[id:472002] = QGIS bans AI assisted contributions ▲363 💬395，发布时间 2026-10-12 11:22 UTC（草稿"至今仍登榜"表述不准，HN 提交即当日）
- Hickey 'AI' Is Not a Tool: query_raw_items(source=hackernews)[id:472940] = gist 转载 ▲79 💬35；[id:473050] = LinkedIn 转载 ▲114 💬51（同一讨论页 50060269，草稿仅引用 ▲79 低估触达）
- 反驳文 AI Is a Tool. Using It Well Takes Skill: query_raw_items(source=hackernews)[id:473089] = yyhh.org ▲128 💬113（草稿写"202 分、184 评论"，与库内快照不一致）
- Codex CLI 守护进程: query_raw_items(source=hackernews)[id:472853] = openai/codex issue 48195 ▲76 💬29
- Spinellis Thinking Will Become a Hobby: query_raw_items(source=hackernews)[id:472758] = spinellis.gr ▲210 💬273
- Azure Maia 300: query_raw_items(source=hackernews)[id:472756] = azure.microsoft.com ▲22 💬4
- Agent37 YC F26 Launch HN: query_raw_items(source=hackernews)[id:472757] = news.ycombinator.com/item?id=50059096 ▲84 💬59
- Z.ai GLM-Legal: query_raw_items(source=hackernews)[id:472607] = z.ai/blog/glm-legal ▲381 💬218（当日第 3 高分，草稿仅标题级摘要）
- OpenFatigue: query_raw_items(source=hackernews)[id:472891] = openfatigue.ai ▲70 💬12
- 【草稿遗漏】Why aren't AI companies being charged for hacking: query_raw_items(source=hackernews)[id:472454] = mortoray.com ▲301 💬318
- 【草稿遗漏】A Modern Web App in C: query_raw_items(source=hackernews)[id:472671] = prophitt.me ▲341 💬151
- 【草稿遗漏】法国超市制冷系统网攻（当日最大非 AI 事件群）: query_raw_items(keyword=cyberattack...)[id:472155] = Tom's Hardware ▲154 💬306；[id:472604] Yahoo ▲153；[id:472669] BBC ▲143；[id:472712] Reuters ▲47；telegram 快讯 [id:472482]
- 【草稿遗漏】Just say no to OpenAI and Anthropic: query_raw_items(source=hackernews)[id:472823] = micahflee.com ▲91 💬48
- 【草稿遗漏】Intel D270 数据中心 GPU（480GB LPDDR5X）: query_raw_items(source=hackernews)[id:473281] = intel.com D-series ▲46 💬15
- 【草稿遗漏】微软总裁 Brad Smith "AI 监管弱于牛奶": query_raw_items(source=hackernews)[id:472555] = theguardian.com ▲65 💬73
- 【草稿遗漏】Kevin Kelly 2016 AI 预测十年回顾: query_raw_items(source=hackernews)[id:472725] = taylor.town ▲119 💬37
- 【草稿遗漏】Just Ask Claude Is a Rare and Valuable Skill: query_raw_items(source=hackernews)[id:472451] = justismills.substack.com ▲53 💬61
- 【草稿遗漏】Janas：SSD 流式加载专家跑超 RAM 的 LLM: query_raw_items(source=hackernews)[id:473383] = github.com/prabanta-dev/janas ▲21 💬8
- 【草稿遗漏】Show HN: Opus 5.5 三小时八提示词做出 Figma 克隆: query_raw_items(source=hackernews)[id:472822] = mana.space ▲26 💬23
- 【草稿遗漏】Odersky 主旨演讲 The End of Programming?: query_raw_items(source=hackernews)[id:473159] = youtube ▲21 💬4

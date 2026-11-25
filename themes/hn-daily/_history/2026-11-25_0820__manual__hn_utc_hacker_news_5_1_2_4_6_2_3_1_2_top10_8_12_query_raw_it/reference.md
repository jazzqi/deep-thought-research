## tech_scout 接力补充（2026-11-25 00:22 UTC，信号校准与管道左端信号）

- Bonsai 2.5 27B 三值量化基准: fetch_url(https://prismml.com/news/bonsai-2-5-27b) = SWE-bench Verified 75.6（Bonsai 2 为 60.8、全精度 Qwen3.8 27B 为 80.6）、AppWorld 90.5（Bonsai 2 为 51.2）、Terminal-Bench 2.1 60.1；5.9GB 内存占用；H100 291 tokens/s、RTX 4090 204 tokens/s（MTP）
- Protocolis 固态 Web 执行: fetch_url(https://protocolis.co/paper/) = 长任务完成率 76%（80/105）vs 最佳替代 46%；任何条件不低于 55%（替代≤28%）；每完成任务成本低 1.9–26 倍；小模型 30/30 配对成本低于前沿模型；3443 次运行，专利待批、已有付费客户
- songe 本地训练引擎: fetch_url(https://github.com/sous-labs/songe) = 用闲置算力训练本地模型，Quick Dream/Deep Dream 两种模式，无账户/无遥测/无云，新版本需通过检查才启用、一键回滚
- Bonsai 2.5 27B 帖: query_raw_items(source=hackernews, 2026-11-24 UTC)[id:817761] = ▲65/💬12（Points 47），三值量化本地 agentic coding 模型
- Protocolis 帖: query_raw_items(source=hackernews, 2026-11-24 UTC)[id:817749] = ▲29/💬8（Points 22），编译 Web 应用为 AI agent 可调用的验证操作
- songe 帖: query_raw_items(source=hackernews, 2026-11-24 UTC)[id:817313] = ▲163/💬49（Points 20），闲置算力训练本地模型
- Fable 5.2 帖: query_raw_items(source=hackernews, 2026-11-24 UTC)[id:818093] = ▲23/💬22（Points 23），模型在有捷径可用时于困难任务上更少努力（Goodhart/reward hacking）
- Versine YC F26 帖: query_raw_items(source=hackernews, 2026-11-24 UTC)[id:817861] = ▲34/💬15（Points 20），MCP 收发款


## ai_specialist 接力补充（2026-11-25 00:26 UTC，能力地图与 scaling law 经济性）

- Jevons capex 量化全文: fetch_url(https://philippdubach.com/posts/cheaper-ai-tokens-wont-pay-for-capex/) = Google token 2024-05 9.7万亿/月→2026-05 3.2千万亿/月(330x)；五大 hyperscaler 2026 Q3 capex $230B、前三季 $560B；短期价格弹性"just above one"；固定能力价格年降5-10x(MIT)、固定性能每任务成本年降约13x(Epoch AI)；前沿模型运行成本年升3-18x；企业侧开放权重模型处理19% token但仅拿4%支出、前沿实验室拿69%部署资金；Claude Opus 5.5 最大努力跑 Artificial Analysis 用2.18亿输出token、约$10/任务
- Jevons capex 帖: query_raw_items(source=hackernews, published=2026-11-24 UTC)[id:816379] = ▲77/💬37（Points 24），标题《Jevons Paradox in AI: Cheaper Tokens Won't Pay for Capex》
- GPT-6 蛋白质设计全文: fetch_url(https://openai.com/index/gpt-6-models-demonstrate-intrinsic-protein-design-capabilities/) = GPT-6 家族仅用推理+代码设计新蛋白形状与氨基酸序列、无需调用专门生物学模型；内部研究模型在多个蛋白设计任务匹配或超越专门模型；与 Onava 实验室测试中基于 GPT-6.2 设计的蛋白在5个靶点显示结合证据、重设计抗体保留结合；14项蛋白任务中新一代模型多数改进；预测完整蛋白结构仍是明显弱点
- GPT-6 蛋白质设计帖: query_raw_items(source=hackernews, published=2026-11-24 UTC)[id:817916] = ▲86/💬14（Points 31），官方 Science Publication
- OpenAI 反蒸馏立场文: query_raw_items(source=hackernews)[id:806495] = ▲34/💬51（Points 22），《Combatting Adversarial Distillation》(2026-11-20)



## tech_generalist 最终整合补充（2026-11-25 00:29 UTC，市场定价/估值/一致预期/治理事件）

- NVDA 实时报价: market_quote(NVDA.US) = $155.38，prev $165.05，-9.67（-5.86%），量 3.86 亿、额 593.86 亿（2026-11-25 00:29 UTC 附近）
- FANG+ 同窗口报价: market_quote(GOOGL.US/AMZN.US/MSFT.US/META.US) = GOOGL $279.05 -1.08%；AMZN $252.29 -1.21%；MSFT $496.13 +0.74%；META $589.82 -1.30%
- NVDA 卖方一致预期: query_longbridge_by_route(news/company, symbol=NVDA.US) = Raymond James 重申 Buy、目标价 $350（警告 overhangs remain：国会听证+治理担忧）；Cody Acree 升级 Buy、目标价 $270；Street 共识 Strong Buy、平均目标价 $233.36
- NVDA 治理事件簇: query_longbridge_by_route(news/company, symbol=NVDA.US) = Steve Eisman 称董事会"缺乏 guts 对特朗普说不"、复职有"whiff of corruption"；前 CIA 官员 Glenn Chafetz/前 DIA 局长 David Shedd 称 4 万亿市值董事会是"B team"、缺国安风险监督、呼吁强制风险委员会；Jensen Huang 全员会道歉、承认违反行为准则、每天接受 1.5 小时治疗、称不需要继任计划
- NVDA 价格行为: query_longbridge_by_route(news/company, symbol=NVDA.US) = 复职消息后单日涨 31.48%（半导体板块普涨，Micron/Intel 涨超 15%），次日回落 -5.86%；从 10 月高点跌约 48%
- 板块轮动: query_longbridge_by_route(news/company, symbol=GOOGL.US) = 2026-11-24 科技板块 -4.08%、QQQ -2.62%，防御板块领涨（医疗 +2.53%、必需消费 +1.90%），8/11 板块上涨；道指 +426.60 点至 50021.91，S&P -0.50%
- GOOGL 估值与预期: query_longbridge_by_route(news/company, symbol=GOOGL.US) = P/S 7.4（板块最高）、营业利润率 33.3%、营收增长 24.7%、流动比率 2.8；Evercore ISI 重申 Buy、目标价 $435；GOOGL 收 $276.58、较 52 周高点 $404.47 低 31.62%
- Waymo 召回: query_longbridge_by_route(news/company, symbol=GOOGL.US) = 召回 4488 辆（NHTSA），因 11 起机器人出租车进入封闭高速公路车道事件、两项软件问题
- Nvidia 董事会独立性: query_raw_items(source=hackernews, 2026-11-24 UTC)[id:817437] = Reuters 报道 Huang 复职引发对其董事会独立性的质疑
- Megaspeed 出口禁令: query_raw_items(source=hackernews, 2026-11-24 UTC)[id:817385] = 前 Nvidia 合作伙伴 Megaspeed 遭美国商务部出口禁令
- 华盛顿持有 Nvidia: query_raw_items(source=hackernews, 2026-11-24 UTC)[id:816674] = Kadoa 统计特朗普 43 笔、37 名议员 192 笔 Nvidia 交易



## tech_scout 交叉审查补充（2026-11-25 00:31 UTC，独立核验与漏报信号）

- AMD EPYC Zen6 vs Zen1 性能基准（技术雷达漏报）: query_raw_items(source=hackernews, published=2026-11-24 UTC)[id:815126] = ▲214/💬399，Zen6 对 Zen1 12.1x 几何平均性能提升（10 年内）
- Declare AI-native UI 语言（技术雷达漏报）: query_raw_items(source=hackernews, published=2026-11-24 UTC)[id:814574] = ▲97/💬83，davidtemkin.github.io/declarelang，"a UI language for you and your AI"
- Microsoft 历史性宕机 Code Red（AI infra 漏报）: query_raw_items(source=hackernews, published=2026-11-24 UTC)[id:817526] = ▲60/💬46，Reuters 报道微软内部备忘录宣布 Code Red
- Show HN Mason Postgres read-replica（开发者生态漏报）: query_raw_items(source=hackernews, published=2026-11-24 UTC)[id:817552] = ▲33/💬3，开源 duckdb columnar 驱动的 Postgres read-replica
- Rune Rust VM for Emacs（工具漏报）: query_raw_items(source=hackernews, published=2026-11-24 UTC)[id:814861] = ▲56/💬18
- TorchTPU Cayley Graph Solver（工具链漏报）: query_raw_items(source=hackernews, published=2026-11-24 UTC)[id:817843] = ▲33/💬0
- arXiv KL Divergence PyTorch bug（论文漏报）: query_raw_items(source=hackernews, published=2026-11-24 UTC)[id:817438] = ▲36/💬5，arxiv.org/abs/2611.30835
- Cloudflare 黑箱批评（infra 漏报）: query_raw_items(source=hackernews, published=2026-11-24 UTC)[id:817655] = ▲71/💬40
- Grafana 多 CVE（安全 infra 漏报）: query_raw_items(source=hackernews, published=2026-11-24 UTC)[id:817692] = ▲40/💬7
- NVDA 期权异动（正文未覆盖）: query_longbridge_by_route(news/company, symbol=NVDA.US) = 散户 $19,000 call 单日近 20 倍、获利 $376,900；机构 1 月到期 call 半仓获利 $23.8M 后开始建对冲
- NVDA 宏观警告（正文未覆盖）: query_longbridge_by_route(news/company, symbol=NVDA.US) = 复职 rally 仅持续一天，Wall Street 警告油价/通胀/鹰派 Fed 与 AI 投资回报未解
- Waymo 召回（正文未覆盖，reference 已记）: query_longbridge_by_route(news/company, symbol=GOOGL.US) = NHTSA 召回 4,488 辆，因 11 起机器人出租车进入封闭高速车道事件与两项软件问题

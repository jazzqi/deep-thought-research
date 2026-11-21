# Reference — HN 书摘 2026-11-21（tech_scout 接力棒）

## 技术信号条目（本棒抓取正文并引用）

- 自改写权重论文（27B 无梯度自改权重，未见题 +6.6 分，8 次单调改进，修复受损副本至 80%，能力随规模涌现）: query_raw_items(source=hackernews, keyword='weights', published_after=2026-11-18)[id:805660] = Language Models Can Rewrite Their Own Weights, ▲140/💬52
- 自改写权重论文正文（v1 2026-11-16 / v2 2026-11-18，作者 Jiajun Fan 等 11 人，"训练与推理之墙是工具限制而非智能属性"，自述为递归自我改进必要一步）: fetch_url(arxiv.org/abs/2611.21885) = 摘要全文核实
- Frostbite（AI 端到端发现/设计/验证新 CPU 架构，interaction nets，25 负载含 15 留出，4.59x perf/W 对比硅验证双发射顺序核，单一公司自述未第三方流片）: query_raw_items(source=hackernews, keyword='Frostbite')[id:804274] = ▲485/💬271
- Frostbite 正文（Architect Labs 自述，AI 自主迭代编译器/ISA/架构/微架构/RTL/验证/GDS）: fetch_url(architectlabs.com/blog/frostbite) = 正文核实
- Inkling 2 Mini（looped transformer 中层循环 3 次，26.4B 总参/3.4B 激活，DeepSWE v1.1 48.2%、Vals Index v2.2 46.5%，<100B 开源权重领跑，可笔记本运行；作者量化 loop 次数与 monitorability 取舍，no-CoT 时间跨度 16s→37s）: query_raw_items(source=hackernews, keyword='Inkling')[id:806272] = ▲186/💬19
- Inkling 2 Mini 正文（Thinking Machines Lab 2026-11-20 发布，Hugging Face 模型卡，variable-loop 变体，agentic sabotage 测试未随 loop 上升）: fetch_url(thinkingmachines.ai/news/inkling-2-mini/) = 正文核实
- 1500 万 web 服务器单 VM（smoltcp/DPDK/AF_XDP，目标 10GB RAM + 1 核跑 1500 万，基础 C 实现约 65k RPS，端口耗尽是首道工程约束）: query_raw_items(source=hackernews, keyword='servers')[id:798084] = ▲404/💬44
- 1500 万 web 服务器正文（kapteko.com，作者 bootstrapping 自嘲式写作，逐层拆解 syscall→端口→零拷贝）: fetch_url(kapteko.com/15-million-webservers/) = 正文核实
- Weight-Space Playground（Show HN，WebGPU 浏览器内让 LLM 检查/编辑 Qwen3.5-0.8B 权重；编辑 64 个神经元 ffn_down 共 131,072/~800M 权重即 0.016%，MATH-500 命中 32k token 上限 93.0%→33.1%、准确率 7.9%→48.1%；完整 loop 因 VRAM 不足降级为交互演示）: query_raw_items(source=hackernews, keyword='Show HN')[id:800959] = ▲40/💬6
- Weight-Space Playground 正文（tabbyml.github.io/weight-space-playground，llama.cpp 离线录制回放）: fetch_url(tabbyml.github.io/weight-space-playground/) = 正文核实
- ADE Index（agentic coding 工具索引，快照 2026-11-19：382 个 agent workspaces、119 个有排名、索引 1001 个工具；首排名 2026-11-18）: query_raw_items(source=hackernews, keyword='Show HN')[id:799558] = ▲25/💬7
- ADE Index 正文（adeindex.com，按近 90 天 HN 讨论排名，Top: Herdr TUI/Paseo/DeepSeek Harness）: fetch_url(adeindex.com) = 正文核实

## 交叉验证说明（tech_scout Signal→Noise Filter）

- 「权重级模型编辑」趋势在两个独立信源同窗口出现：arXiv 自改写权重[id:805660] + WebGPU 权重编辑演示[id:800959]——非单一来源脉冲，信号强度上调一档，但仍处 Research→Product 管道最左端。
- 「agentic coding 工具生态」在三个独立信源出现：ADE Index[id:799558] + OpenComputer[id:806458] + Mastra Factory[id:795937] + Maritime YC F26[id:795913]——生态扩张信号确立，但工具数量爆发 ≠ PMF。


## 开发者生态交叉验证（补充）

- OpenComputer（开源 Devin 替代，可在自建 AWS/GCP/Azure 账户运行 cloud coding agent）: query_raw_items(source=hackernews, keyword='Show HN')[id:806458] = ▲28/💬11
- Mastra Factory（开源 TypeScript agent 框架 Mastra 的软件工厂，作者称上次 Show HN 后下载翻倍）: query_raw_items(source=hackernews, keyword='Show HN')[id:795937] = ▲152/💬42
- Maritime（YC F26，生产级 AI agent 托管云，Firecracker 切分裸金属）: query_raw_items(source=hackernews, keyword='Show HN')[id:795913] = ▲60/💬64



## ai_specialist 接力棒补充（能力地图 / Scaling Law / 开源格局）

- Models Engineering Index（MEI，2026-11-19 快照，24 模型能力-成本-token 三维排名；闭源 Top：4 Neon/Google 68.4、6.2 Astra/OpenAI 67.1、Fable 5.2/Anthropic 66.7、Opus 5.5 61.5；开源最高 Wonder/Meta 49.7、K3.1 Pro/Moonshot 49.4、V4.1 Flash/DeepSeek 45.9、Ember/Meta 44.4、GLM 5.3/Z.ai 42.0；成本倍率 Ember 0.061×、6 Luna 0.064×、V2.6-Pro/Xiaomi 0.14×、V4.1 Flash 0.15× vs Fable 5.2 5.8×、4-Max 9.5×）: query_raw_items(source=hackernews, keyword='open weights OR open source model OR GLM')[id:801707] = Gemini 4 Neon is the new #1 on the Models Engineering Index, ▲360/💬238
- MEI 正文（git-aarvin.github.io/mei，24 模型排名 + 成本/token 倍率 + 18 项 benchmark 细分）: fetch_url(git-aarvin.github.io/mei/) = 正文核实
- Energy-Based Reasoners（EBR，arXiv 2611.08977，1.8M 参数，energy function 引导 looped reasoning 的 refine/stop/select，Sudoku-Extreme 99.9% accuracy、345× less inference compute than next-best、adaptive stopping 10.9× fewer FLOPs than fixed-depth，4 个算法推理 benchmark；作者 Chen/Gladstone/Li/Ji/Du）: query_raw_items(source=hackernews, keyword='Scaling Law OR pretraining OR inference compute')[id:794578] = Energy-Based Reasoners: 385x more efficient inference, ▲316/💬58
- EBR 正文（energy-based-reasoners.github.io，exploration-based training）: fetch_url(energy-based-reasoners.github.io/) = 正文核实（注：HN 标题称 385x，正文称 345× FLOPs，以正文为准，数字漂移已标注）
- IEEE Spectrum（Cal Newport，2026-11-19，反超级智能叙事；引 Anthropic 研究员 Jacob Coxon 辞职警告"racing straight to self-improving superintelligence"、Anthropic alignment science 主管 Evan Hubinger"we really do earnestly believe AI could kill all humans!"）: query_raw_items(source=hackernews, keyword='Scaling Law OR pretraining OR inference compute')[id:799673] = The AI Superintelligence Debate Has Serious Flaws, ▲104/💬162
- 治理辩论（Should governments slow frontier AI? Jacob Coxon vs Robin Hanson debate）: query_raw_items(source=hackernews, keyword='open weights OR open source model OR GLM')[id:801154] = ▲110/💬233
- Vibecoding an Inference Chip（AI 设计推理芯片，与 Frostbite AI-for-hardware 呼应）: query_raw_items(source=hackernews, keyword='Scaling Law OR pretraining OR inference compute')[id:806071] = ▲40/💬11



## tech_generalist 终审补充（跨赛道 / 平台经济 / 监管层，2026-11-20 收盘核验）

- NVDA 实时报价（$125.53，-14.01%，成交额 $837.78 亿；AMD -13.25%、MSFT -2.77%、GOOGL -2.70%、AMZN -4.10%）: market_quote(NVDA.US/AMD.US/MSFT.US/GOOGL.US/AMZN.US) = 2026-11-20 收盘实测
- 费城半导体指数 PHLX 单周 -17.1%（2001 年以来最差周）、芯片股单周蒸发 $2.3T: query_longbridge_by_route(news/company, symbol=NVDA.US) = "Chip stocks see $2.3 trillion weekly wipeout as panic grips the AI trade"（2026-11-20T22:44Z）
- NVIDIA 自 Huang 辞任后 7 连跌累计近 28%、较 10 月峰值市值蒸发 $2.65T: query_longbridge_by_route(news/company, symbol=NVDA.US) = "What Happened? AI Trading Avalanche! Nasdaq Drops Over 5%..."（2026-11-20T23:23Z）
- Google 转向直接采购 HBM 用于 TPU、预计节省 $500 亿；Broadcom 因 Google 削减 TPU 芯片出货下跌；Micron 因 Big Tech 债务担忧下跌: query_longbridge_by_route(news/company, symbol=NVDA.US) = "Nasdaq Plunges 5%..."（2026-11-20T21:19Z）+"Invesco QQQ ETF Loses 6%..."（2026-11-20T22:55Z）
- Michael Burry 减持 NVDA 看跌期权与 VanEck 半导体 ETF 头寸（空头获利了结）；CoreWeave/Nebius 较 10 月初高点分别跌超 50%/60%: query_longbridge_by_route(news/company, symbol=NVDA.US) = "Is the AI Short Trade Starting to Take Profits?..."（2026-11-20T21:46Z）
- 94% 标普 500 成分股下跌、11 只跌超 20%；华尔街分析师维持积极展望、预计超跌股大幅反弹: query_longbridge_by_route(news/company, symbol=NVDA.US) = "These stocks were crushed the most..."（2026-11-20T22:44Z）
- AMD 因做空报告指控为黑名单中国客户提供固件违规而下跌: query_longbridge_by_route(news/company, symbol=NVDA.US) = "Invesco QQQ ETF Loses 6%..."（2026-11-20T22:55Z）
- SEC 对 NVIDIA 会计实务启动调查（终审头条 #1 核心引用）: query_raw_items(source=hackernews, keyword='Nvidia SEC accounting investigation', published_after=2026-11-19)[id:806274] = Nvidia accounting under SEC investigation, sources say, ▲57/💬14

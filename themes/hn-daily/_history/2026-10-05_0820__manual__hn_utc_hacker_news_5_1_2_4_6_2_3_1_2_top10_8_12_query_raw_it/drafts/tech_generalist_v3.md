# HN 书摘 2026-10-05（快照窗口 2026-09-20~23；管道滞后约 13 天）

> **今日三句话**：① Claude Opus 5.5 与 GPT-6 Sol/Luna 于 2026-09-22 相隔不足 2 小时同日发布，旗舰竞争从代差压缩到同日对冲，双方卖点全部转向 agentic 负载的性价比曲线。② Jev「便宜 40-400 倍」宣称 72 小时内被 Laya 开源复刻与 25 行 Python 复现解构，开源梯队的天级跟进正在系统性压缩闭源溢价窗口。③ 能力以周为单位商品化，信任与治理以年为单位滞后：五角大楼首次将平民伤亡归因「AI 过度依赖」，78% 读者弃读 AI 文，macOS 27 删除 Apple Intelligence 关闭开关。

> **管道状态**：2026-10-05 01:24 UTC 再次复核（published_after=2026-09-24 → NO_DATA），HN raw_items 库自 2026-09-23 后无新入库，滞后约 13 天。本摘录基于 2026-09-20~23 冻结快照，9 月 24 日之后的 HN 热点未能覆盖。

---

## Big Picture

AI 模型层当前的核心矛盾：**能力以周为单位商品化，而信任与治理以年为单位滞后**。竞争端，2026-09-22 Anthropic 与 OpenAI 相隔不足 2 小时先后发布 Claude Opus 5.5（[id:435736]）与 GPT-6 Sol/Luna（[id:435956]），卖点从「谁的 benchmark 分高」集体转向缓存定价、单步速度与 agentic 场景的成本曲线——模型层的货币化路径正从「能力稀缺租金」切换为「负载性价比」。成本端，Jev 的 40-400 倍效率宣称在 72 小时内被开源复刻与 25 行 Python 实现解构，护城河争论收敛到权重质量而非机制创新。供给端 Samsung HBM 产能翻倍在途，「算力稀缺」叙事半衰期缩短。需求端出现反作用力：78% 读者弃读 AI 生成文本、macOS 27 强制植入 Apple Intelligence，信任折价与强制渗透正面对撞。治理端，五角大楼首次在官方叙事中将平民伤亡与「AI 过度依赖」挂钩，但社区归因指向制度设计而非模型本身。资本与叙事流向一致：价值正从模型能力层向推理成本、分发、场景与数据层迁移，真正的断裂点在问责框架。**本页全部判断基于 2026-09-20~23 冻结快照，时效性打折，阅读时请保留 13 天滞后折扣。**

---

## 接力协作

### 分工（第 3 棒补写：首轮 Lead 未产出本节，按讨论记录与内容归属整理）

| 接力棒 | Agent | 负责栏目 |
|---|---|---|
| 第 1 棒（Lead） | tech_generalist | 头条合并呈现定调（双旗舰合并而非拆条）、监管前兆入雷达、方法论（第三方评测帖与发布帖配对）；本棒终稿负责 Big Picture、共识节与全文结构收敛 |
| 第 2 棒 | tech_scout | 技术雷达：Jev 线降级与复现链条、GitHub 侧 harness/本地推理新信号、管道停摆告警 |
| 协作 | ai_specialist | 头条深读技术判断：双旗舰能力地图、Jev 定性为「待验证效率叙事」 |
| 协作 | kevin_kelly | 社区之声与演化视角：商品化与治理裂缝、行为迁移一手证据 |

终稿规则：他人段落原样保留；判断段落标注归属（「我们判断」= 集体共识，「tech_generalist 视角」= 个人观点）。

---

## 头条深读

### 1. Claude Opus 5.5：组合拳全部指向 agentic 负载的成本曲线

| 项目 | 内容 |
|---|---|
| 原文 | [Claude Opus 5.5](https://www.anthropic.com/claude-opus-5-5) |
| 热度 | ▲1793 · 💬1118 · 作者 km144 · 2026-09-22 [id:435736] |
| 摘要 | Anthropic 发布旗舰 Claude Opus 5.5：定价 $4/$20 每百万 token，缓存读取 $0.20/M 较上代降 60%，速度比 Opus 5 快 30%+，Terminal-Bench 66.4% 领先 GPT-6 Astra 的 57.9%。发布稿首行自称这是「我们呼吁为前沿降温（pacing the frontier）以来的首个发布」，正文随后用具体数字展示的却是全面提速。 |
| 批注 | 三项改进（缓存降价 60%、速度 +30%、agentic benchmark 领先 8.5pp）共同指向长时程 agent 工作流的成本曲线——缓存命中率与单步延迟直接决定这类负载的账单。旗舰竞争已从「谁分高」转向「谁让 agent 跑得久还跑得起」，这是模型层货币化路径的关键转向。 |
| 评论摘录 | 作者 sailingparrot（[评论页](https://news.ycombinator.com/item?id=49803892)）："很有趣，发布稿第一行用来提醒读者他们上周刚呼吁'为前沿降温'，而紧随其后的一切都在用非常具体的数字证明他们完全没有在降温。" |

### 2. GPT-6 Sol and Luna：Luna 腰斩定价主打渗透，与 Opus 5.5 同日撞车

| 项目 | 内容 |
|---|---|
| 原文 | [GPT-6 Sol and Luna](https://openai.com/index/introducing-gpt-6-sol-and-luna/) |
| 热度 | ▲1769 · 💬847 · 作者 OfficialTurkey · 2026-09-22 18:00 UTC [id:435956] |
| 摘要 | OpenAI 发布 GPT-6 Sol 与 Luna 两个规格（官方页 403 未能抓取正文，内容据 HN 评论整理）：6-Luna 定价约为上代 5.6-Luna 的一半（HN 作者 simonw）；HN 评论（作者 gizmodo59）称 6-Luna 在多数任务上处于帕累托前沿。与 Opus 5.5 发布相隔不足 2 小时（16:29 vs 18:00 UTC）。 |
| 批注 | 与 Opus 5.5 的「性能+缓存」打法不同，OpenAI 用腰斩定价主打渗透——双旗舰同日撞车说明头部实验室已把对方发布日视为必须对冲的事件，营销日历完全联动；开发者选型与定价权重估窗口被压缩到同一天。 |
| 评论摘录 | 作者 simonw（[评论页](https://news.ycombinator.com/item?id=49805509)）："GPT-6 Luna 的价格只有 GPT-5.6 Luna 的一半，这是件大事。" 同页作者 gizmodo59 补充：OpenRouter 月榜显示 5.6-Luna 仍是当月用量第一——新一代发布初期，实际负载仍由上一代承载。 |

**头条融合判断：**

1. **我们判断**：竞争焦点已迁移到「agentic 负载的性价比曲线」。双方发布材料的重合点不在能力宣称，而在成本结构：缓存降价、腰斩定价、速度提升——全部服务于长时程 agent 工作流的单位经济性。
2. **我们判断**：用量侧给出关键校准——OpenRouter 月榜当月用量第一仍是上一代 5.6-Luna。旗舰发布 ≠ 生态切换，切换滞后通常以季度计；发布日的热度脉冲不应外推为即期收入结构变化。
3. **我们判断**：Hype vs Reality 鉴别分层。高可信（可直接核对）：缓存 $0.20/M 降 60%（定价事实）、Terminal-Bench 66.4% vs 57.9%（第三方 benchmark）；中可信（依赖自家测法）：「快 30%+」「比上代更强」类宣称；低可信：GPT-6 侧性能宣称（官方页 403，仅评论区转述）。基于 Anthropic 单方数据的「性能领先」判断置信度约 65%，若 OpenAI 后续放出基准数据，格局可能有出入。
4. **tech_generalist 视角**：「Pacing the Frontier」修辞正在被社区定价为竞争策略而非治理承诺。发布评论区的主流读法是言行不一（作者 sailingparrot）；更尖锐的版本来自作者 epolanski 与 DiogenesKynikos：Amodei 呼吁的具体行动项是对华 GPU 与设备出口管制，而非自我设限——前沿实验室的安全修辞被读成「以安全之名行护城河之实」。对监管线的推论：若自监管修辞被市场普遍视为监管俘获，行业缓冲真实监管压力（EU/DOJ/出口管制）的能力将被削弱，监管落地反而更陡。该判断基于评论区定性样本，置信度约 60%。
5. **tech_generalist 视角**：需求侧的一手成本核算在拆穿「半价」叙事。评论区作者 sieve 贴出 30 天真实用量：订阅制下约 $10 覆盖 DeepSeek V4 Flash + MiMo + GLM 约 $184 的等价 API 用量，且指出 Luna 缓存读取与输入价差 8-10 倍对重缓存编码负载足以吞噬「半价」优势。「便宜」的结论高度依赖计价方式与负载画像；模型层定价权实际上正在被订阅聚合层截胡——这与 OpenRouter 用量向上代低价型号聚集互证。

---

## 值得一读

### 3. 五角大楼将平民伤亡归因 Palantir AI 过度依赖

| 项目 | 内容 |
|---|---|
| 原文 | [Pentagon: Palantir AI Overreliance Led to Strike Killing 123 Iranian Children](https://news.ycombinator.com/item?id=436148)（Bloomberg；官网 403 未能抓取，链接为 HN 讨论页） |
| 热度 | ▲955 · 💬541 · 2026-09-22 [id:436148]（另有 Gizmodo 同题版本 [id:436090]） |
| 摘要 | 五角大楼首次在官方叙事中将平民伤亡与「AI 过度依赖」直接挂钩：2026-09-22 空袭造成 123 名伊朗儿童死亡，官方归因指向 Palantir 系统的过度依赖。HN 高赞评论（作者 legitster）提供反叙事：AI 是替罪羊，根因是目标审核团队被裁撤 + 白宫强推 1000 目标清单。 |
| 批注 | 技术问责进入官方语言，但社区的制度性归因（模型是放大器，责任在制度设计）比「AI 杀人」标题更接近事实——这直接决定监管走向是针对模型还是针对流程。 |

### 4. 78% 读者弃读 AI 生成文本

| 项目 | 内容 |
|---|---|
| 原文 | [I don't want to read what you didn't write](https://blog.colinbreck.com/i-dont-want-to-read-what-you-didnt-write/) |
| 热度 | ▲1054 · 💬452 · 2026-09-21 [id:432595] |
| 摘要 | 调查数据：78% 读者遇到 AI 生成文本会弃读，71% 会主动避开该作者——AI 内容的信任折价首次被量化到这个规模。 |
| 批注 | 需求侧约束被量化，对内容生态与 AI 写作工具构成实质天花板；与 macOS 27 强制植入形成供给侧-需求侧对撞（见第 5 条）。 |

### 5. macOS 27 删除 Apple Intelligence 关闭开关

| 项目 | 内容 |
|---|---|
| 原文 | [I said no and Apple said yes](https://dbushell.com/2026/09/22/apple-intelligence/) |
| 热度 | ▲869 · 💬695 · 2026-09-22 [id:434197] |
| 摘要 | macOS 27 删除了 Apple Intelligence 的关闭开关，系统组件占用 22.28 GB，系统级 AI 渗透不可逆化，用户选择权收窄。 |
| 批注 | 平台锁定效应回潮的消费侧样本（与 Android 17 新增 API 不进 AOSP 的开发者侧样本同构），是反垄断语料的标准输入。 |

### 6. Xiaomi MiMo v2.6：用可验证性对抗宣称式发布

| 项目 | 内容 |
|---|---|
| 原文 | [Xiaomi MiMo v2.6](https://news.ycombinator.com/item?id:432439)（mimo.xiaomi.com 官方页仅返回标题，链接为 HN 讨论页） |
| 热度 | ▲1123 · 💬477 · 2026-09-21 [id:432439] |
| 摘要 | 两个差异化点：实时训练仪表盘（mimo.xiaomi.com/rl/）公开训练过程；技术报告诚实列出未达标项。正文据 HN 评论页（id:49792730）整理。 |
| 批注 | 开源/透明路线用「可验证性」对抗闭源旗舰的「宣称式发布」——在第三方评测帖热度只有发布帖 1/5 的环境里（见共识第 6 条），可验证性本身就是竞争武器。 |

### 7. Samsung 预计 HBM4/HBM4E 产量翻倍以上

| 项目 | 内容 |
|---|---|
| 原文 | [Samsung is expected to more than double output of HBM4/HBM4E](https://en.sedaily.com/finance/2026/09/20/samsung-to-double-hbm4-output-next-year-sources-say) |
| 热度 | ▲557 · 💬456 · 2026-09-20 [id:429138] |
| 摘要 | 玻璃载板清洗产能 2 万→5 万张/月，月投片 18 万→25 万片，HBM 系列占 DRAM 产值比重 40%→80%，12 层 HBM4E 已送样 Nvidia。 |
| 批注 | AI infra 上游供给扩张的领先指标——若落地，2027 年 HBM 供给紧张显著缓解，利好推理负载扩张，削弱「算力稀缺」叙事。 |

### 8. AI 抽走的是组织的制度性知识，不只是个人技能

| 项目 | 内容 |
|---|---|
| 原文 | [AI Has No Wisdom and Neither Will You](https://alexn.org/blog/2026/09/22/ai-has-no-wisdom-and-neither-will-you/) |
| 热度 | ▲384 · 💬551 · 2026-09-22 [id:434921] |
| 摘要 | 核心论点：以制造业外包为类比，AI 不仅替代个体技能，还在抽走组织层面的制度性隐性知识储备；当这一代从业者退出，复利的知识断层才显现。HN 评论（作者 NalNezumi）延伸到「没人会再训练新人」的组织风险。 |
| 批注 | 对「AI 替代论」的结构性反驳——被替代的不是岗位而是知识再生产机制，这条成本以十年计，不在任何模型 roadmap 里。 |

---

## 技术雷达

### 9. Jev/System-1 复现风暴：宣称是营销，机制是已知工程

| 项目 | 内容 |
|---|---|
| 原文 | [Jev in 25 Lines of Python](https://nobodywho.ai/posts/jev-in-25-lines/) [id:437668]；原始宣称 [Typesafe Jev 发布](https://typesafe.ai/blog/introducing-system-one-models-and-jev) [id:400453] |
| 热度 | 复现帖 ▲682 · 💬212（2026-09-23）；原始帖 ▲1885 · 💬494（2026-09-15） |
| 摘要 | Typesafe 于 2026-09-15 宣称 Jev/System One 比 frontier 模型便宜 40-400 倍、快 20-200 倍；72 小时内社区完成 Laya 开源复刻（▲1330）、25 行 Python logprobs 复现（Qwen3-0.6B 上钓鱼分类输出 0.031/0.084/0.885）、CUA-S1 等衍生（[id:428097]，▲90），并有多篇「一年前已开源同架构」的先行工作声明。工程约束随之浮出：选项 token 概率质量需 95%+ 机制才可用，且需字母排列平均抵消模型对 "A" 的先验偏置（评论 id:49812769）。 |
| 批注 | **我们判断（置信度 75%）**：复现门槛低至 25 行代码，强烈暗示 Jev 本质是已知技术组合（logprob 门控/早退/小模型级联）而非新范式；40-400 倍宣称在特定任务分布可能成立，「全面替代 frontier」不成立。配套分析（arcturus-labs ▲324/💬226 [id:435464]）指出护城河在权重不在机制——OpenAI/Anthropic 自有 logprobs 接口，可零成本把同样机制内化进 Agent 产品。本期最清晰的 hype vs reality 案例。 |

### 10. GPT-6 Astra 破译 Enigma MVUEH：能力展示，非可用突破

| 项目 | 内容 |
|---|---|
| 原文 | [GPT-6 Astra breaks Enigma MVUEH](https://cryptocellar.org/bgac/the-mvueh-break.html) |
| 热度 | ▲734 · 💬442 · 2026-09-22 [id:435320]（同题更早版本 [id:427676]，▲396/💬180，prinzai.com，2026-09-19） |
| 摘要 | 2026-09-15 破解 MVUEH 报文：使用 ROSENOW crib + 自研 bombe，攻破 72 位左轮换位（transposition）。 |
| 批注 | 密码学趣味性 > 实用意义（现代密码不走这条路线），归类为符号搜索与约束满足任务上的能力展示而非可用突破；它的价值在于为「前沿模型能做什么」提供可复述的锚点，间接支撑旗舰叙事。 |

### 11. Scaling 维度迁移与供给信号汇总

| 项目 | 内容 |
|---|---|
| 原文 | 三条独立信号：[Samsung HBM4/HBM4E 翻倍](https://en.sedaily.com/finance/2026/09/20/samsung-to-double-hbm4-output-next-year-sources-say) [id:429138]、MiMo v2.6 实时训练仪表盘 [id:432439]、Opus 5.5 缓存降价 60% [id:435736] |
| 热度 | ▲557/💬456 · ▲1123/💬477 · ▲1793/💬1118 |
| 摘要 | MiMo v2.6 公开含未达标项的实时训练仪表盘、Samsung HBM 产能翻倍、Opus 5.5 缓存降价 60%——三条信号同向：竞争维度正从「更大的预训练」转向「推理成本、后训练效率、供给弹性」的多维 scaling。 |
| 批注 | **我们判断**：预训练 scaling 边际收益递减已是共识，新 scaling 维度（推理时计算、缓存经济学、HBM 供给）成为主战场；「算力稀缺」叙事的半衰期取决于 Samsung 扩产的实际兑现节奏。附注：《Attention is all you have》（▲1068/💬325 [id:432085]）为注意力经济评论文而非技术论文，本期未深读，下期管道恢复后可追踪。 |

---

## 社区之声

### 12. 从「它能做什么」到「它对我们做了什么」

| 项目 | 内容 |
|---|---|
| 原文 | 综合：[Palantir 问责帖](https://news.ycombinator.com/item?id:436148)、[78% 弃读率](https://blog.colinbreck.com/i-dont-want-to-read-what-you-didnt-write/)、[macOS 27 强制 AI](https://dbushell.com/2026/09/22/apple-intelligence/)、[AI Has No Wisdom](https://alexn.org/blog/2026/09/22/ai-has-no-wisdom-and-neither-will-you/) |
| 热度 | ▲955/▲1054/▲869/▲384（各条详见「值得一读」） |
| 摘要 | 能力端（双旗舰、MiMo、HBM）与认知觉醒端（Palantir 问责、78% 弃读率、macOS 27 强制 AI、Wisdom 讨论）同期升温。对 AI 事故的归因之争趋于成熟：高赞评论拒绝「AI 替罪羊」叙事，指向制度性根因——模型是放大器，责任在制度设计。 |
| 批注 | **我们判断**：这组讨论是 AI 从新鲜工具走向基础设施级存在的过渡期特征；社区成熟的问责框架（针对流程而非仅针对模型）对预判监管走向有直接参考价值。 |

### 13. 「廉价奇迹」的天级证伪与用户主权对撞

| 项目 | 内容 |
|---|---|
| 原文 | 综合：[Jev 25 行复现](https://nobodywho.ai/posts/jev-in-25-lines/)、[OpenAI 吞噬 Jev 午餐](https://arcturus-labs.com/blog/2026/09/21/will-openai-eat-jevs-lunch/)、[macOS 27 强制 AI](https://dbushell.com/2026/09/22/apple-intelligence/) |
| 热度 | ▲682/▲324/▲869（各条详见前文） |
| 摘要 | Jev 的 40-400 倍宣称在 72 小时内被拆解为 25 行代码复现 + 概率质量门槛 + 字母偏置讨论；同期 macOS 27 删除关闭开关 × 71% 读者避开 AI 作者，供给侧渗透与需求侧抵触同步加强。 |
| 批注 | **我们判断**：当前 AI 周期的两个特征——任何效率宣称会在三天内被复现或证伪（社区的 hype 消化速度本身就是定价机制）；用户主权摩擦若持续扩大，将构成 AI 应用层的政治风险变量（监管、平台反弹、替代品需求），值得跨团队追踪。 |

---

## 数据速览

| # | 原文标题 | 中文 | 分数 | 评论 |
|---|---|---|---|---|
| 1 | Claude Opus 5.5 | Claude Opus 5.5 发布 | ▲1793 | 💬1118 |
| 2 | GPT-6 Sol and Luna | GPT-6 Sol 与 Luna 发布 | ▲1769 | 💬847 |
| 3 | Xiaomi MiMo v2.6 | 小米 MiMo v2.6 | ▲1123 | 💬477 |
| 4 | Attention is all you have | 你拥有的只有注意力 | ▲1068 | 💬325 |
| 5 | I don't want to read what you didn't write | 我不想读你没亲手写的东西 | ▲1054 | 💬452 |
| 6 | Pentagon: Palantir AI Overreliance… | 五角大楼：Palantir AI 过度依赖致 123 名伊朗儿童死亡 | ▲955 | 💬541 |
| 7 | I said no and Apple said yes | 我说了不，苹果说了行 | ▲869 | 💬695 |
| 8 | GPT-6 Astra breaks Enigma MVUEH | GPT-6 Astra 破译 Enigma MVUEH | ▲734 | 💬442 |
| 9 | Jev in 25 Lines of Python | 25 行 Python 复现 Jev | ▲682 | 💬212 |
| 10 | Samsung is expected to more than double output of HBM4/HBM4E | Samsung 预计 HBM4/HBM4E 产量翻倍以上 | ▲557 | 💬456 |
| 11 | AI Has No Wisdom and Neither Will You | AI 没有智慧，你也不会有 | ▲384 | 💬551 |
| 12 | OpenAI is about to eat Jev's lunch | OpenAI 即将吞掉 Jev 的午餐 | ▲324 | 💬226 |

**⚠️ 数据管道状态（2026-10-05 01:24 UTC 复核，NO_DATA 再次确认）**：HN raw_items 库在 2026-09-23 之后无新条目；本摘录为 2026-09-20~23 冻结窗口复盘，滞后约 13 天；09-24 之后热点（双旗舰发布后的社区发酵、10 月初事件）未能覆盖。行动项：采集管道需排查（疑似上游抓取或入库中断）；恢复前日报降级为窗口复盘并显式标注滞后天数。

---

## 共识

**多 agent 一致认同（标「共识」）：**

1. **【共识】双旗舰同日对垒是竞争节奏的质变**：Opus 5.5 与 GPT-6 Sol/Luna 于 2026-09-22 相隔不足 2 小时发布（16:29 vs 18:00 UTC），头部实验室已把对方发布日视为必须对冲的事件；日报头条应合并呈现而非拆成孤立资讯。
2. **【共识】Jev 定性为「已知工程组合 + 营销包装」**：40-400 倍为厂商自报、无第三方基准；72 小时内被 Laya + 25 行 Python 复现解构。正文只写「自报倍数 + 社区可复现」，不把倍数当事实；护城河在权重质量而非机制（logprobs 接口为前沿实验室自有）。
3. **【共识】竞争维度正在迁移**：Opus 5.5 缓存降价 60%、Samsung HBM 产能翻倍、MiMo 公开训练仪表盘——三条独立信号指向同一方向：从预训练规模转向推理成本、后训练效率与供给弹性的多维 scaling。
4. **【共识】能力商品化与治理滞后的裂缝是本期主线**：能力以周为单位商品化（复现天级化），信任与治理以年为单位滞后（78% 弃读率、macOS 27 强制 AI、Palantir 问责进入官方语言但归因框架不成熟）；问责走向（针对模型 vs 针对流程）是监管线关键变量。
5. **【共识】数据管道停摆，本期为冻结窗口复盘**：所有结论带 13 天时效折扣，禁止当作昨日榜单解读；管道修复前延续窗口复盘 + 显式滞后标注的降级方案。
6. **【共识】方法论：发布帖与第三方验证帖配对呈现**：Opus 5.5 官方发布帖 ▲1793 vs ArtificialAnalysis 第三方评测帖 ▲331（[id:435876]），热度比约 5:1——HN 对「发布」的定价远高于「验证」，配对呈现用以抵消营销偏置。

**少数派：**

- **tech_scout**：主张头条让位给「Harness 成为平台层」（GitHub 月榜 deepseek-harness 243,395★、生态双桌面端 + awesome 列表，2026-10-05 取数），Jev 线降雷达。终稿采纳其「Jev 降级」部分；头条仍给双旗舰，理由：Harness 为 GitHub 单信源、HN 侧零覆盖（query_raw_items 无条目），置信度 55 不足以支撑头条。已保留为 follow-up：管道修复后优先验证 HN 侧热度。
- 其余判断（管道告警、成本叙事禁直采厂商倍数、监管前兆入雷达）无异议。

---

## 数据来源（附录）

热度数值全部来自 query_raw_items 冻结快照（每条带 [id:N] 可溯源）；正文与评论摘录来自 fetch_url（URL 见各表格）。本次终稿新增核验：HN 评论页 id:49803892（Opus 5.5，作者 sailingparrot/epolanski/DiogenesKynikos）、id:49805509（GPT-6，作者 simonw/gizmodo59/sieve）；GPT-6 原文 URL 经 query_raw_items(id:435956) 核验为 openai.com/index/introducing-gpt-6-sol-and-luna/；管道复核 query_raw_items(published_after=2026-09-24) = NO_DATA。完整逐条溯源见 reference.md。
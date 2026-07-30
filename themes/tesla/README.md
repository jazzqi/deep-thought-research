# Tesla

> Tesla 在 EV 市场成熟化、FSD/robotaxi 商业化和能源业务扩展中的三条战线——从汽车制造商到 AI/能源公司的叙事验证。

## 范围

**覆盖：**
- EV 市场渗透率与需求周期：全球 EV 销量增速、Tesla 市占率变化（分区域：US/EU/CN）
- 车型周期：Model 2（低成本车型）量产时间线、Cybertruck 爬坡、Semi 交付节奏
- FSD 技术进展：端到端神经网络迭代、V13+ 能力提升、监管审批地图
- Robotaxi 商业运营：Cybercab 量产计划、Fleet 运营经济性、保险/Uber 竞争
- 全自动驾驶监管：NHTSA 安全标准、各州自动驾驶法规、联邦自动驾驶框架进展
- 利润率与成本结构：汽车毛利率（excl. credits）、每车成本下降曲线、降价策略影响
- Dojo 超算项目：AI 训练基础设施 vs NVIDIA GPU 外购的决策、Dojo 对 FSD 训练的实际价值
- 能源业务：Megapack 和 Solar 收入贡献、储能毛利率、Powerwall 3 市场渗透
- 竞争格局：中国 EV 厂商（BYD、蔚小理等）全球扩张、传统车企 EV 转型、新玩家（小米、华为等）

**不覆盖：**
- Elon Musk 个人行为/推文对公司治理的影响（仅关注对业务的实质影响）
- 特斯拉股价的日内交易策略或期权定价
- 传统燃油车市场的整体变化
- 充电基础设施的行业范围分析（仅关注 Supercharger Network）
- Tesla 涉足机器人（Optimus）和企业 AI 产品（仅关注进展时间线，不做估值）
- SpaceX/Twitter/xAI 与 Tesla 之间的资源分配讨论（仅限 Musk 注意力分散风险）

## 核心问题

- **Robotaxi 的"童话故事" vs "现实"** — 2026 年 Cybercab 量产能否如期实现？Tesla 主张的 FSD 无需激光雷达/高精地图的纯视觉方案在 L4/L5 能否真正落地？
- **Model 2 能否重振增长** — $25K 低成本车型能否在 2027 年前量产出货？能否在已被 BYD/中国厂商打穿的低端市场做出差异化？
- **利润率底部在哪** — 汽车毛利率（excl. regulatory credits）还能降多少？当毛利率稳定时，稳态水平是多少（~15% or ~20%）？
- **FSD 价值释放方式** — 是订阅（月付 $99/$199）还是买断（$8K/$12K）模式更优？FSD 的实际 take rate 和渗透率上限？
- **AI 基础设施投入回报** — Dojo 在训练效率上相比 NVIDIA GPU 有显著优势吗？AI 训练基础设施投入的 ROIC 是否存在被高估的风险？
- **ESG/Sustainability 转型风险** — 环保机构对 Tesla 碳排放信用交易的质疑、董事会治理争议是否影响机构持有？
- **BYD 和全球 EV 定价战** — 中国 EV 厂商降价潮是否系统性压低了整个 EV 行业的利润池？Tesla 的定价自主权还剩多少？

## 数据源

- **Tesla 季度财报** — 汽车收入、毛利率（excl./incl. credits）、能源业务收入、FSD 递延收入、现金/AI capex
- **EV 销量跟踪** — 各区域（US/EU/CN）月度/季度注册量、产量 vs 交付量差异
- **中国乘联会 / 欧洲 ACEA** — 中国和欧洲 EV 市场月度销售数据，Tesla vs BYD vs 竞品份额
- **FSD Beta 测试数据** — FSD 版本发布日志、每次 major release 的能力提升、干预里程
- **NHTSA / NHTSA 监管追踪** — FSD 召回事件、自动驾驶安全报告、监管审批状态
- **Dojo/超算项目进展** — Dojo 算力指标、训练成本和效率 vs NVIDIA GPU 的对比
- **Robotaxi 试点城市运营数据** — Cybercab 路测里程、安全指标、运营经济性测算
- **Reuters/路透供应链调研** — 零部件采购、4680 电池产量爬坡、柏林/奥斯汀工厂运营

## 典型参与 Agent

| Agent | 角色 | 关注维度 |
|-------|------|---------|
| tech_generalist | 科技行业全景扫描 | EV 需求周期、竞争格局、Margin 趋势、量产时间线验证 |
| ai_specialist | AI 赛道专项深度 | FSD 端到端技术进展、Dojo 计算架构、AI 训练效率对比 |
| disruptive-innovation 视角 | 颠覆式创新 | FSD/Robotaxi 范式级颠覆、自动驾驶对出行行业的重塑 |
| buffett | 基本面/尾部风险 | 高估值下的安全边际、管理层风险、竞争侵蚀护城河 |
| soros | 反身性/叙事 | FSD 自实现叙事 vs 技术突破验证，Elon 个人品牌与股价的反身性 |
| kahneman | 行为金融/认知偏误 | 市场对 FSD 时间表的过度乐观、确认偏误在 Tesla 投资者中的体现 |
| ten-bagger-hunting 视角 | 十倍投资机会扫描 | FSD 成功情景下的估值跃迁潜力 vs 完全失败的下行风险 |

## 关联主题

- **qqq** — TSLA 在 QQQ 中占比约 2-3%，表现受 EV 叙事和 AI 叙事双重影响
- **disruptive-innovation** — FSD/Robotaxi 是交通运输领域的潜在颠覆式创新
- **nvda** — Tesla 是 NVIDIA 的 GPU 大客户之一（Dojo + 车载），同时自研芯片形成竞合关系
- **energy** — Tesla Megapack 和 Powerwall 在储能领域与能源主题交叉

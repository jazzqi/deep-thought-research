# Roundtable Scratchpad — disruptive-innovation

- Session: 2026-08-08_1955__manual__demo_product_query_raw_items_keyword_source_grok_agentic_ai
- Lead: kevin_kelly
- 议题: 颠覆式创新扫描主题更新：当前哪些技术/商业模式正在穿越颠覆式创新的关键拐点？ 哪些是演示（Demo）、哪些是可量产产品（Product）、哪些正在渗透主流？ 市场定价了多少？哪些范式迁移信号被低估？
【数据 · 全部工具查询，不注入数值】用工具主动取数（禁止凭空写数字）： - 新闻/进展：query_raw_items 工具（keyword + source 双维度）。
  关键词覆盖领域+公司+技术词：grok/agentic ai/ai agent/推理成本/crispr/
  gene editing/glp-1/核聚变/solid state battery/人形机器人/robotaxi/
  quantum/脑机接口/合成生物/AI 制药等；
  source 首选 'telegram:Financial_Express'（中文实时快讯，最先反映科技/产业突发），
  次选 'hackernews'/'solidot'/'36kr'（科技深度），
  也可用 'longbridge'（港美股新闻源，含受影响上市公司报道）。
- 可交易标的：QueryLongbridgeByRouteTool（如 AI 产业链、减肥药相关、机器人
  相关上市公司的基本面/估值/一致预期/最新新闻），
  search_routes / list_routes / inspect_route 探索全部可用数据路由。
- 宏观背景：query_indicators（利率/流动性/风险偏好等） - 单一最新确认：binance_get_price / MarketQuoteTool 等行情工具
【规范 · 必读】用 ReadThemeDocsTool 读取两份规范后动笔： 1. themes/disruptive-innovation/template.md —— 报告结构 v1（SEED 顶层节精确匹配：
   ## Big Picture / ## 共识 / ## 各维度分析 / ## 预测时间线 / ## 分歧地图；
   各维度分析按领域组织：AI/前沿技术、生物科技/医疗、能源/材料、
   消费/商业模式、其他前沿；每领域含 当前状态+成熟度定位+投资信号；
   禁止编号顶层节）
2. themes/WRITING_GUIDE.md —— 写作硬规则（集体署名/金字塔原理/数字溯源）
【方法 · 领域雷达 + 成熟度检验】每个领域按 template.md 范式： - 当前状态：该领域最值得注意的新证据（带来源与日期） - 成熟度定位：技术成熟度 S-curve 位置（研究/原型/Demo/早期产品/主流渗透）
  + Demo vs Product 检验——是演示还是可量产产品？离真实采用还有多远？
- 投资信号：范式迁移方向 + 跟踪指标 + 时间窗口 + 置信度 - 交叉融合敏感度：AI+生物、AI+能源、AI+机器人的交叉点常孕育最大机会 - 没有真实数据支撑的领域写「暂无有效信号」而非硬凑
【立场】服务资本市场投资决策，不输出政治立场。
【格式三铁律】① 加粗后必须留空格（`**当前状态：** 一句话`，禁止无空格致加粗失效）； ② emoji 极度克制——只允许「信号强度汇总表」首列用 emoji，正文一律用文字； ③ 数字带单位/时间/口径。禁止 session 目录名/manual/miss 等内部元数据出现在正文。

- 参与 Agent: ai_specialist, karpathy
- 轮次: 3 / 3
- 状态: ok

## Lead 最终综合

{"action":"finalize","questions":[],"confirmed_missing_indicators":[],"confirmed_event_mappings":[]}

## 第 1 轮（ask）

- 问题: ai_specialist：请将Agentic AI、AI制药、CRISPR、Robotaxi分别按“Demo/早期产品/主流渗透”分级，并明确最小可验证商业指标（真实用户、付费收入、单位经济性或临床终点）及未来6-24个月的证伪条件；特别评估高盛规模化使用Agentic AI、Zoox获准付费无人Robotaxi、字节AI制药产业化等证据是否足以从Demo升级为Product。；karpathy：请聚焦工程现实性与资本定价，比较人形机器人、核聚变、固态电池、脑机接口和量子计算的“演示—量产”鸿沟，并判断NVDA（PE 33.37倍、FY2026营收2159.38亿美元、净利润1200.67亿美元）与TSLA（PE 256.36倍、近期FSD仍需人类监督）分别定价了多少未来增长；同时指出哪些范式迁移信号被市场低估、哪些叙事已明显透支。

## 第 2 轮（ask）

- 问题: ai_specialist：基于本轮新增证据，请最终确认 Agentic AI 与 Robotaxi 的成熟度边界：在缺少公开任务成功率、续费率、单位成本、付费里程、事故率和车辆利用率的情况下，是否将二者分别定为“早期产品”和“有限区域早期产品”，而非主流渗透？请给出未来6—12个月最小可证伪指标，并说明哪些中间层（权限审计、工作流编排、自动驾驶模型授权、车队运营）相对终局叙事被低估。；karpathy：请最终核验人形机器人、固态电池、核聚变、脑机接口、量子计算和AI制药的Demo/Product分级，并明确哪些方向有足够真实数据支持形成投资信号、哪些必须写“暂无有效信号”。同时请判断在缺少估值、财务和一致预期路由数据的情况下，NVDA、TSLA、GLP-1和CRSP只能保留短期报价，是否同意不作具体市场定价倍数结论；若不同意，请仅提供可由已查询来源直接支持的替代判断。

## 第 3 轮（finalize）

- 问题: (无)

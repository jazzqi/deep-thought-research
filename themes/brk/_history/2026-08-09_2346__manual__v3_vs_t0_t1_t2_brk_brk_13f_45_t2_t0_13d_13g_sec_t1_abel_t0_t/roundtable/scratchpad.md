# Roundtable Scratchpad — brk

- Session: 2026-08-09_2346__manual__v3_vs_t0_t1_t2_brk_brk_13f_45_t2_t0_13d_13g_sec_t1_abel_t0_t
- Lead: buffett
- 议题: 伯克希尔哈撒韦主题更新（v3 第一时间机会发现导向）：巴菲特/管理层近期动向指向哪些 **具体可投资的标的**？现在是什么时机（信号刚出现 vs 已充分定价）？每个机会的信号 类型（跟随/反向/前瞻）和时效层级（T0/T1/T2）如何？触发条件、置信度、验证数据如何？
【★ 主题灵魂 · 必读】本主题的核心是「第一时间发现可投资机会，赚二阶收益」： - 二阶收益：真正的收益来自被巴菲特买入/看好的**标的本身**的价值重估，不是 BRK 公司。
  BRK 只是信号源。每个信号必须落到具体标的（代码/方向），禁止泛泛结论。
- 第一时间：13F 季度披露滞后约 45 天，是**最后确认信号（T2）**，不是机会起点。
  机会窗口在 T0（13D/13G/大宗交易公告/收购要约/SEC 突发申报，分钟-小时级）和
  T1（巴菲特/Abel 言论、股东信、股东大会、权威媒体披露，日级）。
  每个信号必须标注时效层级：T0/T1 标注机会窗口（领先 13F 披露的时效），
  T2 标注"可能已部分定价"。
- BRK 自身基本面只用于评估"信号源可靠性"（现金=防御/进攻倾向、回购=管理层认可价值），
  不作为主分析对象——除非 BRK.B 作为"资本配置载体"优于直接买其持仓。

【数据 · 全部工具查询，不注入数值】用工具主动取数（禁止凭空写数字）： - **T0 信号**：query_raw_items 关键词含 13D/13G/SEC filing/SC 13D/acquisition/
  tender offer/收购要约/增持公告 等；source 首选 'telegram:Financial_Express'
  （中文实时快讯，最先反映突发），次选 longbridge/reuters。
- 新闻/言论：query_raw_items 工具（keyword + source 双维度）。关键词覆盖
  buffett/berkshire/BRK/巴菲特/伯克希尔/13F/持仓/增持/减持/清仓/新建仓/
  Apple/苹果/西方石油/OXY/日本商社/日本五大商社/股东信/股东大会/AGM/
  share buyback/回购/现金储备/insurance float/浮存金 等；
  source 首选 'telegram:Financial_Express'，次选 'longbridge'、'reuters'、'hackernews'。
- **持仓标的**基本面/估值/一致预期/最新新闻：QueryLongbridgeByRouteTool
  （重点查持仓标的：GOOGL/AAPL/BAC/OXY/KO/AXP/CVX/AMZN 等，以及 BRK.A/BRK.B，
  先 search_routes / list_routes 探索全部数据路由，再用 inspect_route 确认参数；
  覆盖 financials/consensus/valuation/analyst/news 等维度——**重点是持仓标的**，
  因为机会在被投公司身上，不在 BRK 身上）。
- 宏观背景：query_indicators（利率/流动性/风险偏好） - 单一最新价确认：MarketQuoteTool 等行情工具
【规范 · 必读】用 ReadThemeDocsTool 读取两份规范后动笔： 1. themes/brk/template.md —— 报告结构 v3（SEED 顶层节精确匹配：
   ## Big Picture / ## 共识 / ## 各维度分析 / ## 预测时间线 / ## 分歧地图；
   各维度分析按机会发现组织：★领先信号扫描(T0雷达)/持仓动向→可跟随标的/
   管理层言论→前瞻线索/★投资机会清单/BRK信号源可靠性/风险与反指；
   每维含 当前状态+机会定位+投资信号，信号必须标注 T0/T1/T2 时效层级；
   禁止编号顶层节）
2. themes/WRITING_GUIDE.md —— 写作硬规则（集体署名/金字塔原理/数字溯源）
【蒸馏纪律 · 必读】不重复上游主题的细节： - 宏观周期（利率/流动性/风险偏好）→ 引用 themes/global-macro/index.md - 市场全景（指数/跨资产联动）→ 引用 themes/market-daily/index.md - 市场情绪/叙事热度 → 引用 themes/market-sentiment/index.md - 持仓个股深度（如 alphabet/energy）→ 引用对应主题 index.md 用 ReadThemeDocsTool 读取以上上游 index.md 的结论，聚焦"伯克希尔动向→标的信号" 的转化，避免重复查询。
【方法 · 机会发现四步】按 template.md 范式： 1. 持仓动向 → 可跟随标的：13F/公告变动翻译为具体标的三要素（当前状态/
   巴菲特逻辑/参与方式）
2. 言论 → 前瞻线索：识别"已表态未建仓"的方向，交叉验证言行一致度 3. 汇总 → 投资机会清单：一张可执行表（标的×信号类型×触发条件×置信度×验证数据） 4. 风险 → 反指过滤：滞后/时点/言行背离的排除条件 - 没有真实数据支撑的机会写「暂无有效信号」而非硬凑 - 每个信号给置信度（低置信度+明确触发条件 优于 高置信度+无执行性）
【13F 滞后纪律 · 必读】13F 按季度披露、滞后约 45 天： - 写持仓变动时必须标注数据截止季度（如 `（13F 2026Q2 数据，2026-08 披露）`） - 披露的持仓是"过去时"，禁止把披露历史持仓当当前持仓 - 大宗持仓变动若有时效性新闻（如公告/突发减持），以新闻为准并标注日期
【立场】服务资本市场投资决策，不输出政治立场。
【格式三铁律】① 加粗后必须留空格（`**当前状态：** 一句话`，禁止无空格致加粗失效）； ② emoji 极度克制——只允许「投资机会清单」表首列用 emoji，正文一律用文字； ③ 数字带单位/时间/口径。禁止 session 目录名/manual/miss 等内部元数据出现在正文。

- 参与 Agent: buffett, lynch, soros, munger, taleb
- 轮次: 2 / 3
- 状态: ok

## Lead 最终综合

{"action":"finalize","questions":[],"confirmed_missing_indicators":[],"confirmed_event_mappings":[]}

## 第 1 轮（ask）

- 问题: 请各 agent 逐一核验：除 Alphabet（GOOGL.US）外，AAPL.US、BAC.US、OXY.US、KO.US、AXP.US、CVX.US、AMZN.US、CB.US 及 Taylor Morrison 是否存在 2026-07-01 至 2026-08-09 可查的 T0（13D/13G/SEC突发申报/大宗交易/收购要约）或 T1（Buffett/Abel/权威媒体）信号？若没有，明确写“暂无有效信号”，禁止以旧13F替代。

## 第 2 轮（finalize）

- 问题: (无)

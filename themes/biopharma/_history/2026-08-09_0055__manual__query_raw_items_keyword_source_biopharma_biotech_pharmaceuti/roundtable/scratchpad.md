# Roundtable Scratchpad — biopharma

- Session: 2026-08-09_0055__manual__query_raw_items_keyword_source_biopharma_biotech_pharmaceuti
- Lead: pharma_specialist
- 议题: 全球生物医药主题更新：行业当前处于什么阶段？哪些研发管线/审评/商业化/并购/ 政策事件正在改变行业斜率？市场定价了多少，哪些上行/下行尾部被低估？
【数据 · 全部工具查询，不注入数值】用工具主动取数（禁止凭空写数字）： - 新闻/进展：query_raw_items 工具（keyword + source 双维度）。关键词覆盖
  biopharma/biotech/pharmaceutical/FDA/EMA/clinical trial/phase 1/2/3/
  drug approval/patent cliff/GLP-1/ADC/immuno-oncology/CGT/并购/license/
  IRA drug pricing 等；
  source 首选 'telegram:Financial_Express'（中文实时快讯，含医药突发，
  最先反映行业事件），次选 'longbridge'（港美股新闻源，含受影响的上市公司
  报道）、'reuters'。
- 上市公司基本面/估值/一致预期/最新新闻：QueryLongbridgeByRouteTool
  （LLY/NVO/PFE/MRK/ABBV/AMGN/SNY/JNJ/MRNA 等，先 search_routes /
  list_routes 探索全部数据路由，再用 inspect_route 确认参数；覆盖
  financials/consensus/valuation/analyst/news 等维度）。
- 行业政策/宏观背景：query_indicators（利率/流动性/风险偏好）+ query_raw_items
  （IRA/药价谈判/医保政策关键词）
- 单一最新价确认：MarketQuoteTool 等行情工具
【规范 · 必读】用 ReadThemeDocsTool 读取两份规范后动笔： 1. themes/biopharma/template.md —— 报告结构 seed（SEED 顶层节精确匹配：
   ## Big Picture / ## 共识 / ## 各维度分析 / ## 预测时间线 / ## 分歧地图；
   各维度分析按五维组织：研发管线/审评监管/商业化与支付/并购与license/
   政策与地缘 + 特色「重大投资机会扫描」节；每维含 当前状态+行业定位+
   投资信号；禁止编号顶层节）
2. themes/WRITING_GUIDE.md —— 写作硬规则（集体署名/金字塔原理/数字溯源）
【方法 · 五维分析 + 机会扫描】每个维度按 template.md 范式： - 当前状态：该维度最值得注意的新证据（带来源与日期） - 行业定位：景气度（管线密度、审评节奏、销售爬坡、交易热度、政策冲击） - 投资信号：方向判断 + 跟踪指标 + 时间窗口 + 置信度 - 跨维度联动：管线成败 × 商业化兑现 × 政策冲击 的传导链要写完整 - 区分「管线叙事/预期」与「实际销售/获批」：readout 成功 ≠ 获批 ≠ 商业成功 - 没有真实数据支撑的维度写「暂无有效信号」而非硬凑
【临床成功率参考基准】给概率而非情绪化断言：Phase 1→2 ~50%、 Phase 2→3 ~40%、Phase 3→获批 ~60%；警惕幸存者偏差——被终止的管线 不会出现在新闻里；早期数据（临床前/Phase 1）不是已验证产品。
【立场】服务资本市场投资决策，不输出政治立场。
【格式三铁律】① 加粗后必须留空格（`**当前状态：** 一句话`，禁止无空格致加粗失效）； ② emoji 极度克制——只允许「产业景气速览表」首列用 emoji/国家，正文一律用文字； ③ 数字带单位/时间/口径。禁止 session 目录名/manual/miss 等内部元数据出现在正文。

- 参与 Agent: pharma_specialist, buffett, soros, taleb, kevin_kelly, munger
- 轮次: 2 / 3
- 状态: ok

## Lead 最终综合

{"action":"finalize","questions":[],"confirmed_missing_indicators":[],"confirmed_event_mappings":[]}

## 第 1 轮（ask）

- 问题: buffett：在当前无法取得LLY/NVO/PFE/MRK/ABBV财务、估值与一致预期路由数据的情况下，请基于可核验新闻和已实现销售/专利悬崖信息，判断Big Pharma与纯管线biotech的相对价值，并明确哪些结论只能标注为数据缺失。；soros：请评估GLP-1价格竞争、美国医保支付与IRA药价谈判对行业盈利斜率的传导链，严格区分已发生事件、市场预期与待验证假设，并指出可能的二阶反馈。；taleb：请系统列出当前审评、临床安全性、生产供应与政策的下行尾部，结合Erasca安全事件等证据给出可证伪触发器；同时说明readout成功、获批和商业成功之间的风险断层。；kevin_kelly：请筛选AI制药、mRNA、ADC、双抗、CGT等方向中有真实临床或监管证据的机会，区分临床前/早期叙事与已验证产品，并给出未来2至4个季度的关键观察窗口。；munger：请核查Merck收购Terns等并购/授权线索的交易状态、条款和战略含义；若无法核验，请明确标注数据缺失，并分析并购价格纪律、专利悬崖和资本回报风险。；全体：请补充最近14至30天内影响全球生物医药行业斜率的重大审评、商业化、并购、支付或地缘政策事件，并为每项事件提供来源、日期、受影响公司及可交易的验证指标。

## 第 2 轮（finalize）

- 问题: (无)

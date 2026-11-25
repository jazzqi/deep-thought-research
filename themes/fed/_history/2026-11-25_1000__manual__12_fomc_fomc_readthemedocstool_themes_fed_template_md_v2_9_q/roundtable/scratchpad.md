# Roundtable Scratchpad — fed

- Session: 2026-11-25_1000__manual__12_fomc_fomc_readthemedocstool_themes_fed_template_md_v2_9_q
- Lead: soros
- 议题: 美联储主题更新：政策基准、未来 12 个月 FOMC 会议时间表、关键数据指标、 FOMC 成员立场、市场定价偏差、政策二阶效应、反应函数、多路径概率评估。
【规范 · 必读】用 ReadThemeDocsTool 读取 themes/fed/template.md —— 报告结构 v2（核心价值 = 美联储政策分析与预测；顶层节精确标题 + 9 大模块， 缺模块视为缺陷），未读规范即写作视为流程缺陷。
【数据 · 全部自主查询】用 query_calendar_events(country=US, days=180, lookback_days=14, limit=200) 查询未来 12 个月美国高重要事件（FOMC 会议/CPI/非农等）+ 最近 14 天已发布事件 （含 actual，如昨日 CPI 实值——以 actual 字段为准，勿用 forecast 冒充； ★ limit 必须 ≥200，否则 14 天窗口内初请/财报等高频事件会挤掉 CPI 等关键数据）； 用 query_fomc 查询 FOMC 会议结构化信息（SEP/链接/点阵图）；用 query_indicators (country=us) 查询美国宏观指标；**成员信息优先调用 query_fomc_members** （DB 结构化：19 位现任领导 + 票委状态 + 下次轮值 + 最新言论 + stance 鹰鸽分 + stance_changes_30d 转边事件 + scorecard 投票/言论/综合/样本 + divergences 言行不一）； **优先一次调用 `GET /api/fomc/committee-brief` 或 `query_fomc_members(member="A,B,C")` 批量取数， 不要逐人请求 /members/{id}/statements**；言论事件已按成员+日期去重； 市场预期用 `query_fomc_market` 或 `GET /api/fomc/market-expectations`（Polymarket 事件合约， 非 CME FedWatch/OIS；附 volume/liquidity，thin 不作结论）； **若有转边，必须在 Big Picture 开头高亮**；委员会综合分与每人综合分必须带样本状态； 需要完整轮换表/文档结构时读 themes/fed/FOMC_MEMBERS.md，再按需用 query_raw_items(keyword=Fed OR FOMC) 定向补充；市场定价用 QueryIndicatorsTool 拉取美债收益率/美元指数。前值/预测以工具返回为准，缺失标 ⚠️，禁止编造。 agents 无 web 搜索能力——**禁止输出任何工具查询不到的具体日期/数值/言论**， 未核实的写「数据缺失（工具未返回）」或「待人工确认」，宁可留白不可瞎编。 ★ **必查指标清单**（template.md §2 硬约束）：总体/核心 CPI 同比环比、
 PPI 同比/环比（含核心）、PCE/核心 PCE、非农/失业率、平均时薪、JOLTS、
 初请/续请、零售销售、ISM 制造/非制造、密歇根信心——每项必须出现在
 「关键经济指标监测表」，查到写 actual、查不到写「数据缺失」并保留该行，
 遗漏任何一项视为缺陷。

【记忆 · 分析中自主沉淀】分析中如产生以下内容，调用 remember 工具存储（个人记忆层）： - 客观事实 / 带出处与数据的关键结论（如"非农 -2.3万，美元走低黄金上涨"） - 短期有效的观察（如"9月加息25bp隐含概率 56.5%"） 无需存储：过程性描述、已 publish 进主题文档的完整内容（避免重复）。
【格式三铁律】① 加粗后必须留空格（**当前政策基准：** 内容）； ② 高重要级标题加粗；③ emoji 克制——只用于表格首列/章节标题，正文用文字。

- 参与 Agent: soros, nick_timiraos, dalio, kahneman, taleb
- 轮次: 1 / 3
- 状态: ok

## Lead 最终综合

{"action": "finalize", "questions": [], "confirmed_missing_indicators": ["美国PCE同比", "美国核心PCE同比"], "confirmed_event_mappings": [], "actions": [{"type": "follow_up", "priority": "P1", "summary": "11-25 21:30 公布10月PCE，验证核心PCE同比≥3.2%预测；若环比≤0.2%则12月加息80%基准需重估", "verification_date": "2026-11-25", "confidence": 0.8}, {"type": "monitoring", "priority": "P2", "summary": "监控1月连加预期降温（Polymarket加息25bp 7d -7.5pp）与CTA 680亿机械抛售，作为鹰派反身性回路拐点先行信号", "recurrence": "weekly"}]}

## 第 1 轮（finalize）

- 问题: (无)

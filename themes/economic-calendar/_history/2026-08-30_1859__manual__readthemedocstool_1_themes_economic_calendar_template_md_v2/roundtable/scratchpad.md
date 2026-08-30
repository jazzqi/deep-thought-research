# Roundtable Scratchpad — economic-calendar

- Session: 2026-08-30_1859__manual__readthemedocstool_1_themes_economic_calendar_template_md_v2
- Lead: ackman
- 议题: 下周全球财经日历预读：重点事件识别、影响评估、数据指标预测与场景路径。
【规范 · 必读】用 ReadThemeDocsTool 读取两份规范后动笔： 1. themes/economic-calendar/template.md —— 报告结构 v2（TL;DR/行情快照/场景表三要素/
   对组合的含义/数据可用性声明等 13 节，缺节视为缺陷）
2. themes/WRITING_GUIDE.md 的「财经日历报告专项」节 —— 写作硬规则（数字带口径/
   禁内部元数据/验证闭环等）
未读取规范即写作视为流程缺陷。
【数据 · 全部自主查询】prompt 不注入日历数据。用 query_calendar_events 工具 查询未来 14 天事件（参数：days=14，可按 importance/country 过滤）。原则： - 3 星（high）必分析（重点主轴）；2 星（medium）分工发掘（指派 1 名参与者
  扫描识别有价值事件，提交圆桌共同分析）；1 星（low）噪音忽略。
前值/共识以工具返回为准，缺失标 ⚠️，禁止编造。
【承接 · 硬性要求】用 ReadThemeDocsTool 读取上周 recap.md（路径 themes/economic-calendar/{本周一YYYY-MM-DD}__{本周日YYYY-MM-DD}/recap.md）： ① 观察清单逐条承接进「日历外的已知未知」； ② 成绩单用于校准置信度。
【行情快照】用 QueryIndicatorsTool / MarketQuoteTool 拉取当前水平 （10Y/2Y 美债、DXY、SP500、Brent、Gold、CNH）写入快照节。
【格式三铁律】 ① 加粗后必须留空格（`**第一触发器：** 🇺🇸 美国 7 月 CPI`， 禁止 `**xxx：**🇺🇸` 无空格致加粗失效）； ② 高重要级的标题一律加粗（`**美国 Core CPI**`/ `**非农失业率**`/`**联邦基准利率**`）； ③ emoji 克制——只用于表格首列/章节标题/TL;DR 关键句， 长段落正文用国家全名（`美国`），禁止每句堆 emoji。数字带单位/时间/口径； 禁止 session 目录名/manual/miss 等内部元数据出现在正文。

- 参与 Agent: ackman, soros, dalio, zhou_jintao
- 轮次: 1 / 3
- 状态: ok

## Lead 最终综合

{"action": "finalize", "questions": [], "confirmed_missing_indicators": ["us_10y_yield", "us_2y_yield", "gold_xauusd", "usdcnh", "us_nfp_forecast", "us_cpi_yoy_forecast"], "confirmed_event_mappings": [], "actions": [{"type": "monitoring", "priority": "P1", "summary": "监控9月1日ISM制造业指数（前值55.6，共识55.2），若跌破55将触发组合防御性调整", "recurrence": "daily"}, {"type": "follow_up", "priority": "P1", "summary": "9月4-5日非农/失业率数据验证：若失业率>4.2%则触发Sahm Rule早期预警，需更新降息交易假设", "verification_date": "2026-09-05"}, {"type": "monitoring", "priority": "P2", "summary": "监控霍尔木兹海峡通行僵局进展与OPEC+9月5日会议，评估能源价格冲击对CPI的传导风险", "recurrence": "daily"}]}

## 第 1 轮（finalize）

- 问题: (无)

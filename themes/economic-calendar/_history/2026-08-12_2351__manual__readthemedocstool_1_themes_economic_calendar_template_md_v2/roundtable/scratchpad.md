# Roundtable Scratchpad — economic-calendar

- Session: 2026-08-12_2351__manual__readthemedocstool_1_themes_economic_calendar_template_md_v2
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
- 轮次: 3 / 3
- 状态: ok

## Lead 最终综合

{"action":"finalize","questions":[],"confirmed_missing_indicators":[],"confirmed_event_mappings":[]}

## 第 1 轮（ask）

- 问题: 请 soros 扫描并评估 2026-08-17 至 2026-08-23 的中国主轴：7月社零、工业增加值、固定资产投资（8/17）及8月LPR（8/20）。请给出不编造共识数值前提下的方向性基准预测、上/下行触发条件、对CNH/中国风险资产/工业品的场景路径，并确认日历未给共识是否构成待采集指标缺口。；请 dalio 与 zhou_jintao 分别评估全球交叉验证：美国7月PPI、零售销售、密歇根信心及初请（8/13–14）如何验证已公布的美国7月CPI（同比3.4%、核心同比2.5%、环比分别+0.1%/+0.2%）的去通胀叙事；以及欧元区GDP修正、日本二季度GDP和贸易数据对全球增长/美元/久期的影响。请明确各自基准情景、可证伪阈值及组合建议。

## 第 2 轮（ask）

- 问题: 请 soros 补充扫描英国主轴并与中国主轴整合：8月18日英国失业率/含红利三个月平均工资同比（前值4.9%/4.3%）及8月19日英国总体/核心CPI同比（前值均2.6%）的基准方向、明确的上/下行触发条件，以及对英镑、英国短端利率、全球美元和风险偏好的场景路径。日历未返回四项共识，请确认应列为待采集缺口而非数值预期。；请 dalio 与 zhou_jintao 对下周非中美的全球事件作最终排序和可证伪判断：日本二季度GDP初值（8月16日23:50 UTC，实际GDP季环比前值0.5%、年化前值1.8%）及7月贸易账（8月19日，前值-4,069亿日元）、加拿大7月CPI（8月17日）和欧元区7月HICP终值（8月19日）。请说明哪些进入重点事件深度解读、哪些仅列周历，且严格依据日历缺失的共识/前值标注数据缺口。另请核验上期recap准确路径或提供观察清单与成绩单；指定路径不存在，正式稿无法完成逐条承接和置信度校准。

## 第 3 轮（finalize）

- 问题: (无)

# Roundtable Scratchpad — economic-calendar

- Session: 2026-08-10_1359__manual__readthemedocstool_1_themes_economic_calendar_template_md_v2
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

- 问题: 请 soros 提出美国 CPI、PPI、零售销售联合情景的可证伪阈值及跨资产反应，并评估霍尔木兹通航未确认对能源—通胀尾部的影响。；请 dalio 分析美国逾千亿美元国债标售、10Y/2Y收益率与美元的传导链，并评估澳洲联储决议的全球流动性意义。；请 zhou_jintao 扫描英国二季度GDP、欧元区工业生产/GDP、日本二季度GDP及美国消费者信心/零售控制组，筛选应进入本周重点时间线的中等重要性事件，并给出数据缺口。

## 第 2 轮（ask）

- 问题: 请 soros 在不使用日历未返回数字的前提下，确认美国CPI同比共识在日历条目中出现3.4%与3.5%的口径冲突应如何处理；并给出CPI—核心PPI—零售销售（控制组共识缺失）联合情景中最可执行的证伪信号与跨资产排序。；请 dalio 与 zhou_jintao 共同确认本周重点时间线的最终取舍：澳洲联储、英国二季度GDP、欧元区6月工业产出/二季度GDP、日本二季度GDP、密歇根信心各自是否进入正文；对每项写明前值/共识缺口、影响链及为何不应喧宾夺主。另请校验上周观察清单中霍尔木兹实际通航、战争险/运费、油轮安全、美国关税成本传导、国债拍卖需求与日元干预数据的可观测触发器。

## 第 3 轮（finalize）

- 问题: (无)

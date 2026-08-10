# Roundtable Scratchpad — economic-calendar

- Session: 2026-08-10_0900__manual__readthemedocstool_1_themes_economic_calendar_template_md_v2
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
【承接 · 硬性要求】用 ReadThemeDocsTool 读取上周 recap.md（路径 themes/economic-calendar/{本周一YYYY-MM-DD}__{本周日YYYY-MM-DD}/recap.md）： ① 观察清单逐条承接进「日历外的已知未知」；② 成绩单用于校准置信度。
【行情快照】用 QueryIndicatorsTool / MarketQuoteTool 拉取当前水平 （10Y/2Y 美债、DXY、SP500、Brent、Gold、CNH）写入快照节。
【格式三铁律】① 加粗后必须留空格（`**第一触发器：** 🇺🇸 美国 7 月 CPI`， 禁止 `**xxx：**🇺🇸` 无空格致加粗失效）；② 重要性星级一律加粗（`**⭐⭐⭐**`/ `**⭐⭐**`/`⭐`）；③ emoji 克制——只用于表格首列/章节标题/TL;DR 关键句， 长段落正文用国家全名（`美国`），禁止每句堆 emoji。数字带单位/时间/口径； 禁止 session 目录名/manual/miss 等内部元数据出现在正文。

- 参与 Agent: ackman, soros, dalio, zhou_jintao
- 轮次: 3 / 3
- 状态: ok

## Lead 最终综合

{"action":"finalize","questions":[],"confirmed_missing_indicators":[],"confirmed_event_mappings":[]}

## 第 1 轮（ask）

- 问题: soros：请评估8月9日霍尔木兹“尚未重开/协议无进展/船只遇袭”新闻对本周美国CPI能源项、通胀预期与油价尾部的影响；给出可执行触发信号及其推翻条件。；dalio：请分析美国8月11日至13日逾千亿美元国债标售与8月12日CPI、8月13日PPI、8月14日零售销售的联动，明确2Y/10Y、美元、风险资产的三种情景路径；同时审阅10Y、2Y、DXY、Brent、Gold、CNH直接行情缺失是否妨碍结论。；zhou_jintao：请完成2星全球事件筛选：英国二季度GDP与6月月度GDP、欧元区6月工业产出、日本7月企业商品物价、澳洲联储决议；仅保留会改变全球增长或通胀叙事者，并用日历返回的前值/共识及缺失字段说明判断。

## 第 2 轮（ask）

- 问题: 全体：请最后确认报告主轴与事件排序：美国7月CPI（8月12日）—10年期国债标售（8月12日）—PPI（8月13日）—零售销售（8月14日）是否应共同列为最高优先级；并将基准、再通胀、增长下行三条路径各自的可证伪触发条件压缩为一句，避免把单一数据当作结论。；soros/dalio：请确认霍尔木兹风险在最终报告中的严格表述：8月8—9日谈判与航运安全新闻只能构成8月及以后能源、通胀预期和油运成本的尾部风险，不能解释或上调8月12日发布的美国7月CPI；同时确认“持续航运受阻+油价/运费/通胀预期同步上行”为升级条件。；zhou_jintao：请最终确认二级全球事件的取舍与数据纪律：保留澳洲联储、英国二季度及6月GDP、欧元区6月工业产出、日本7月企业商品物价；所有缺失共识均以⚠️缺共识标注，不给无来源点预测。

## 第 3 轮（finalize）

- 问题: (无)

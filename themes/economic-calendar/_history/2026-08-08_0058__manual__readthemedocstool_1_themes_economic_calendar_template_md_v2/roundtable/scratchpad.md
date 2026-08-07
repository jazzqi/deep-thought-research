# Roundtable Scratchpad — economic-calendar

- Session: 2026-08-08_0058__manual__readthemedocstool_1_themes_economic_calendar_template_md_v2
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
【格式】国家标注 emoji+全名（表头/关键句）；长段落用全名；数字带单位/时间/口径； 禁止 session 目录名/manual/miss 等内部元数据出现在正文。

- 参与 Agent: ackman, soros, dalio, zhou_jintao
- 轮次: 3 / 3
- 状态: ok

## Lead 最终综合

{"action":"finalize","questions":[],"confirmed_missing_indicators":[],"confirmed_event_mappings":[]}

## 第 1 轮（ask）

- 问题: soros：请围绕🇺🇸美国7月CPI（8月12日）、PPI（8月13日）给出可交易的上/下行意外阈值、核心分项确认条件，以及美元、2年期美债、黄金和美股的非线性反应；尤其说明在霍尔木兹能源风险未消除时，何种数据组合会推翻软着陆基准情景。；dalio：请评估🇺🇸美国8月11—13日国债标售、CPI/PPI、8月14日零售销售与初请数据的联动：何种组合构成“通胀黏性+财政供给压力+增长不弱”的高利率更久路径？请明确久期、2s10s曲线、美元和信用资产的组合建议与反证条件。；zhou_jintao：请完成2星全球事件扫描，筛选并分析🇦🇺澳大利亚央行8月11日决议、🇯🇵日本央行7月会议意见摘要及国内企业物价、🇪🇺欧元区GDP修正/工业产出、🇬🇧英国二季度GDP中最可能外溢全球资产的节点；同时承接🇨🇳中国制造业PMI 49.2、非制造业PMI 49.0（2026年7月）的弱景气信号，说明对CNH、工业品和风险偏好的传导。请严格标明日历未返回的共识数据。

## 第 2 轮（ask）

- 问题: 请三位参与者在最终追问中只补充可直接写入终稿的核验结论：① 以日历原始字段为准，确认🇺🇸美国7月整体CPI同比共识在同源条目中为3.4%与3.5%的冲突应如何在“数据可用性声明”披露；② 确认🇨🇳中国7月PPI同比日历显示前值4.1%、共识3.8%但未标正负号，终稿不得沿用首轮出现的负号；③ 给出🇦🇺澳大利亚联储、🇯🇵日本银行意见摘要/企业物价、🇪🇺欧元区GDP/工业产出、🇬🇧英国二季度GDP中各1项最应入重点时间线的事件及其严格基于前值/共识的情景阈值（共识缺失须明确标⚠️）。；请dalio或soros补齐可验证的行情快照来源与报告时点：🇺🇸10年期/2年期国债收益率、DXY、S&P 500、Brent、Gold、USDCNH；如工具仍不能返回，请逐项确认缺失而非引用无日期或未经核验数字。同时请确认“高利率更久”基准被推翻的联合条件，须包括核心CPI/PPI、零售/初请、10年期国债标售需求三类证据。

## 第 3 轮（finalize）

- 问题: (无)

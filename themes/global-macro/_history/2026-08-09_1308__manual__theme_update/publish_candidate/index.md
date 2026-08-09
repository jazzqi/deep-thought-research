---
name: 宏观（全球+美国+中国）
slug: global-macro
status: active
lead_agent: soros
created: 2026-07-29
updated: 2026-08-09T13:22:14+08:00
revision: 2026-08-09
sources:
  - path: 2026-08-09_1308__manual__theme_update/reference.md
    agent: theme_update
    summarized: false
---

# 宏观（全球+美国+中国）

## Big Picture

全球宏观交易的核心标的不是单一公司，而是一组由美元、美国国债、实际利率、黄金、工业品和区域风险资产组成的资产体系。其“商业模型”可以理解为货币与财政信用定价：央行通过政策利率和资产负债表影响资金成本，政府通过债券发行把财政支出转化为市场久期供给，企业和居民部门再决定流动性能否转化为信贷、投资与消费。当前主线已从“全球是否同步软着陆”转向“通胀能否持续回落、财政供给是否推高期限溢价、宽货币能否传导至私人部门需求”。美国面临通胀高于目标与财政融资压力并存，中国面临货币总量与信用需求背离，地缘冲突则提供能源与通胀路径上的尾部风险。未来资产表现更可能分化，而不是由“全球同步降息”这一单一叙事驱动。
本主题没有单一公司的营收、利润、估值倍数或分析师一致预期，因此不能虚构公司财务数据。对宏观资产而言，基本面替代变量是通胀、增长、财政融资、信用传导、实际利率和风险溢价；估值则应围绕现金流久期、无风险利率和风险溢价变化展开。当前可验证的核心矛盾是：短端政策利率可能存在下行空间，但长端利率未必同步下降。

## 各维度分析

### 叙事/情绪面

全球宏观交易的核心标的不是单一公司，而是一组由美元、美国国债、实际利率、黄金、工业品和区域风险资产组成的资产体系。其“商业模型”可以理解为货币与财政信用定价：央行通过政策利率和资产负债表影响资金成本，政府通过债券发行把财政支出转化为市场久期供给，企业和居民部门再决定流动性能否转化为信贷、投资与消费。当前主线已从“全球是否同步软着陆”转向“通胀能否持续回落、财政供给是否推高期限溢价、宽货币能否传导至私人部门需求”。美国面临通胀高于目标与财政融资压力并存，中国面临货币总量与信用需求背离，地缘冲突则提供能源与通胀路径上的尾部风险。未来资产表现更可能分化，而不是由“全球同步降息”这一单一叙事驱动。

### 基本面

本主题没有单一公司的营收、利润、估值倍数或分析师一致预期，因此不能虚构公司财务数据。对宏观资产而言，基本面替代变量是通胀、增长、财政融资、信用传导、实际利率和风险溢价；估值则应围绕现金流久期、无风险利率和风险溢价变化展开。当前可验证的核心矛盾是：短端政策利率可能存在下行空间，但长端利率未必同步下降。

### 宏观背景

全球宏观交易的核心标的不是单一公司，而是一组由美元、美国国债、实际利率、黄金、工业品和区域风险资产组成的资产体系。其“商业模型”可以理解为货币与财政信用定价：央行通过政策利率和资产负债表影响资金成本，政府通过债券发行把财政支出转化为市场久期供给，企业和居民部门再决定流动性能否转化为信贷、投资与消费。当前主线已从“全球是否同步软着陆”转向“通胀能否持续回落、财政供给是否推高期限溢价、宽货币能否传导至私人部门需求”。美国面临通胀高于目标与财政融资压力并存，中国面临货币总量与信用需求背离，地缘冲突则提供能源与通胀路径上的尾部风险。未来资产表现更可能分化，而不是由“全球同步降息”这一单一叙事驱动。

## 预测时间线

| 时间窗 | 预测 | 置信度 | 提出者 | 提出日期 | 验证 |
|--------|------|--------|--------|----------|------|
| （待添加） |  |  |  |  |  |

## 分歧地图

| 维度 | 观点 A | 观点 B | 分歧根因 |
|------|--------|--------|---------|
| （待添加） |  |  |  |

> **审查意见**：17 条（详见 _history/review/）

## 数据来源

- 美国CPI同比3.5%（数据日期2026-06-01）: query_indicators({category:'macro',country:'us',limit:30,time_range:'24h'}) = 3.5，⚠️数据滞后69天
- 美国核心CPI指数336.065（数据日期2026-06-01）: query_indicators({category:'macro',country:'us',limit:30,time_range:'24h'}) = 336.065，⚠️数据滞后69天
- 美国PPI指数286.827（数据日期2026-06-01）: query_indicators({category:'macro',country:'us',limit:30,time_range:'24h'}) = 286.827，⚠️数据滞后69天
- 美国消费者信心49.5（数据日期2026-06-01）: query_indicators({category:'macro',country:'us',limit:30,time_range:'24h'}) = 49.5，⚠️数据滞后69天
- 美国联储资产负债表6748567.0（数据日期2026-08-05）: query_indicators({category:'macro',country:'us',limit:30,time_range:'24h'}) = 6748567.0
- 中国出口359703900000、进口270641300000（数据日期2026-04-01）: query_indicators({category:'macro',country:'china',limit:30,time_range:'24h'}) = 对应数值，⚠️数据滞后130天
- 美国7月CPI日历预测：总CPI同比3.4%、核心同比2.5%、核心环比0.2%（事件日期2026-08-12）: query_calendar_events({country:'US',days:30,importance:'high,medium',limit:100}) = previous/forecast字段
- 美国财政部2026-08-11至13日标售逾千亿美元国债: query_calendar_events({country:'US',days:30,importance:'high,medium',limit:100}) = 事件
- 美国10年期国债拍卖此前高收益率4.58%（事件日期2026-08-12）: query_calendar_events({country:'US',days:30,importance:'high,medium',limit:100}) = previous字段
- 汇丰预计美国7月CPI核心分项超预期降温: query_raw_items({keyword:'美国 7 月 CPI',limit:50,source:'telegram:Financial_Express',status:null}) = 2026-08-09新闻标题/摘要
- 伊朗寻求走出与美国“既非战争也非和平”僵局: query_raw_items({keyword:'Iran',limit:50,source:'aljazeera',status:null}) = 2026-08-09新闻
- 俄罗斯称边境州遭乌大规模无人机袭击、13人受伤: query_raw_items({keyword:'无人机',limit:50,source:'telegram:Financial_Express',status:null}) = 2026-08-09新闻

- 美国CPI同比3.5%，数据日期2026-06-01（已滞后）: query_indicators({"category":"macro","country":"us","time_range":"24h"}) = 3.5, indicator=cpi_yoy_us_pct
- 美国核心CPI指数336.065，数据日期2026-06-01（已滞后）: query_indicators({"category":"macro","country":"us","time_range":"24h"}) = 336.065, indicator=core_cpi
- 美联储资产负债表6748567.0，数据日期2026-08-05: query_indicators({"category":"macro","country":"us","time_range":"24h"}) = 6748567.0, indicator=fed_balance_sheet
- 美国7月纽约联储1年通胀预期前值3.7%、3年通胀预期前值3.3%，发布日期/事件日期2026-08-10: query_calendar_events({"country":"US","days":30,"importance":"high,medium"}) = previous 3.7%, 3.3%
- 美国财政部计划2026-08-11至13日标售逾千亿美元国债: query_calendar_events({"country":"US","days":30,"importance":"high,medium"}) = event scheduled
- 中国7月M2货币供应年率及7月新增人民币贷款（年初至今）于2026-08-10发布，当前actual为空，系统当前仅返回过时中国出口/进口数据: query_calendar_events({"country":"CN","days":30,"importance":"high,medium"}); query_indicators({"category":"macro","country":"china","time_range":"24h"})
- 2026-08-09 Al Jazeera报道伊朗寻求走出与美国“既非战争也非和平”僵局: query_raw_items({"keyword":"iran","limit":30}) = headline
- 2026-08-09 Financial Express报道俄称边境州遭乌大规模无人机袭击、13人受伤: query_raw_items({"keyword":null,"limit":30}) = headline
- 2026-08-09 Financial Express报道经济学家普遍预期美国通胀年率略有放缓、汇丰预期多个核心分项降温: query_raw_items({"keyword":null,"limit":30}) = headlines; these are expectations/news, not realized CPI values

- 2026-08-09 伊朗寻求走出与美国“既非战争也非和平”僵局: query_raw_items({"keyword":"iran","limit":50,"source":"aljazeera","status":null}) = Al Jazeera headline
- 2026-08-09 俄罗斯称边境州遭乌大规模无人机袭击、已致13人受伤: query_raw_items({"keyword":"无人机","limit":50,"source":"telegram:Financial_Express","status":null}) = Financial Express headline
- 2026-08-09 汇丰前瞻美国7月CPI并预期多项核心分项降温: query_raw_items({"keyword":"美国 7 月 CPI","limit":50,"source":"telegram:Financial_Express","status":null}) = Financial Express headlines
- 2026-08-10 中国7月M2货币供应年率及7月新增人民币贷款（年初至今）: query_calendar_events({"country":"CN","days":30,"importance":"high,medium","limit":100}) = scheduled, actual=null
- 2026-08-12 美国7月CPI预测：总CPI同比3.4%、核心同比2.5%、核心环比0.2%: query_calendar_events({"country":"US","days":30,"importance":"high,medium","limit":100}) = previous/forecast fields
- 2026-08-11至13日美国财政部计划标售逾千亿美元国债: query_calendar_events({"country":"US","days":30,"importance":"high,medium","limit":100}) = scheduled event
- 2026-08-12 美国10年期国债拍卖规模390亿美元、此前高收益率4.58%: query_calendar_events({"country":"US","days":30,"importance":"high,medium","limit":100}) = previous fields
- 美国7月纽约联储1年通胀预期前值3.7%、3年通胀预期前值3.3%: query_calendar_events({"country":"US","days":30,"importance":"high,medium","limit":100}) = previous fields
- 澳大利亚央行2026-08-11现金利率预测4.35%、前值4.35%: query_calendar_events({"country":"AU","days":30,"importance":"high,medium","limit":100}) = previous/forecast fields
- 日本央行2026-08-10公布7月货币政策会议意见摘要: query_calendar_events({"country":"JP","days":30,"importance":"high,medium","limit":100}) = scheduled event
- 当前美国指标查询未返回可用的最新宏观/债券数值快照: query_indicators({"category":"macro,bond,monetary_credit","country":"us","limit":30,"time_range":"24h"}) = 0 indicators
- 当前中国指标查询未返回可用的最新宏观/信贷数值快照: query_indicators({"category":"macro,pmi,monetary_credit","country":"china","limit":30,"time_range":"24h"}) = 0 indicators

- 美国CPI同比3.5（数据日期2026-06-01）: query_indicators(country=us,category=macro,time_range=24h) = 3.5%
- 美国核心CPI数值336.065（数据日期2026-06-01）: query_indicators(country=us,category=macro,time_range=24h) = 336.065（数据库未提供同比口径，未据此推导）
- 美联储资产负债表6748567.0（数据日期2026-08-05）: query_indicators(country=us,category=macro,time_range=24h) = 6,748,567.0（数据库口径/单位未明）
- 中国出口359703900000、中国进口270641300000（数据日期2026-04-01，均被工具标记为超过90天过时）: query_indicators(country=china,category=macro,time_range=24h) = 原始值
- 中国7月M2与新增人民币贷款：日历显示计划于2026-08-10公布，actual为空: query_calendar_events(country=CN,days=30,importance=high,medium) = 未发布
- 美国7月纽约联储1年通胀预期前值3.7%、3年通胀预期前值3.3%，计划2026-08-10公布: query_calendar_events(country=US,days=30,importance=high,medium) = previous 3.7%, 3.3%
- 美国7月CPI预测：总体同比3.4%、核心同比2.5%、核心环比0.2%，前值分别3.5%、2.6%、0.0%，计划2026-08-12公布: query_calendar_events(country=US,days=30,importance=high,medium) = forecast/previous
- 美国8月11日至13日标售逾千亿美元国债，8月12日10年期国债规模390亿美元、前次高收益率4.58%: query_calendar_events(country=US,days=30,importance=high,medium) = event data
- 伊朗寻求走出与美国“既非战争也非和平”僵局（2026-08-09）: query_raw_items(source=aljazeera,keyword=null,limit=50) = headline
- 俄罗斯称边境州遭乌克兰大规模无人机袭击、13人受伤（2026-08-09）: query_raw_items(source=telegram:Financial_Express,keyword=null,limit=50) = headline
- 澳洲联储现金利率前值/预测4.35%，决议计划2026-08-11公布: query_calendar_events(country=AU,days=30,importance=high,medium) = previous/forecast

- 美国CPI同比3.5%，数据日期2026-06-01（已滞后）: query_indicators(country=us,category=macro,time_range=24h) = 3.5
- 美国联储资产负债表6748567.0，数据日期2026-08-05（单位/口径未明确）: query_indicators(country=us,category=macro,time_range=24h) = 6748567.0
- 中国出口359703900000、进口270641300000，数据日期2026-04-01（均已过时）: query_indicators(country=china,category=macro,time_range=24h) = 359703900000.0 / 270641300000.0
- 美国7月CPI日历预测：总体同比3.4%、核心同比2.5%、核心环比0.2%，前值分别3.5%、2.6%、0.0%: query_calendar_events(country=US,days=30,importance=high,medium) = 2026-08-12事件
- 美国8月12日10年期国债拍卖规模390亿美元、前次高收益率4.58%: query_calendar_events(country=US,days=30,importance=high,medium) = 2026-08-12事件
- 美国财政部8月11日至13日标售逾千亿美元国债: query_calendar_events(country=US,days=30,importance=high,medium) = 2026-08-10事件
- 澳洲联储现金利率前值/预测4.35%: query_calendar_events(country=AU,days=30,importance=high,medium) = 2026-08-11事件
- 伊朗寻求走出与美国“既非战争也非和平”僵局: query_raw_items(keyword=null,source=aljazeera,limit=50,status=null) = 2026-08-09新闻
- 俄罗斯称边境州遭乌克兰大规模无人机袭击、13人受伤: query_raw_items(keyword=null,source=telegram:Financial_Express,limit=50,status=null) = 2026-08-09新闻
- 汇丰及经济学家预期美国通胀年率略有放缓、核心分项可能降温: query_raw_items(keyword=CPI,source=telegram:Financial_Express,limit=50,status=null) = 2026-08-09新闻
- 美国CPI同比: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 3.5，数据日期2026-06-01（工具标记69天前，过时）
- 美联储资产负债表: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 6748567.0，数据日期2026-08-05

## 更新日志

| 日期 | 操作者 | 变更摘要 |
|------|--------|---------|
| 2026-08-09 13:22 | theme_publish | 更新（theme_update） |
| 2026-07-29 | 人类 | 创建 theme 骨架 |

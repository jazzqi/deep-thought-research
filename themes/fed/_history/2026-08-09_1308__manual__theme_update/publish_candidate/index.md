---
name: 美联储
slug: fed
status: active
lead_agent: soros
created: 2026-07-29
updated: 2026-08-09T13:25:50+08:00
revision: 2026-08-09
sources:
  - path: 2026-08-09_1308__manual__theme_update/reference.md
    agent: theme_update
    summarized: false
---

# 美联储

## Big Picture

美联储不是单一资产，而是全球金融体系的核心定价器：它通过联邦基金利率、资产负债表和政策沟通，影响美元流动性、国债收益率、企业融资成本与风险资产估值。当前主线并非“降息何时开始”这么简单，而是通胀仍高于目标、就业出现边际降温、财政持续发债，以及央行独立性风险同时作用于短端和长端利率。若通胀继续回落且就业恶化，Fed可以通过降息缓冲增长；若能源、关税和财政供给令通胀预期重新上行，降息将被迫后延，甚至重新讨论收紧。核心矛盾因此是：Fed能否在不重新点燃通胀预期、不损害政策信誉的前提下，转向宽松。对投资者而言，真正需要判断的不是一次会议或一次数据，而是名义增长、实际利率、财政融资与政策信用能否共同支持资产价格。

## 各维度分析

### 叙事/情绪面

（本轮无此维度内容）

### 基本面

本报告研究对象是美联储及其政策路径，不是上市公司或可交易公司股票，因此不存在公司营收、利润、资产负债表、PE估值或分析师一致预期等公司层面数据。当前工具也未提供可归属于某一公司标的的财报和估值对象。
同理，本轮新闻查询未返回可独立复核的Fed近期原始新闻条目，因此有关官员表态和政治压力的内容应区分为已有稿件中的报道线索，而非本轮重新核验的事实。相关缺口不能用宏观指标替代；如后续研究转向具体股票，应另行补充公司财务、估值、一致预期及公司新闻数据。

### 宏观背景

### 通胀仍高于目标是政策约束

最新可用美国CPI同比为3.5%，显著高于2%的目标；核心CPI同比最新预测为2.5%，前值为2.6%。若7月核心CPI环比为0.2%，这意味着环比动能较前值0.0%回升，而不是无条件地支持宽松。总CPI同比预测仍处于3.4%—3.5%，因此更准确的描述是“核心通胀可能改善，但总体通胀仍偏高”。
能源CPI同比前值为15.7%，说明能源分项仍是总通胀判断中的重要风险源。能源价格本身未必会导致Fed立即改变政策，但如果通过运输、商品成本和工资谈判形成二阶传导，核心通胀回落就可能中断。

### 通胀预期尚未回到支持激进宽松的水平

纽约联储7月调查的1年通胀预期前值为3.7%，3年通胀预期前值为3.3%。两者均高于2%目标，但它们是前值，而不是2026年8月10日即将公布的新数据，不能据此断言预期正在继续上升。它们只能说明，若Fed过早降息，仍面临通胀预期再次脱锚的风险。

### 需求尚未显示明显坍塌

7月零售销售日历预测为环比增长0.3%，前值为0.2%，实际值将在8月14日公布。预测不等于事实，但若消费保持韧性，Fed就没有必要仅因单月核心通胀改善而迅速转向；若零售销售显著低于预期，增长风险权重才会提高。

### 就业证据仍不完整

当前稿件引用的失业率4.1%、非农就业人数158,858、初请失业金199,000和续请失业金1,801,000，未能在本轮查询中重新获得完整指标来源，因此我们不把这些数字作为本次独立核验的核心事实。
当前仍缺少连续数月新增非农、工资增速、劳动参与率、职位空缺、工时及修正后的就业趋势。没有完整就业组合，不能严谨判断Fed是否已经面临“必须牺牲通胀控制来保护就业”的局面。7月成屋销售预测为年化407万户、环比降幅预测为0.7%，也只能作为住房需求的前瞻线索，不能替代完整就业与消费数据。

## 预测时间线

| 时间窗 | 预测 | 置信度 | 提出者 | 提出日期 | 验证 |
|--------|------|--------|--------|----------|------|
| （待添加） |  |  |  |  |  |

## 分歧地图

| 维度 | 观点 A | 观点 B | 分歧根因 |
|------|--------|--------|---------|
| （待添加） |  |  |  |

> **审查意见**：28 条（详见 _history/review/）

## 数据来源

- 美联储资产负债表: query_indicators(category=macro,country=us,time_range=24h) = 6748567.0，数据日2026-08-05
- 美国CPI同比百分比: query_indicators(category=macro,country=us,time_range=24h) = 3.5，数据日2026-06-01（工具标记数据较旧）
- 美国GDP: query_indicators(category=macro,country=us,time_range=24h) = 32475.21，数据日2026-04-01（工具标记过时）
- 美国7月CPI同比: query_calendar_events(country=US,days=30,importance=high,medium) = 前值3.5%，预测3.5%，发布日期2026-08-12
- 美国7月核心CPI同比: query_calendar_events(country=US,days=30,importance=high,medium) = 前值2.6%，预测2.5%，发布日期2026-08-12
- 美国7月CPI环比: query_calendar_events(country=US,days=30,importance=high,medium) = 前值-0.4%，预测0.2%，发布日期2026-08-12
- 美国7月核心CPI环比: query_calendar_events(country=US,days=30,importance=high,medium) = 前值0.0%，预测0.2%，发布日期2026-08-12
- 美国7月零售销售环比: query_calendar_events(country=US,days=30,importance=high,medium) = 前值0.2%，预测0.3%，发布日期2026-08-14
- Fed相关新闻: query_raw_items(keyword=Fed OR Federal Reserve OR Powell OR FOMC,limit=50) = No raw items found（新闻缺失，不代表事件不存在）
- 美国CPI同比事件映射候选: calendar_event_mapper(action=lookup,country=US,event_name=美国7月CPI年率未季调(%)) = cpi_yoy_us_pct等候选，尚未确认
- 美国核心CPI同比事件映射候选: calendar_event_mapper(action=lookup,country=US,event_name=美国7月核心CPI年率未季调(%)) = core_cpi等候选，但现有core_cpi为指数而非同比百分比，尚未确认

- 美国CPI同比: query_indicators({category:"macro",country:"us",time_range:"24h"}) = 3.5，数据日期2026-06-01，标记为69天前，非当前实时数据
- 美国核心CPI: query_indicators({category:"macro",country:"us",time_range:"24h"}) = 336.065，数据日期2026-06-01；该序列不是同比百分比，不能直接与2%目标比较
- 美联储资产负债表: query_indicators({category:"macro",country:"us",time_range:"24h"}) = 6748567，数据日期2026-08-05
- 美国7月核心CPI同比预测: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 2.5%，实际值未公布，事件日期2026-08-12
- 美国7月核心CPI环比预测: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 0.2%，实际值未公布，事件日期2026-08-12
- 美国7月CPI同比预测: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 3.4%与3.5%两条记录并存，实际值未公布，事件日期2026-08-12
- 纽约联储1年通胀预期前值: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 3.7%，实际值未公布，事件日期2026-08-10
- 纽约联储3年通胀预期前值: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 3.3%，实际值未公布，事件日期2026-08-10
- 美国财政部国债标售计划: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 2026-08-11至13日标售逾千亿美元国债
- 美国10年期国债竞拍: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 2026-08-12总金额390亿美元，前次中标/高收益率4.58%
- Fed相关新闻检索: query_raw_items({keyword:"Fed OR federal reserve OR Powell",limit:50}) = 未返回原始新闻，无法在本轮独立核验官员表态或政治干预事件

- 美国7月核心CPI同比预测: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 2.5%，前值2.6%，发布日期2026-08-12，实际值未公布
- 美国7月核心CPI环比预测: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 0.2%，前值0.0%，发布日期2026-08-12，实际值未公布
- 美国7月CPI同比预测: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 3.4%与3.5%两条记录并存，发布日期2026-08-12，实际值未公布
- 美国7月CPI环比预测: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 0.2%，前值-0.4%，发布日期2026-08-12，实际值未公布
- 美国7月零售销售环比预测: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 0.3%，前值0.2%，发布日期2026-08-14，实际值未公布
- 美国7月纽约联储1年通胀预期前值: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 3.7%，发布日期2026-08-10，实际值未公布
- 美国7月纽约联储3年通胀预期前值: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 3.3%，发布日期2026-08-10，实际值未公布
- 美国财政部国债标售计划: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 2026-08-11至13日标售逾千亿美元国债
- 美国10年期国债竞拍: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 2026-08-12总金额390亿美元，前次高收益率4.58%
- Fed官员鹰派表态: query_raw_items({keyword:"Fed",limit:50}) = 2026-08-05 Kashkari称开始逐步上调利率、Schmid称通胀过高需更紧政策（Hacker News条目）
- Fed独立性相关新闻: query_raw_items({keyword:"Fed",limit:50}) = 2026-08-08 Al Jazeera/NPR报道特朗普再次推动解雇Fed理事Lisa Cook
- Fed主席相关新闻: query_raw_items({keyword:"Fed",limit:50}) = 2026-08-06 Hacker News条目称特朗普频繁联系Fed主席Warsh；仅作新闻线索，未由官方来源独立确认

- 美国CPI同比：QueryIndicatorsTool(query_indicators, category=macro,country=us,time_range=24h) = 3.5，数据日期2026-06-01，工具标记滞后
- 美国核心CPI：QueryIndicatorsTool(query_indicators, category=macro,country=us,time_range=24h) = 336.065，数据日期2026-06-01
- 美联储资产负债表：QueryIndicatorsTool(query_indicators, category=macro,country=us,time_range=24h) = 6,748,567，数据日期2026-08-05
- 美国7月核心CPI同比：query_calendar_events(country=US,days=14,importance=high,medium) = 前值2.6%，预测2.5%，发布时间2026-08-12
- 美国7月核心CPI环比：query_calendar_events(country=US,days=14,importance=high,medium) = 前值0.0%，预测0.2%，发布时间2026-08-12
- 美国7月CPI同比：query_calendar_events(country=US,days=14,importance=high,medium) = 前值3.5%，预测3.4%/3.5%（记录不一致），发布时间2026-08-12
- 美国7月纽约联储1年通胀预期：query_calendar_events(country=US,days=14,importance=high,medium) = 前值3.7%，发布时间2026-08-10
- 美国7月纽约联储3年通胀预期：query_calendar_events(country=US,days=14,importance=high,medium) = 前值3.3%，发布时间2026-08-10
- 美国财政部8月11日至13日标售逾千亿美元国债：query_calendar_events(country=US,days=14,importance=high,medium) = 事件日历，发布时间/事件日期2026-08-10至13
- 美国8月12日10年期国债竞拍：query_calendar_events(country=US,days=14,importance=high,medium) = 总金额390亿美元，前次高收益率4.58%


- 美国未来30日高重要性事件清单: query_calendar_events({country:"US",days:30,importance:"high,medium",limit:100}) = 2026-08-11至13日财政部标售逾千亿美元国债；2026-08-12核心CPI同比预测2.5%、环比预测0.2%、总CPI同比预测3.4%与3.5%两条记录；2026-08-12十年期国债竞拍390亿美元、前次高收益率4.58%；2026-08-13 PPI同比前值5.5%、核心PPI同比前值4.7%；2026-08-14零售销售环比预测0.3%
- 美国7月CPI与10年期国债竞拍待发布数据: query_calendar_events({country:"US",days:30,importance:"high,medium"}) = 实际值均未公布，不能作为已实现事实
- Fed近期原始新闻检索: query_raw_items({keyword:"Fed OR Federal Reserve OR Powell OR Cook OR Warsh",limit:50,source:null,status:null}) = No raw items found；缺失不等于相关事件未发生，本文仅将既有稿件中的新闻作为待复核线索

- 美国资产负债表: query_indicators({"category":"monetary_credit","country":"us","limit":50,"time_range":"24h"}) = 本次未返回指标；前次可用值仍为6,748,567.0（数据日2026-08-05）
- 2026-08-08特朗普再次推动解雇Fed理事Lisa Cook: query_raw_items({"keyword":"Lisa Cook","limit":30,"source":null,"status":null}) = Al Jazeera/NPR条目，确有近期报道；同一查询还返回2026-06-29最高法院裁决暂不允许解雇Cook的条目
- 2026-08-05 Kashkari称现在是开始逐步上调利率的时候: query_raw_items({"keyword":"Kashkari","limit":30,"source":null,"status":null}) = Hacker News条目
- 2026-08-05 Schmid称通胀过高、需要更紧政策: query_raw_items({"keyword":"Schmid","limit":30,"source":null,"status":null}) = Hacker News条目
- 2026-08-06特朗普在Warsh成为Fed主席后多次联系他: query_raw_items({"keyword":"Warsh","limit":30,"source":null,"status":null}) = Hacker News条目；仅为转引新闻，未由官方来源确认
- 2026-08-07美国7月就业意外减少: query_raw_items({"keyword":"rate","limit":30,"source":"fed_rss","status":null}) = 本次指定fed_rss查询未返回该条；不得将搜索结果标题作为独立确认事实
- 美国宏观指标快照: query_indicators({"category":"macro","country":"us","limit":50,"time_range":"24h"}) = CPI同比3.5（数据日2026-06-01，69天前）；Fed资产负债表6,748,567（数据日2026-08-05）；GDP 32,475.21（数据日2026-04-01，工具标记过时）；核心CPI 336.065（指数，非同比百分比）

## 更新日志

| 日期 | 操作者 | 变更摘要 |
|------|--------|---------|
| 2026-08-09 13:25 | theme_publish | 更新（theme_update） |
| 2026-07-29 | 人类 | 创建 theme 骨架 |

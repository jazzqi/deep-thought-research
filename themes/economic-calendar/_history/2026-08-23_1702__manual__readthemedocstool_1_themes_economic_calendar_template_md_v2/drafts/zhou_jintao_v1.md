Now I'll compile and write the complete economic calendar forecast report based on all the data I've gathered. Let me first save the reference data, then write the full report.<tool_call>
<function=write_theme_docs_tool>
<parameter=path>themes/economic-calendar/_history/2026-08-23_1702__manual__readthemedocstool_1_themes_economic_calendar_template_md_v2/drafts/reference.md</parameter>
<parameter=content># Data Sources & Reference (周度财经日历 Forecast 2026-08-25 ~ 08-29)

> 本文件为报告溯源库；每条数据标注来源工具、查询参数与返回值。
> 维护规则：写入报告的每个数字/事实必须能追溯至此文件的某一行。

---

## Fed & Monetary Policy

- 美联储联邦基金利率目标区间: FOMC (2026-07-28) = 3.50-3.75% [query_fomc]
- FOMC 9月会议日期: 2026-09-15~16 (SEP会议) [query_fomc]
- FOMC 10月会议日期: 2026-10-27~28 [query_fomc]
- FOMC 7月会议纪要核心信息: "Several Fed officials favored a rate hike last month and many indicated policy tightening would be necessary if inflation didn't decline" [id:132467] query_raw_items(keyword:'Fed minutes OR rate hike')
- Kevin Warsh 将在 Jackson Hole 8/29 发表就任 Fed Chair 后首次演讲 [id:135539] query_raw_items(keyword:'Warsh Jackson')
- Mary Daly: "Bond market showing trust in Fed's policy positioning" [id:135028] query_raw_items(keyword:'Daly bond market')
- 道明证券: "美国长期国债收益率目前颇具吸引力，但投资者信心不足，短期收益率可能继续承压" [id:133326] query_raw_items(keyword:'DXY treasury')
- Bessent 试图遏制债券市场压力 (bond vigilantes) [id:134512] query_raw_items(keyword:'Bessent bond')

## US Economic Data (Last Week Released)

- 7月新屋开工(万户): actual=123.9, forecast=134.5, previous=142.7 [query_calendar_events lookback 14d]
- 7月新屋开工环比: actual=-12.4%, forecast=-5.9%, previous=19.0%
- 7月营建许可(万户): actual=144.3, forecast=137.5, previous=137.4
- 7月进口价格指数同比: actual=5.9%, forecast=6.7%, previous=7.1%
- 7月进口价格指数环比: actual=-0.4%, forecast=0.1%, previous=0.3%
- 8月纽约联储制造业指数: actual=20.6, forecast=10.0, previous=15.6
- 8月NAHB房产市场指数: actual=35.0, forecast=33.0, previous=34.0
- 7月工业产出环比: actual=0.2%, forecast=0.3%, previous=0.1%
- 7月制造业产出环比: actual=0.2%, forecast=0.2%, previous=0.0%
- 7月成屋签约销售环比: actual=-2.3%, forecast=0.0%, previous=-5.4%
- 6月国际资本净流入(亿美元): actual=1335, previous=1322
- 6月长期资本净流入(亿美元): actual=1727, previous=2327

## Japan Economic Data (Released)

- Q2实际GDP年化季环比初值: actual=1.1%, forecast=2.1%, previous=1.8% — 大幅不及预期
- Q2实际GDP季环比初值: actual=0.3%, forecast=0.5%, previous=0.5%
- Q2名义GDP季环比初值: actual=1.2%, forecast=1.2%, previous=0.6%
- Q2 GDP平减指数同比: actual=2.6%, forecast=2.3%, previous=3.2%
- 6月工业产出环比终值: actual=1.9%, previous=1.3%
- 6月核心机械订单环比: actual=9.7%, forecast=7.2%, previous=-12.4%

## China Economic Data (Released)

- 1-7月城镇固定资产投资同比: actual=-6.7%, previous=-5.7% — 进一步恶化
- 1-7月社会消费品零售总额同比: actual=1.2%, previous=1.3%
- 7月社会消费品零售总额同比: actual=0.6%, previous=1.0% — 显著放缓
- 7月规模以上工业增加值同比: actual=4.5%, previous=5.3% — 大幅下滑
- 1-7月规模以上工业增加值同比: actual=5.3%, previous=5.4%
- 7月城镇调查失业率: actual=5.2%, previous=5.0% — 就业恶化
- 1-7月全国房地产开发投资: actual=-19.2%, previous=-18.0% — 房地产继续深化

## Europe Economic Data (Released)

- 德国8月ZEW经济景气指数: actual=34.2, forecast=30.0, previous=26.3
- 德国8月ZEW经济现况指数: actual=-61.1, forecast=-69.3, previous=-77.6
- 欧元区8月ZEW经济景气指数: actual=31.4, previous=23.4
- 欧元区7月调和CPI同比终值: actual=2.9%, forecast=2.9%, previous=2.9%
- 欧元区7月核心调和CPI同比终值: actual=2.5%, forecast=2.5%, previous=2.5%

## UK Economic Data (Released)

- 7月CPI同比: actual=2.9%, forecast=2.9%, previous=2.6%
- 7月核心CPI同比: actual=2.6%, forecast=2.5%, previous=2.6%
- 6月三个月ILO失业率: actual=4.9%, forecast=4.8%, previous=4.9%
- 6月三个月ILO就业人数变动(万人): actual=8.4, forecast=13.0, previous=14.8
- 7月失业率(ILO): actual=4.3%, previous=4.4%

## Trade & Geopolitical

- 美国对加拿大部分产品加征50%关税 (约200亿美元) [query_calendar_events]
- 加拿大总理Carney宣布9月8日起对美国实施报复性关税, "dollar for dollar" [id:135532] query_raw_items
- 加拿大将对美国钢铁、电子产品等加征关税 [id:135565] query_raw_items
- 特朗普宣布将对伊朗实施"前所未见"的措施 [query_calendar_events]
- 伊朗警告加入美国"经济战争"的国家将遭报复 [id:135556] query_raw_items
- 伊拉克油轮获伊朗许可通过霍尔木兹海峡 [id:135541] query_raw_items
- 美国国债突破40万亿美元大关 [id:132632] query_raw_items
- 瑞士与中国达成贸易协议, 几乎完全取消关税 [id:135295] query_raw_items

## Corporate Events

- NVIDIA: 8月26日盘后公布Q2 FY2027财报 [query_calendar_events]
- NVIDIA: 披露210亿美元SpaceX持股 [id:128533] query_raw_items
- OpenAI DevDay 2026: 8月28日 [query_calendar_events]
- 阿里巴巴: 8月20日财报及电话会 [query_calendar_events]
- 小米: 8月18日财报及电话会 [query_calendar_events]
- 百度: 8月18日财报及电话会 [query_calendar_events]
- 快手: 8月19日财报及电话会 [query_calendar_events]
- 泡泡玛特: 8月19日中报及董事会会议 [query_calendar_events]

## Market Indicators

- 美元指数 DXY: 约98.708 (从 raw items id:133744 荷兰国际报告获取, 8月20日附近)
- 美联储资产负债表: 6,759,955百万美元 (2026-08-12) [query_indicators fed_balance_sheet]
- US CPI YoY: 3.4% (2026-07-01) [query_indicators]
- US Core CPI: 336.789 index (2026-07-01) [query_indicators]
- US PPI: 284.057 index (2026-07-01) [query_indicators]
- US Consumer Confidence: 49.5 (2026-06-01, ⚠️ 过时83天) [query_indicators]

## 本周前瞻数据 (待发布, 含前值/预测)

- 8月25日 14:00 🇺🇸 8月消费者信心指数: previous=90.8, forecast=90.2
- 8月25日 14:00 🇺🇸 7月新屋销售(万户): previous=62.8, forecast=61.8
- 8月26日 12:30 🇺🇸 Q2 GDP年化季环比修正值: previous=1.5, forecast=1.5
- 8月26日 12:30 🇺🇸 Q2 PCE物价指数年化季环比修正值: previous=3.4
- 8月26日 12:30 🇺🇸 7月核心PCE同比: previous=3.3, forecast=3.3
- 8月26日 12:30 🇺🇸 7月核心PCE环比: previous=0.1, forecast=0.2
- 8月26日 12:30 🇺🇸 7月PCE同比: previous=3.7, forecast=3.6
- 8月27日 12:30 🇺🇸 7月商品贸易帐(亿美元): previous=-1015, forecast=-997
- 8月27日 12:30 🇺🇸 8月22日当周首请失业金: previous=无
- 8月27日 23:30 🇯🇵 8月东京CPI同比: previous=2.0
- 8月28日 13:45 🇺🇸 8月芝加哥PMI: previous=57.6
- 8月28日 14:00 🇺🇸 8月密歇根消费者信心终值: previous=51.0
</parameter>
<parameter=overwrite>True</parameter>
</function>
</tool_call>
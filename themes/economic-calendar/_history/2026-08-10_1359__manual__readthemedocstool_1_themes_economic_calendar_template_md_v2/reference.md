- 美国10年期国债收益率: query_indicators(category=null,country=us,time_range=24h) = 4.69%（OpenBB，数据日2026-08-06）
- 美国2年期国债收益率: query_indicators(category=null,country=us,time_range=24h) = 4.25%（OpenBB，数据日2026-08-06）
- SPY: market_quote(symbols=[SPY.US,GLD.US]) = 773.26美元，较前收+0.61%
- GLD: market_quote(symbols=[SPY.US,GLD.US]) = 398.47美元，较前收+2.26%
- 美元兑人民币: query_indicators(category=exchange_rate,country=null,time_range=24h) = 6.7467（akshare，指标usd_cny；非CNH）
- 原油: query_indicators(category=commodity,country=null,time_range=7d) = 81.96美元/桶（OpenBB，数据日2026-08-03；品种未明确且时效较弱）
- 未来14天全球日历: query_calendar_events(days=14,importance=high,medium,country=null) = 美国7月CPI/PPI/零售销售、美国国债标售、澳洲联储、英国GDP、欧元区工业生产/GDP、日本GDP等，字段以前值/共识原样返回
- 霍尔木兹风险: query_raw_items(keyword=Hormuz,limit=20) = 2026-08-10 Al Jazeera报道伊朗要求令前景不明、油价上涨；多来源显示通航安排未确认
- 美联储治理/政策新闻: query_raw_items(keyword=Fed,limit=20) = 2026-08-08多来源报道特朗普再次推动解除理事Lisa Cook职务；该新闻未经本报告进一步法律状态核验

- 下周高重要性日历：query_calendar_events(days=14, importance=high, country='') = 美国财政部8月11—13日标售逾千亿美元国债；澳洲联储8月11日决议；美国8月8日当周初请失业金8月13日（前值/共识未返回）；美国7月零售销售环比8月14日（前值+0.2%，共识+0.3%）。
- 下周中重要性美国通胀日历：query_calendar_events(days=14, importance=medium, country='') = 8月12日美国7月核心CPI同比前值2.6%、共识2.5%；核心CPI环比前值0.0%、共识+0.2%；CPI环比前值-0.4%、共识+0.2%；美国CPI同比条目共识出现3.4%与3.5%两种记录，须在报告中按条目披露并标注口径冲突；8月13日核心PPI环比前值+0.2%、共识+0.3%，PPI环比前值-0.3%、共识+0.2%。
- 霍尔木兹状态：query_raw_items(keyword='Hormuz', limit=20) = 2026-08-08至10日Al Jazeera、BBC、NYT、NPR报道谈判与伊朗要求并存，且有油轮遇袭/船员风险报道；不能视为通航已获确认。
- 上周承接与成绩单：ReadThemeDocsTool(themes/economic-calendar/2026-08-03__2026-08-09/recap.md) = 7月非农-2.3万人、霍尔木兹谈判进展但实际机制未确认；上期为冷启动，累计预测命中率数据不足，不能据此量化校准置信度。

- 2026年8月11-13日美国财政部标售逾千亿美元国债：query_calendar_events({days:14,importance:'high,medium',country:null}) = 事件列示，未提供本次共识
- 2026年8月12日美国10年期国债竞拍规模390亿美元、前次中标收益率4.58%：query_calendar_events({days:14,importance:'high,medium',country:null}) = previous 4.58, total 390.0
- 美国7月CPI同比前值3.5%、预测3.4%；核心CPI同比前值2.6%、预测2.5%；总体环比前值-0.4%、预测0.2%；核心环比前值0.0%、预测0.2%：query_calendar_events({days:14,importance:'high,medium',country:null}) = US CPI entries
- 美国7月PPI同比前值5.5%、核心PPI同比前值4.7%；总体PPI环比前值-0.3%、预测0.2%；核心PPI环比前值0.2%、预测0.3%：query_calendar_events({days:14,importance:'high,medium',country:null}) = US PPI entries
- 澳洲联储政策利率前值4.35%、预测4.35%：query_calendar_events({days:14,importance:'high,medium',country:null}) = AU policy rate entry
- 英国二季度GDP季环比前值0.6%、同比前值0.9%；英国6月GDP月率前值0.1%；6月工业产出环比-0.5%、同比1.0%：query_calendar_events({days:14,importance:'high,medium',country:null}) = GB entries
- 欧元区6月工业产出环比前值-0.2%、同比-1.2%：query_calendar_events({days:14,importance:'high,medium',country:null}) = EU entries
- 美国联储资产负债表2026-08-05为6,748,567百万美元：query_indicators({category:'macro',country:'us',time_range:'7d'}) = fed_balance_sheet 6748567.0
- 2026年8月10日阿布扎比国家石油公司天然气部门CEO称正在研究替代路线但无法进一步置评：query_raw_items({keyword:null,limit:30,source:null,status:null}) = telegram:Financial_Express item
- 2026年8月8-10日霍尔木兹相关谈判/通航与油价风险信息：query_raw_items({keyword:null,limit:30,source:null,status:null}) = 当前返回的实时新闻未提供足够可核实细节，正文仅作已知未知，不将通航恢复写为事实
- 美国市场10Y/2Y、DXY、S&P500、Brent、Gold、USDCNH当前数值：query_indicators({category:'market',country:'us',time_range:'24h'}) = 未返回有效指标，报告不臆造

- 2026-08-10至2026-08-24未来经济日历事件及前值/预测字段: query_calendar_events(country=null, days=14, importance=high,medium, limit=100) = 返回215条匹配事件；重点包括美国7月CPI（前值3.5%、预测字段存在3.4%与3.5%冲突；核心同比前值2.6%、预测2.5%；总体环比前值-0.4%、预测0.2%；核心环比前值0.0%、预测0.2%）、美国7月PPI（同比前值5.5%、核心同比4.7%、环比预测0.2%、核心环比前值0.2%/预测0.3%）、澳洲联储政策利率前值/预测4.35%、美国10年期国债拍卖前次中标收益率4.58%及规模390亿美元、英国二季度GDP前值季率0.6%/同比0.9%、欧元区6月工业产出前值环比-0.2%/同比-1.2%、日本7月企业商品价格同比前值7.1%/环比0.4%、法国7月CPI同比终值前值2.1%。
- 2026-08-10近期新闻扫描: query_raw_items(keyword=null, limit=30, source=null, status=null) = Financial Express条目显示阿布扎比国家石油公司管理层称持续监控霍尔木兹局势、研究替代路线但未提供进一步说明；欧洲股指期货小幅走弱；未发现可核实的霍尔木兹通航执行证据。

- 2026年8月11—13日美国财政部标售逾千亿美元国债: query_calendar_events(country=US,days=14,importance=high,medium,limit=200) = upcoming event
- 2026年8月12日美国7月CPI同比: query_calendar_events(country=US,days=14,importance=high,medium,limit=200) = 前值3.5%，预测字段3.4%及3.5%并存
- 2026年8月12日美国7月核心CPI同比/环比: query_calendar_events(country=US,days=14,importance=high,medium,limit=200) = 前值2.6%/0.0%，预测2.5%/0.2%
- 2026年8月12日美国7月CPI环比: query_calendar_events(country=US,days=14,importance=high,medium,limit=200) = 前值-0.4%，预测0.2%
- 2026年8月12日美国10年期国债拍卖: query_calendar_events(country=US,days=14,importance=high,medium,limit=200) = 前次高收益率4.58%，规模390亿美元，本次共识缺失
- 2026年8月13日美国7月PPI/核心PPI环比: query_calendar_events(country=US,days=14,importance=high,medium,limit=200) = 前值-0.3%/0.2%，预测0.2%/0.3%
- 2026年8月14日美国7月零售销售: query_calendar_events(country=US,days=14,importance=high,medium,limit=200) = 环比前值0.2%、预测0.3%；除汽车与汽油环比前值0.4%、预测0.3%；控制组前值0.5%、预测缺失
- 2026年8月14日美国8月密歇根大学消费者信心初值: query_calendar_events(country=US,days=14,importance=high,medium,limit=200) = 前值55.2，预测53.8
- 2026年8月11日澳洲联储政策利率: query_calendar_events(country=null,days=14,importance=high,medium,limit=80) = 前值4.35%，预测4.35%
- 2026年8月13日英国二季度GDP及6月工业产出: query_calendar_events(country=null,days=14,importance=high,medium,limit=80) = GDP季环比前值0.6%、同比0.9%，6月GDP环比0.1%、工业产出环比-0.5%，共识缺失
- 2026年8月13日欧元区6月工业产出: query_calendar_events(country=null,days=14,importance=high,medium,limit=80) = 环比前值-0.2%、同比-1.2%，共识缺失
- 2026年8月12日日本7月国内企业商品物价指数: query_calendar_events(country=null,days=14,importance=high,medium,limit=80) = 同比前值7.1%、环比0.4%，共识缺失
- 2026年8月12日美国EIA库存: query_calendar_events(country=US,days=14,importance=high,medium,limit=200) = 原油前值增加247.9万桶、汽油-164.3万桶、精炼油-347.3万桶，共识缺失
- 2026年8月8—10日霍尔木兹相关新闻: query_raw_items(keyword=Hormuz,limit=20,source=telegram:Financial_Express,status=processed) = Al Jazeera报道油价上升且伊朗诉求令海峡前景不明；BBC报道谈判积极但伊朗称协议未必开放海峡；无可核验通航恢复数据
- 美国宏观数据库最新可用CPI同比: query_indicators(category=macro,country=us,time_range=24h,limit=20) = 3.5%，数据期2026-06-01，已过70天，不作为当前读数

- 2026-08-08至2026-08-10霍尔木兹风险的独立新闻核验: query_raw_items(keyword=Hormuz, limit=30, source=null, status=null) = Al Jazeera（8月8日）报道阿联酋称伊朗袭击ADNOC油轮（无人伤亡）；NPR（8月8日）称油轮船员仍面临危险；BBC（8月8日）称谈判积极但伊朗警告协议未必开放海峡；Al Jazeera（8月10日）称伊朗诉求令前景不明且油价上涨。

- 2026-08-10 近期新闻：市场定价显示美联储2026年9月加息25个基点概率约44.4%: query_raw_items({"keyword":"美联储","limit":30,"source":null,"status":null}) = telegram:Financial_Express，发布时间2026-08-09 21:58:31 UTC
- 2026-08-07 近期新闻：美国7月就业超预期萎缩，美联储面临政策难题: query_raw_items({"keyword":"美联储","limit":30,"source":null,"status":null}) = blockbeats，发布时间2026-08-07 13:06:16 UTC
- 2026-08-07 近期新闻：特朗普继续推进解雇美联储理事库克的尝试: query_raw_items({"keyword":"美联储","limit":30,"source":null,"status":null}) = blockbeats，发布时间2026-08-07 17:06:16 UTC
- 2026-08-06 近期新闻：美联储戴利表示若通胀压力再度加剧，可能需要激进利率应对: query_raw_items({"keyword":"美联储","limit":30,"source":null,"status":null}) = blockbeats，发布时间2026-08-06 01:36:18 UTC
- 2026-08-09 中国7月CPI同比0.5%，低于预期0.8%和前值1.0%；PPI同比-3.5%，低于预期-3.8%和前值-4.1%: query_raw_items({"keyword":"CPI","limit":30,"source":null,"status":null}) = telegram:Financial_Express，发布时间2026-08-09 01:33:23 UTC
- 2026-08-09 汇丰前瞻美国7月CPI，预计多项核心通胀分项低于市场预期: query_raw_items({"keyword":"CPI","limit":30,"source":null,"status":null}) = telegram:Financial_Express，发布时间2026-08-09 04:43:49 UTC

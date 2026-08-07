- 美国核心CPI指数（2026-06-01，非同比/环比口径未在返回中说明）: query_indicators(category=macro,country=us,time_range=7d) = 336.065
- 美国联储资产负债表（2026-07-29）: query_indicators(category=macro,country=us,time_range=7d) = 6,738,190.0
- 新闻称市场聚焦美国7月失业率与非农就业（抓取时间2026-08-07）: query_raw_items(source=null,status=processed,limit=50) = blockbeats《预告：市场聚焦今晚美国7月失业率和非农数据，机构前瞻一览》

- 中国制造业PMI（2026年7月）: query_indicators({category:'pmi',country:'china',time_range:'7d',limit:10}) = 49.2
- 中国非制造业PMI（2026年7月）: query_indicators({category:'pmi',country:'china',time_range:'7d',limit:10}) = 49.0
- 美国核心CPI指数（数据日期2026-06-01，发布距查询日67天）: query_indicators({category:'macro',country:'us',time_range:'7d',limit:20}) = 336.065；该值非同比率，不能直接替代7月核心CPI
- 美国联储资产负债表（数据日期2026-07-29）: query_indicators({category:'macro',country:'us',time_range:'7d',limit:20}) = 6,738,190.0（数据库单位未说明，未用于情景数值）
- 最新原始新闻条目未提供可核验的下周美国/中国宏观日历共识: query_raw_items({limit:20,status:null,source:null}) = 未返回相关宏观事件

- 中国制造业PMI（2026年7月）: query_indicators(category=pmi,country=china,limit=10,time_range=7d) = 49.2
- 中国非制造业PMI（2026年7月）: query_indicators(category=pmi,country=china,limit=10,time_range=7d) = 49.0
- 美国核心CPI指数（数据日期2026-06-01；非同比/环比口径）: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 336.065；不能替代美国2026年7月核心CPI
- 美国联储资产负债表（数据日期2026-07-29）: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 6,738,190.0；数据库单位未说明，未用于预测
- 原始新闻：市场聚焦美国2026年7月失业率与非农数据: query_raw_items(limit=30,status=processed,source=null) = blockbeats，抓取时间2026-08-07；仅作为当前周背景，不替代下周日历

- 中国制造业PMI（2026年7月）: query_indicators(category='pmi',country='china',limit=20,time_range='24h') = 49.2
- 中国非制造业PMI（2026年7月）: query_indicators(category='pmi',country='china',limit=20,time_range='24h') = 49.0
- 原始新闻流（查询时点2026-08-07）: query_raw_items(limit=30,source=null,status='processed') = 含BlockBeats《预告：市场聚焦今晚美国7月失业率和非农数据，机构前瞻一览》；未返回可核验的下周美国/中国宏观日历前值或市场一致预期

- 中国2026年7月制造业PMI: query_indicators(category="pmi", country="china", time_range="24h") = 49.2（数据期：2026年7月）
- 中国2026年7月非制造业PMI: query_indicators(category="pmi", country="china", time_range="24h") = 49.0（数据期：2026年7月）
- 2026-08-10—16财经日历已返回项目（日本经常账户、欧元区Sentix、美国Conference Board就业趋势指数及国债拍卖等）: query_longbridge_by_route(path="calendar/economic", params={"category":"macrodata","start_date":"2026-08-10","end_date":"2026-08-16","force_refresh":true}) = 见路由返回；例如欧元区Sentix前值-3.1、美国ETI前值106.69

- 财经日历（2026-08-10至2026-08-16，宏观数据）: query_longbridge_by_route(path="calendar/economic", params={"category":"macrodata","start_date":"2026-08-10","end_date":"2026-08-16","force_refresh":true}) = 返回日本经常账户/银行贷款/经济观察家调查、欧元区Sentix（前值-3.1）、美国Conference Board就业趋势指数ETI（前值106.69）及美国13/26周国库券拍卖等；返回列表未包含美国7月CPI、PPI、零售销售、中国7月CPI/PPI/社融/工业增加值/社零/固定资产投资、英国二季度GDP或密歇根调查
- 中国2026年7月制造业PMI: query_indicators(category="pmi",country="china",limit=20,time_range="7d") = 49.2
- 中国2026年7月非制造业PMI: query_indicators(category="pmi",country="china",limit=20,time_range="7d") = 49.0
- 美国核心CPI指数（数据期2026-06-01，非同比/环比口径）: query_indicators(category="macro",country="us",limit=30,time_range="7d") = 336.065；不能替代7月核心CPI
- 原始新闻条目: query_raw_items(limit=50,source=null,status=null) = 2026-08-07含BlockBeats《预告：市场聚焦今晚美国7月失业率和非农数据，机构前瞻一览》，未提供下周上述宏观事件的可核验前值/一致预期

- 美国核心CPI指数: query_indicators({"category":"macro","country":"us","limit":30,"time_range":"7d"}) = 336.065（数据日期2026-06-01；工具标记距审查日67天）
- 美国联储资产负债表: query_indicators({"category":"macro","country":"us","limit":30,"time_range":"7d"}) = 6738190.0（数据日期2026-07-29）
- 中国宏观指标查询结果: query_indicators({"category":"macro","country":"china","limit":30,"time_range":"7d"}) = 0 indicators（未返回可核验数值）
- 原始新闻流中“市场聚焦今晚美国7月失业率和非农数据”: query_raw_items({"limit":80,"source":null,"status":null}) = 标题存在，来源blockbeats，采集时间2026-08-07 06:36:16 UTC

- 2026-08-10—16财经日历实际返回项目: query_longbridge_by_route(path="calendar/economic", params={"category":"macrodata","start_date":"2026-08-10","end_date":"2026-08-16","force_refresh":true}) = 日本经常账户/银行贷款/经济观察家调查、欧元区Sentix（前值-3.1）、美国Conference Board就业趋势指数ETI（前值106.69）、美国13/26周国库券拍卖等；返回未包含稿件列出的美国7月CPI、PPI、零售销售、中国7月CPI/PPI/社融/工业增加值/社零/固定资产投资、英国二季度GDP或密歇根调查。
- 中国2026年7月制造业PMI: query_indicators(category="pmi",country="china",limit=30,time_range="7d") = 49.2
- 中国2026年7月非制造业PMI: query_indicators(category="pmi",country="china",limit=30,time_range="7d") = 49.0
- 美国核心CPI指数（数据日期2026-06-01，工具未说明同比/环比）: query_indicators(category="macro",country="us",limit=30,time_range="7d") = 336.065；不能替代7月核心CPI。
- 美国联储资产负债表（数据日期2026-07-29）: query_indicators(category="macro",country="us",limit=30,time_range="7d") = 6738190.0。
- 原始新闻背景: query_raw_items(limit=50,source=null,status=null) = BlockBeats《预告：市场聚焦今晚美国7月失业率和非农数据》，采集时间2026-08-07 06:36 UTC；未提供下周事件的可核验一致预期。

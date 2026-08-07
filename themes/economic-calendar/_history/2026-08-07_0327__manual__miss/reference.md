- 美国核心CPI指数: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 336.065（数据日2026-06-01；工具标记超过90天规则下未过时但距当前有时滞）
- 美国联邦储备系统资产负债表: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 6,738,190（数据日2026-07-29）
- 美国GDP: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 32,475.21（数据日2026-04-01；工具标记超过90天，本文不用于当前判断）
- 中国宏观指标: query_indicators(category=macro,country=china,limit=20,time_range=7d) = 未返回有效指标
- 最新原始新闻: query_raw_items(limit=30,source=null,status=null) = 返回内容主要为Hacker News，未提供可独立确认的本周财经日历或宏观政策新闻

- 美国核心CPI指数: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 336.065（数据日2026-06-01，距查询日66天）
- 美国联邦储备系统资产负债表: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 6,738,190（数据日2026-07-29，距查询日8天）
- 中国宏观指标: query_indicators(category=macro,country=china,limit=20,time_range=7d) = 返回20条快照但0项有效指标
- 最新原始新闻: query_raw_items(limit=30,source=null,status=processed) = 30条均为Hacker News内容，未提供可独立确认的宏观政策、财经日历或标的重大新闻

- 美国7月CPI公布窗口及预期：QueryLongbridgeByRouteTool(calendar/economic, {"category":"macrodata","start_date":"2026-08-12","end_date":"2026-08-12","force_refresh":true}) = 2026-08-12 12:30 UTC；CPI同比前值3.5%、预期3.4%，核心CPI环比前值0.0%、预期0.2%，核心CPI同比前值2.6%、预期2.5%
- 美国7月PPI公布窗口及预期：QueryLongbridgeByRouteTool(calendar/economic, {"category":"macrodata","start_date":"2026-08-13","end_date":"2026-08-13","force_refresh":true}) = 2026-08-13 12:30 UTC；最终需求PPI环比前值-0.3%、预期0.1%，核心（除食品能源）环比前值0.2%、预期0.2%
- 美国7月零售销售和密歇根大学初值窗口：QueryLongbridgeByRouteTool(calendar/economic, {"category":"macrodata","start_date":"2026-08-14","end_date":"2026-08-14","force_refresh":true}) = 均为2026-08-14，零售销售12:30 UTC、密歇根大学14:00 UTC；零售销售环比前值0.2%，控制组前值0.5%，密歇根总指数前值55.2、一年通胀预期前值4.2%
- 欧元区GDP、就业和贸易窗口：QueryLongbridgeByRouteTool(calendar/economic, {"category":"macrodata","start_date":"2026-08-14","end_date":"2026-08-14","force_refresh":true}) = 2026-08-14 09:00 UTC；GDP环比前值/预期均0.4%、同比前值/预期均1.0%，就业环比前值0.1%、同比前值0.5%
- 中国实体、信贷和货币数据窗口及部分预期：QueryLongbridgeByRouteTool(calendar/economic, {"category":"macrodata","start_date":"2026-08-15","end_date":"2026-08-15","force_refresh":true}) = 2026-08-17 02:00 UTC公布零售、固投、工业、失业率；17日08:00 UTC公布社融、信贷、M2。零售同比前值1.0%、预期1.8%，固投同比前值-5.7%、预期-6.0%，社融前值3360、预期1210，新贷款前值1610、预期50，M2同比前值8.0%、预期7.9%
- 美国流动性和核心价格背景：QueryIndicatorsTool(inflation/macro, country=us, time_range=24h) = 核心CPI指数336.065（数据日2026-06-01）；美联储资产负债表6,738,190（数据日2026-07-29）；GDP 32,475.21（数据日2026-04-01，已标记陈旧）

- 美国核心CPI指数: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 336.065（数据日2026-06-01）
- 美国联邦储备系统资产负债表: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 6,738,190（数据日2026-07-29）
- 美国GDP: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 32,475.21（数据日2026-04-01；工具标记过时，不用于当前判断）
- 中国宏观指标: query_indicators(category=macro,country=china,limit=20,time_range=7d) = 返回20条快照但0项有效指标
- 最新原始新闻: query_raw_items(limit=50,source=null,status=null) = 结果主要为Hacker News，未提供可独立确认的财经宏观新闻
- 2026-08-09至2026-08-17经济日历: query_longbridge_by_route(calendar/economic,{"category":"macrodata","start_date":"2026-08-10","end_date":"2026-08-16","force_refresh":true}) = 查询返回日本经常账户/贷款、日本经济观察家调查、欧元区sentix、美国ETI及国债拍卖等；未在该响应中返回美国CPI或零售销售
- 美国PPI（2026-08-13 12:30 UTC）: query_longbridge_by_route(calendar/economic,{"category":"macrodata","start_date":"2026-08-13","end_date":"2026-08-13","force_refresh":true}) = 最终需求PPI环比前值-0.3%、预期0.1%；核心（除食品能源）环比前值0.2%、预期0.2%
- 欧元区GDP/就业（2026-08-14 09:00 UTC）: query_longbridge_by_route(calendar/economic,{"category":"macrodata","start_date":"2026-08-14","end_date":"2026-08-14","force_refresh":true}) = GDP环比前值/预期0.4%、同比前值/预期1.0%；就业环比前值0.1%、同比前值0.5%
- 美国零售销售/密歇根调查（2026-08-14）: query_longbridge_by_route(calendar/economic,{"category":"macrodata","start_date":"2026-08-14","end_date":"2026-08-14","force_refresh":true}) = 零售销售环比前值0.2%、控制组前值0.5%；密歇根总指数前值55.2、一年通胀预期前值4.2%
- 中国实体与信贷数据（2026-08-17）: query_longbridge_by_route(calendar/economic,{"category":"macrodata","start_date":"2026-08-17","end_date":"2026-08-17","force_refresh":true}) = 零售同比前值1%、预期1.8%；固投同比前值-5.7%、预期-6%；工业同比前值5.4%；社融前值3360、预期1210；新贷款前值1610、预期50；M2同比前值8%、预期7.9%

- 美国核心CPI指数336.065（数据日2026-06-01，标记为非90天陈旧）: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 336.065
- 美国联邦储备系统资产负债表6738190.0（数据日2026-07-29）: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 6738190.0
- 美国GDP快照32475.21（数据日2026-04-01，工具标记超过90天陈旧）: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 32475.21
- 中国宏观查询返回20条快照但0个指标: query_indicators({"category":"macro","country":"china","limit":20,"time_range":"7d"}) = 0 indicators
- 美国货币/信用查询返回3条快照但0个指标: query_indicators({"category":"monetary_credit","country":"us","limit":20,"time_range":"7d"}) = 0 indicators
- 美国通胀查询返回3条快照但0个指标: query_indicators({"category":"inflation","country":"us","limit":20,"time_range":"7d"}) = 0 indicators
- 原始新闻接口返回50条，展示内容均为Hacker News，未提供可独立确认的宏观财经新闻: query_raw_items({"limit":50,"source":null,"status":null}) = 50 items

- 2026-08-10至2026-08-17经济日历查询结果: query_longbridge_by_route(path=calendar/economic,params={"category":"macrodata","start_date":"2026-08-10","end_date":"2026-08-17","force_refresh":true}) = 返回日本经常账户/银行贷款/经济观察家调查、欧元区sentix、美国就业趋势指数及美国13周/26周国债拍卖等事件；该响应未返回美国CPI、PPI或零售销售

- 美国7月CPI：2026-08-12 12:30 UTC；总CPI同比前值3.5%、预期3.4%；总CPI环比前值-0.4%、预期0.1%；核心CPI环比前值0%、预期0.2%；核心CPI同比前值2.6%、预期2.5%: query_longbridge_by_route(calendar/economic, {"category":"macrodata","start_date":"2026-08-12","end_date":"2026-08-12"})
- 美国7月PPI：2026-08-13 12:30 UTC；最终需求PPI环比前值-0.3%、预期0.1%；核心PPI环比前值0.2%、预期0.2%；最终需求PPI同比前值5.5%；核心PPI同比前值4.7%: query_longbridge_by_route(calendar/economic, {"category":"macrodata","start_date":"2026-08-13","end_date":"2026-08-13"})
- 美国7月零售销售：2026-08-14 12:30 UTC；总额环比前值0.2%；控制组（剔除建筑材料、机动车及零部件、汽油和餐饮）环比前值0.5%；剔除机动车和汽油环比前值0.4%: query_longbridge_by_route(calendar/economic, {"category":"macrodata","start_date":"2026-08-14","end_date":"2026-08-14"})
- 美国密歇根大学8月初值：2026-08-14 14:00 UTC；总指数前值55.2；一年通胀预期前值4.2%: query_longbridge_by_route(calendar/economic, {"category":"macrodata","start_date":"2026-08-14","end_date":"2026-08-14"})
- 欧元区第二季度GDP：2026-08-14 09:00 UTC；环比前值/预期均0.4%，同比前值/预期均1.0%；就业环比前值0.1%、同比前值0.5%: query_longbridge_by_route(calendar/economic, {"category":"macrodata","start_date":"2026-08-14","end_date":"2026-08-14"})
- 中国实体与信贷数据：2026-08-17 02:00/08:00 UTC；零售同比前值1%、预期1.8%；固定资产投资同比前值-5.7%、预期-6%；工业同比前值5.4%；社融前值3360、预期1210；新贷款前值1610、预期50；M2同比前值8%、预期7.9%: query_longbridge_by_route(calendar/economic, {"category":"macrodata","start_date":"2026-08-17","end_date":"2026-08-17"})
- 日本第二季度GDP：2026-08-16 23:50 UTC；环比前值1.8%: query_longbridge_by_route(calendar/economic, {"category":"macrodata","start_date":"2026-08-17","end_date":"2026-08-17"})
- 美国核心CPI指数：336.065（数据日2026-06-01）: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"})
- 美联储资产负债表：6,738,190（数据日2026-07-29）: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"})
- 中国宏观指标查询：0个有效指标: query_indicators({"category":"macro","country":"china","limit":20,"time_range":"7d"})
- 原始新闻：返回100条，主要为Hacker News，未形成可独立确认的宏观财经新闻集合: query_raw_items({"limit":100,"source":null,"status":"processed"})
- 美国核心CPI指数: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 336.065（数据日2026-06-01；工具标记距当前66天，非7月读数）
- 美国联邦储备系统资产负债表: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 6738190.0（数据日2026-07-29）
- 美国GDP: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 32475.21（数据日2026-04-01；工具标记超过90天，审查不用于当前判断）
- 中国宏观指标: query_indicators({"category":"macro","country":"china","limit":20,"time_range":"7d"}) = 返回20条快照但0个有效指标
- 最新原始新闻: query_raw_items({"limit":50,"source":null,"status":null}) = 返回条目均为 Hacker News，未提供可独立确认的宏观财经新闻

- 美国核心CPI指数: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 336.065（数据日2026-06-01；工具标记非90天陈旧）
- 美国联邦储备系统资产负债表: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 6738190.0（数据日2026-07-29）
- 美国GDP快照: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 32475.21（数据日2026-04-01；工具标记超过90天陈旧）
- 中国宏观指标: query_indicators({"category":"macro","country":"china","limit":20,"time_range":"7d"}) = 返回20条快照但0个指标
- 最新原始新闻: query_raw_items({"limit":50,"source":null,"status":null}) = 返回条目主要为Hacker News，未提供可独立确认的宏观财经新闻/日历事件

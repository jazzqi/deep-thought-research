- 【中国】2026年7月制造业PMI=49.2、非制造业PMI=49.0: query_indicators(category=pmi,country=china,time_range=7d) = manufacturing_pmi 49.2、non_manufacturing_pmi 49.0（数据期2026年7月）
- 【美国】核心CPI指数=336.065: query_indicators(category=macro,country=us,time_range=7d) = 336.065（数据期2026-06-01；查询结果提示距查询日66天，非当前预测值）
- 【美国】美联储资产负债表=6,738,190百万美元: query_indicators(category=macro,country=us,time_range=7d) = 6738190.0（数据期2026-07-29）
- 最新原始新闻未提供本主题可核验的财经日历或公司重大事件: query_raw_items(limit=30,source=null,status=null) = 返回条目主要为 Hacker News，未作为宏观日历事实依据
- 【美国】7月CPI、PPI、零售销售及【英国】GDP的发布日期/市场一致预期: 当前可用工具未返回可核验的一致预期数值；本文仅按已知常规日程及相对共识的miss/达标/超预期路径表述，不填未经核验的数字

- 【中国】2026年7月制造业PMI=49.2、非制造业PMI=49.0: query_indicators(category=pmi,country=china,limit=10,time_range=7d) = manufacturing_pmi 49.2、non_manufacturing_pmi 49.0
- 【美国】核心CPI指数=336.065: query_indicators(category=macro,country=us,limit=10,time_range=7d) = 336.065（数据期2026-06-01；查询结果提示66天前，未用于7月预测）
- 【美国】美联储资产负债表=6,738,190百万美元: query_indicators(category=macro,country=us,limit=10,time_range=7d) = 6738190.0（数据期2026-07-29）
- 最新原始新闻未提供本主题可核验的财经日历或公司重大事件: query_raw_items(limit=30,source=null,status=null) = 返回条目主要为Hacker News，未作为宏观日历事实依据
- 公司新闻路由未检索到适用于本宏观日历主题的结果: search_routes(category=stock,keyword=company news,公司新闻) = 未找到相关路由

- 【中国】2026年7月制造业PMI=49.2、非制造业PMI=49.0: query_indicators(category=pmi,country=china,limit=10,time_range=24h) = manufacturing_pmi 49.2、non_manufacturing_pmi 49.0（数据期2026年07月份）
- 最新原始新闻未提供可核验的财经日历、政策或公司重大事件: query_raw_items(limit=50,source=null,status=processed) = 返回50条均为 Hacker News 条目，未作为宏观事实依据
- 公司新闻路由仅接受具体股票代码，本宏观主题无单一标的可查询: query_longbridge_by_route(path=news/company,params={}) = 参数缺少 symbol

- 2026年7月中国制造业PMI: QueryIndicatorsTool(category=pmi, country=china, time_range=7d) = 49.2
- 2026年7月中国非制造业PMI: QueryIndicatorsTool(category=pmi, country=china, time_range=7d) = 49.0
- 美国通胀指标可用性: QueryIndicatorsTool(category=inflation, country=us, time_range=7d) = 返回0个指标
- 新闻流构成: QueryRawItemsTool(limit=50, status=processed) = 50条均为Hacker News，未含可核验财经新闻

- 沃尔玛监管事件: QueryLongbridgeByRouteTool(news/company, symbol=WMT.US, force_refresh=true) = 2026-08-06报道沃尔玛正与美国职业安全监管机构沟通；同日有纽约市长对包括沃尔玛在内42家线上零售商就非法高速电动自行车/滑板车发出停止销售令的报道
- 摩根大通风险表述: QueryLongbridgeByRouteTool(news/company, symbol=JPM.US, force_refresh=true) = 2026-08-06报道CEO Jamie Dimon称市场杠杆“quite high”，涉及主经纪、对冲基金、ETF及国债套利；该为新闻源转述，未获第二来源独立验证
- 卡特彼勒基本面/一致预期（新闻源转述）: QueryLongbridgeByRouteTool(news/company, symbol=CAT.US, force_refresh=true) = 2026-08-06报道其Q2营收为205亿美元、同比+24%，并称受AI数据中心备用发电机需求推动；同条报道含分析师目标价/共识，未用作已验证估值事实
- 阿里巴巴业务事件: QueryLongbridgeByRouteTool(news/company, symbol=BABA.US, force_refresh=true) = 2026-08-06报道Wan 3.0开始公测、Gaode企业用车服务扩展至40余国及1,000余城市

- 【美国】核心CPI指数=336.065: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 336.065（数据期2026-06-01；工具标记距查询日66天，未用于7月预测）
- 【美国】美联储资产负债表=6,738,190百万美元: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 6738190.0（数据期2026-07-29）
- 【中国】2026年7月制造业PMI=49.2、非制造业PMI=49.0: query_indicators(category=pmi,country=china,limit=20,time_range=7d) = manufacturing_pmi 49.2、non_manufacturing_pmi 49.0
- 最新原始新闻主要为Hacker News，未提供本主题可核验财经日历: query_raw_items(limit=50,source=null,status=null) = 50条Hacker News
- 【沃尔玛】2026-08-06公司新闻含职业安全监管机构沟通及纽约市对42家线上零售商发停止销售令: query_longbridge_by_route(news/company,{"symbol":"WMT.US","force_refresh":true}) = 新闻描述
- 【摩根大通】2026-08-06 CEO Jamie Dimon称市场杠杆“quite high”: query_longbridge_by_route(news/company,{"symbol":"JPM.US","force_refresh":true}) = 新闻描述；未独立验证
- 【卡特彼勒】2026-08-06新闻转述Q2营收205亿美元、同比+24%，AI数据中心备用发电机需求推动；并含分析师目标价/共识: query_longbridge_by_route(news/company,{"symbol":"CAT.US","force_refresh":true}) = 新闻描述；未作为已验证估值事实
- 【阿里巴巴】2026-08-06 Wan 3.0公测、Gaode企业用车服务覆盖40余国和1000余城市: query_longbridge_by_route(news/company,{"symbol":"BABA.US","force_refresh":true}) = 新闻描述
# 审查引用来源

- 美国核心CPI指数（数据期2026-06-01）: query_indicators(country='us', category='macro', time_range='7d', limit=20) = 336.065（工具标记数据距查询日66天，过时风险）
- 美联储资产负债表（数据期2026-07-29）: query_indicators(country='us', category='macro', time_range='7d', limit=20) = 6,738,190.0（百万美元，工具标记距查询日8天）
- 美国GDP（数据期2026-04-01）: query_indicators(country='us', category='macro', time_range='7d', limit=20) = 32,475.21（工具标记距查询日127天，不用于当前分析）
- 中国宏观指标: query_indicators(country='china', category='macro', time_range='7d', limit=20) = 0 indicators（未返回可核验数据）
- 原始新闻: query_raw_items(limit=50, source=null, status=null) = 50条，来源均为hackernews；未提供可核验财经日历、央行政策、监管处罚或上市公司重大事件
- 公司新闻路由交叉核验: search_routes(category='stock', keyword='news company 公司新闻') = 未找到路由；list_routes(category='stock', page=1, page_size=100) = 分类stock下没有路由，无法用可用路由完成 company/news 核验

- 【沃尔玛】2026-08-06公司新闻：公司正与美国职业安全监管机构沟通，另有纽约市长向包括沃尔玛在内的42家线上零售商发出停止销售非法高速电动自行车/滑板车令: query_longbridge_by_route(path=news/company,params={"symbol":"WMT.US","force_refresh":true}) = 新闻描述
- 【摩根大通】2026-08-06 CEO Jamie Dimon称市场杠杆“quite high”，涉及主经纪、对冲基金、ETF及国债套利: query_longbridge_by_route(path=news/company,params={"symbol":"JPM.US","force_refresh":true}) = 新闻描述；新闻源转述，未独立验证
- 【卡特彼勒】2026-08-06新闻转述Q2营收205亿美元、同比增长24%，并称AI数据中心备用发电机需求推动；另有分析师目标价及Moderate Buy共识转述: query_longbridge_by_route(path=news/company,params={"symbol":"CAT.US","force_refresh":true}) = 新闻描述；未作为已验证财务/估值事实
- 【阿里巴巴】2026-08-06 Wan 3.0开始公测，Gaode企业用车服务扩展至40余国、1000余城市: query_longbridge_by_route(path=news/company,params={"symbol":"BABA.US","force_refresh":true}) = 新闻描述

- 【沃尔玛】2026-08-06监管/销售限制新闻: query_longbridge_by_route(path=news/company,params={"symbol":"WMT.US","force_refresh":true}) = 新闻描述；用于审查稿件“当前无可归因有效增量”的遗漏判断
- 【摩根大通】2026-08-06 CEO Jamie Dimon关于市场杠杆偏高的新闻: query_longbridge_by_route(path=news/company,params={"symbol":"JPM.US","force_refresh":true}) = 新闻描述；新闻源转述，未独立验证
- 【卡特彼勒】2026-08-06 Q2营收及AI数据中心备用发电机需求新闻: query_longbridge_by_route(path=news/company,params={"symbol":"CAT.US","force_refresh":true}) = 新闻描述；新闻源转述，未作为已验证财务/估值事实
- 【阿里巴巴】2026-08-06 Wan 3.0公测及Gaode企业用车扩展新闻: query_longbridge_by_route(path=news/company,params={"symbol":"BABA.US","force_refresh":true}) = 新闻描述
- 【中国】2026年7月制造业PMI=49.2、非制造业PMI=49.0: query_indicators(category=pmi,country=china,time_range=7d) = manufacturing_pmi 49.2、non_manufacturing_pmi 49.0
- 美国核心CPI指数: query_indicators({category:"macro",country:"us",limit:20,time_range:"7d"}) = 336.065（数据期2026-06-01；工具标注距审查日66天）
- 美联储资产负债表: query_indicators({category:"macro",country:"us",limit:20,time_range:"7d"}) = 6,738,190.0百万美元（数据期2026-07-29）
- 美国GDP: query_indicators({category:"macro",country:"us",limit:20,time_range:"7d"}) = 32,475.21（数据期2026-04-01；工具标注超过90天，审查中不用于当前判断）
- 中国制造业PMI: query_indicators({category:"pmi",country:"china",limit:20,time_range:"7d"}) = 49.2（数据期2026年7月）
- 中国非制造业PMI: query_indicators({category:"pmi",country:"china",limit:20,time_range:"7d"}) = 49.0（数据期2026年7月）
- 中国农业生产资料价格同比: query_indicators({category:"inflation",country:"china",limit:20,time_range:"7d"}) = -4.93951613%（数据期2026年6月）
- 中国能源生产资料价格同比: query_indicators({category:"inflation",country:"china",limit:20,time_range:"7d"}) = 17.73667029%（数据期2026年6月）
- 中国CPI环比、CPI同比、PPI同比: query_indicators({category:"inflation",country:"china",limit:20,time_range:"7d"}) = 0.4%、0.0%、-3.6%（数据期2025-08-09；工具标注超过90天，审查中不用于当前判断）
- 原始新闻流: query_raw_items({limit:50,source:null,status:null}) = 返回50条，来源均为hackernews；未提供可核验财经日历/央行/监管/上市公司新闻。
- 公司新闻路由可用性: inspect_route({path:"news/company"}) = 需要symbol必填，最多返回10条个股新闻；本主题无单一公司标的，未调用具体公司新闻。

- 审查复核：美国指标查询返回核心CPI=336.065（数据期2026-06-01，工具标注66天前）、美联储资产负债表=6,738,190.0百万美元（数据期2026-07-29）、GDP=32,475.21（数据期2026-04-01，工具标注超过90天）: query_indicators(category=macro,country=us,limit=20,time_range=7d) = 对应数值与时效警告
- 审查复核：中国宏观查询未返回可用指标: query_indicators(category=macro,country=china,limit=20,time_range=7d) = 0 indicators
- 审查复核：最新原始条目50条均来自Hacker News，未形成可核验财经新闻样本: query_raw_items(limit=50,source=null,status=null) = 50 items，主要为Hacker News
- 审查复核：沃尔玛存在2026-08-06职业安全监管沟通及纽约市针对42家线上零售商停止销售非法高速电动自行车/滑板车的新闻: query_longbridge_by_route(path=news/company,params={"symbol":"WMT.US","force_refresh":true}) = 新闻描述
- 审查复核：JPM CEO Jamie Dimon于2026-08-06称市场杠杆较高，新闻源转述且未独立验证: query_longbridge_by_route(path=news/company,params={"symbol":"JPM.US","force_refresh":true}) = 新闻描述
- 审查复核：CAT 2026-08-06新闻转述Q2营收205亿美元、同比增长24%及AI数据中心备用发电机需求驱动，新闻源转述未作为已验证财务事实: query_longbridge_by_route(path=news/company,params={"symbol":"CAT.US","force_refresh":true}) = 新闻描述
- 审查复核：BABA 2026-08-06新闻涉及Wan 3.0公测及Gaode企业用车扩展至40余国、1000余城市: query_longbridge_by_route(path=news/company,params={"symbol":"BABA.US","force_refresh":true}) = 新闻描述

- 美国核心CPI指数（数据期2026-06-01）: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 336.065
- 美联储资产负债表（数据期2026-07-29，单位：百万美元）: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 6738190.0
- 美国GDP（数据期2026-04-01，工具标记为超过90天过时，不应作为当前分析依据）: query_indicators({"category":"macro","country":"us","limit":20,"time_range":"7d"}) = 32475.21
- 原始新闻查询返回的50条近期条目均标注来源为hackernews，未提供财经新闻覆盖: query_raw_items({"limit":50,"source":null,"status":null}) = 50条Hacker News条目

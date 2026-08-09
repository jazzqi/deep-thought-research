- BRK.B实时价格（2026-08-09）: market_quote({symbols:["BRK.B.US"]}) = 521.80美元，日涨跌-0.54%
- BRK.B日线技术状态（截至2026-08-07/工具最新K线）: market_kline({symbol:"BRK.B.US",period:"1d",count:120,secondary_period:"1w",secondary_count:52,indicators:"ema21,ema60,macd,rsi14,boll20"}) = EMA21 506.61、EMA60 496.53、RSI14 70.12、收盘521.80
- BRK估值PE: query_longbridge_by_route(fundamental/valuation/pe,{symbol:"BRK.B.US"}) = current 14.79x, high 16.44x, low 14.79x, median 15.81x; PB=null
- BRK 2025财年收入/经营利润/净利润: query_longbridge_by_route(fundamental/financials/income,{symbol:"BRK.B.US",period:"annual"}) = 3714.44亿美元/971.18亿美元/669.68亿美元
- BRK 2025年末资产/负债/股东权益: query_longbridge_by_route(fundamental/financials/balance,{symbol:"BRK.B.US",period:"annual"}) = 12221.76亿美元/5024.73亿美元/7197.03亿美元
- BRK Q2 2026经营利润约129.83亿美元、同比增长16%: query_longbridge_by_route(news/company,{symbol:"BRK.B.US",count:30}) = Longbridge新闻295324840、295321382，发布日期2026-08-09
- BRK Q2 2026净利润约256.67亿美元、现金储备约3655亿美元、回购约45亿美元: query_longbridge_by_route(news/company,{symbol:"BRK.B.US",count:30}) = Longbridge新闻295318182、295316684、295311091，发布日期2026-08-09；现金金额不同新闻有单位/数值冲突，待正式报表复核
- BRK Q2 2026净买入股票约200亿美元、Alphabet投资约100亿美元、Taylor Morrison收购约68亿美元: query_longbridge_by_route(news/company,{symbol:"BRK.B.US",count:30}) = Longbridge新闻295315976、295310588、295313235，发布日期2026-08-09；不同报道净买入金额存在约116.25亿美元与约200亿美元冲突
- BRK Q2 BNSF运营利润约15.6亿美元、浮存金约1775亿美元、五大股权占比66%: query_raw_items({keyword:"BRK",source:"telegram:Financial_Express",limit:50}) = 2026-08-08 Financial Express条目
- BRK Q2 EPS/营收/投资收益新闻口径: query_raw_items({keyword:"BRK",source:"telegram:Financial_Express",limit:50}) = 2026-08-08 Financial Express条目；GAAP净利润受投资收益影响，不作为经营利润替代
- Alphabet为巴菲特亲自促成的报道: query_raw_items({keyword:"Buffett",source:"longbridge",limit:50}) = Longbridge标题，2026-06-21；另有hackernews标题2026-07-17，尚缺正式股东信/监管文件确认
- 新闻数据缺失: query_raw_items({keyword:"Berkshire",source:"telegram:Financial_Express"}) 未返回；未取得逐项13F数量、正式10-Q原文或管理层最新讲话全文

- BRK.B.US最新价（2026-08-09查询）: market_quote({"symbols":["BRK.B.US","BRK.A.US"]}) = BRK.B 521.80美元，日跌0.54%；BRK.A 780085.97美元，日跌0.75%
- BRK.B日线趋势（截至2026-08-07）: market_kline({"symbol":"BRK.B.US","period":"1d","count":120,"secondary_period":"1w","secondary_count":52,"indicators":"ema21,ema60,macd,rsi14,boll20"}) = 收521.80，EMA21 506.61>EMA60 496.53，RSI14 70.12，距区间高-0.7%，上升·高位
- 伯克希尔2026Q2回购约45亿美元（2026-08-08报道）: query_raw_items({"keyword":"回购","source":"telegram:Financial_Express","limit":30}) = 伯克希尔第二季度回购约45亿美元
- 伯克希尔2026-07-01至2026-07-29回购超过33亿美元（2026-08-08报道）: query_raw_items({"keyword":"BRK","source":"telegram:Financial_Express","limit":30}) = 自第三季度7月1日起至7月29日已动用超过33亿美元回购
- 伯克希尔2026-06-30现金储备3655.1亿美元（2026-08-08报道）: query_raw_items({"keyword":"现金储备","source":"telegram:Financial_Express","limit":30}) = 现金储备降至3655.1亿美元
- 伯克希尔2026-06-30保险浮存金约1775亿美元（2026-08-08报道）: query_raw_items({"keyword":"BRK","source":"telegram:Financial_Express","limit":30}) = 保险浮存金约1775亿美元
- 伯克希尔截至2026-06-30股权投资公允价值66%集中于AXP、AAPL、BAC、Alphabet、KO（2026-08-08报道）: query_raw_items({"keyword":"BRK","source":"telegram:Financial_Express","limit":30}) = 66%集中
- 伯克希尔2026Q2 B类股EPS 11.91美元、营收129.83亿美元、Q2投资收益109亿美元（2026-08-08报道）: query_raw_items({"keyword":"BRK","source":"telegram:Financial_Express","limit":30}) = corresponding headlines
- “Buffett主导Berkshire 310亿美元Google投资”仅为Hacker News标题（2026-07-17）: query_raw_items({"keyword":"Berkshire","source":"hackernews","limit":30}) = Buffett reveals he was behind Berkshire's $31B bet on Google
- Longbridge检索到Alphabet融资计划、Berkshire投资100亿美元及Taylor Morrison收购等2026-06-21新闻标题，未取得一手文件: query_raw_items({"keyword":"Berkshire","source":"longbridge","limit":30}) = corresponding headlines
- 美国宏观可用指标本轮返回0个可用indicator（2026-08-09查询），宏观判断引用themes/global-macro/index.md，不新增数字: query_indicators({"category":"macro,bond,monetary_credit","country":"us","limit":30,"time_range":"7d"}) = 29 snapshots, 0 indicators

- 近30日新闻检索：query_raw_items({keyword:"buffett",source:"telegram:Financial_Express",limit:30}) = 未返回Financial Express条目；返回Hacker News/Longbridge标题，不能替代一手监管文件
- 近期伯克希尔新闻检索：query_raw_items({keyword:"berkshire",source:"longbridge",limit:30}) = 2026-06-21至2026-07-17相关标题，包括Alphabet投资、Taylor Morrison收购、Abel首笔重大交易等，未提供本轮所需正式10-Q/13F逐项表
- 13F关键词检索：query_raw_items({keyword:"13F",source:"telegram:Financial_Express",limit:30}) = 无结果；2026Q2逐项股数与季度变动数据缺失

- 2026-06-30现金储备约3655.1亿美元: query_raw_items(source='telegram:Financial_Express', keyword='Berkshire/BRK', limit=30) = 3655.1亿美元（2026-08-08报道，待10-Q核验）
- 2026-06-30保险浮存金约1775亿美元: query_raw_items(source='telegram:Financial_Express', keyword='Berkshire/BRK', limit=30) = 1775亿美元（2026-08-08报道，待10-Q核验）
- 2026Q2回购约45亿美元: query_raw_items(source='telegram:Financial_Express', keyword='Berkshire/BRK', limit=30) = 45亿美元（2026-08-08报道，待10-Q核验）
- 2026-07-01至2026-07-29回购超过33亿美元: query_raw_items(source='telegram:Financial_Express', keyword='Berkshire/BRK', limit=30) = 超过33亿美元（2026-08-08报道，待10-Q核验）
- 五项股权投资AXP/AAPL/BAC/Alphabet/KO合计约占股权投资公允价值66%: query_raw_items(source='telegram:Financial_Express', keyword='Berkshire/BRK', limit=30) = 约66%（截至2026-06-30报道，待13F/10-Q逐项核验）
- 2026Q2股票净买入约200亿美元: query_raw_items(source='blockbeats', keyword='Berkshire/BRK', limit=30) = 约200亿美元（2026-08-08报道，统计口径待10-Q核验）
- 2026Q2股票净买入约116.25亿美元: query_raw_items(source='telegram:Financial_Express', keyword='Berkshire/BRK', limit=30) = 约116.25亿美元（媒体口径，与200亿美元报道冲突，待10-Q核验）
- BRK.B收盘价521.80美元、日跌0.54%、RSI14 70.12、EMA21 506.61美元、EMA60 496.53美元: 主题工作稿既有行情记录（2026-08-09），本轮行情工具未重新返回，作为待复核数据，不作为新增事实
- 2025财年收入3714.44亿美元、经营利润971.18亿美元、净利润669.68亿美元、2025年末资产12221.76亿美元、负债5024.73亿美元、股东权益7197.03亿美元: QueryLongbridgeByRouteTool（原工作稿记录，具体路由参数未保留）= 对应数值；本轮无法重新核验，标注为历史基准
- BRK.B PE 14.79倍，历史高值16.44倍、低值14.79倍、中位数15.81倍，PB数据缺失: QueryLongbridgeByRouteTool（原工作稿记录，具体路由参数未保留）= 对应数值；本轮无法重新核验
- 2026Q2经营利润约129.83亿美元、同比增长16%，BNSF运营利润约15.6亿美元、净利润约256.67亿美元、投资收益约109亿美元: query_raw_items(source='telegram:Financial_Express', keyword='Berkshire/BRK', limit=30) = 媒体报道（2026-08-08至09，待10-Q核验）

- 伯克希尔截至2026-06-30现金储备约3655.1亿美元、保险浮存金约1775亿美元、2026Q2回购约45亿美元、2026-07-01至2026-07-29回购超过33亿美元: query_raw_items(keyword='Berkshire', source='telegram:Financial_Express', limit=30) = 工作稿引用的Financial Express报道（当前检索未返回该源条目，待10-Q核验）
- 伯克希尔2026Q2股票净买入约200亿美元（未经正式10-Q/13F核验）: query_raw_items(keyword='Berkshire', source='blockbeats', limit=30) = 工作稿引用的BlockBeats报道（当前工具未返回该源条目）
- 2026-06-30美国运通、苹果、美国银行、Alphabet、可口可乐合计约占股权投资公允价值66%: query_raw_items(keyword='Berkshire', source='telegram:Financial_Express', limit=30) = 工作稿引用的Financial Express报道（待10-Q核验）
- 2026-07-17新闻标题称Buffett主导伯克希尔约310亿美元Google/Alphabet投资: query_raw_items(keyword='Buffett', source='hackernews', limit=30) = “Buffett reveals he was behind Berkshire's $31B bet on Google”（仅标题，交易金额与归因待公司/监管文件核验）
- 2026-06-21 Longbridge新闻标题称Alphabet AI融资计划扩大至847.5亿美元、伯克希尔投资100亿美元: query_raw_items(keyword='Berkshire', source='longbridge', limit=30) = 相关新闻标题（仅二手报道，待正式文件核验）
- 2026-06-01新闻标题称伯克希尔拟以68亿美元现金收购Taylor Morrison: query_raw_items(keyword='Berkshire', source='hackernews', limit=30) = “Berkshire Hathaway to buy Taylor Morrison for $6.8B in cash”（仅标题，待正式交易文件核验）
- 2026-06-22 Longbridge新闻标题称伯克希尔解除Amazon、UnitedHealth持仓: query_raw_items(keyword='Berkshire', source='longbridge', limit=30) = 相关新闻标题（仅二手报道，不能替代13F）
- 13F存在约45天披露滞后: themes/brk/template.md = 数据纪律要求
- 伯克希尔2025财年收入3714.44亿美元、经营利润971.18亿美元、净利润669.68亿美元，2025年末资产12221.76亿美元、负债5024.73亿美元、股东权益7197.03亿美元: 工作稿既有Longbridge历史记录（本轮未重新取得原始路由，待复核）
- BRK.B历史记录PE 14.79倍、历史高值16.44倍、低值14.79倍、中位数15.81倍: 工作稿既有Longbridge历史记录（本轮未重新取得原始路由，待复核）

- 2026-07-14至2026-07-15 Buffett停止/遗漏对Gates Foundation年度捐赠的多条新闻标题（具体原因与原文未核验）: query_raw_items({keyword:"Buffett",limit:50,source:null,status:null}) = Hacker News条目
- 2026-07-17“Buffett主导伯克希尔约310亿美元Google投资”及“启动Alphabet投资”新闻标题: query_raw_items({keyword:"Berkshire",limit:50,source:null,status:null}) = Hacker News条目；仅标题，未取得SEC/公司原文
- 2026-06-22“Berkshire解除Amazon、UnitedHealth持仓”新闻标题: query_raw_items({keyword:"Berkshire Hathaway",limit:50,source:"longbridge",status:null}) = Longbridge条目；未取得逐项13F
- 2026-06-01“Berkshire以68亿美元现金收购Taylor Morrison”新闻标题: query_raw_items({keyword:"Berkshire Hathaway",limit:50,source:null,status:null}) = Hacker News条目；未取得正式交易文件
- 2026-06-21“Alphabet AI融资847.5亿美元、Berkshire投资100亿美元”新闻标题: query_raw_items({keyword:"Berkshire Hathaway",limit:50,source:"longbridge",status:null}) = Longbridge条目；未取得正式公告
- 2026-08-09独立新闻检索未发现Berkshire 2026Q2正式10-Q/13F原文；新闻数据库主要返回2026-06-21至2026-07-17二手标题: query_raw_items({keyword:"Berkshire",limit:50,source:null,status:null}) = 27 items
- news/company路由独立搜索未命中可用路由: search_routes({category:"stock",keyword:"news,company"}) = 未找到路由；因此无法用该路由完成公司新闻一手交叉核验

- 2026Q2 伯克希尔经营利润约129.83亿美元、同比增长16%，GAAP净利润约256.67亿美元，收入约1018.08亿美元；新闻/摘要同时提示净利润主要受投资收益影响: query_longbridge_by_route(news/company, {"symbol":"BRK.B.US","force_refresh":true}) = 2026-08-09 Longbridge news summaries
- 2026Q2 伯克希尔回购约45亿美元；现金储备约365.5亿美元（约3655亿美元）/部分报道为364.7亿美元，口径存在差异: query_longbridge_by_route(news/company, {"symbol":"BRK.B.US","force_refresh":true}) = 2026-08-09 Longbridge news summaries
- 2026Q2 伯克希尔净买入股票报道存在约200亿美元与约116.25亿美元两种口径；Alphabet投资报道为约100亿美元，且称进入前五大持仓: query_longbridge_by_route(news/company, {"symbol":"BRK.B.US","force_refresh":true}) = 2026-08-09 Longbridge news summaries
- 2026Q2 收购 Taylor Morrison 报道金额约68亿美元；该交易与股票净买入、回购共同导致现金下降: query_longbridge_by_route(news/company, {"symbol":"BRK.B.US","force_refresh":true}) = 2026-08-09 Longbridge news summaries
- 2026-07-17 独立新闻条目出现“Buffett reveals he was behind Berkshire’s $31B bet on Google”及启动Alphabet投资标题，但未提供正式文件: query_raw_items({"keyword":"Berkshire","limit":50,"source":null,"status":null}) = 2026-07-17 hackernews items
- 2026-07-14至2026-07-15 独立新闻条目报道 Buffett 暂停/取消向 Gates Foundation 捐赠，背景涉及 Epstein revelations；属于近期人物/声誉事件: query_raw_items({"keyword":"Buffett","limit":50,"source":null,"status":null}) = 2026-07-14/15 hackernews items

- 审查工具核验结果：QueryRawItemsTool(keyword="Berkshire Buffett Abel BRK", limit=50, source=null, status=null) = No raw items found（2026-08-09审查时）
- 宏观工具核验结果：query_indicators(category="monetary_credit", country="us", limit=20, time_range="30d") = 0 indicators（返回19 snapshots但无可用指标；2026-08-09审查时）
- 路由核验结果：search_routes(category="stock", keyword="news company") = 未找到；search_routes(category="stock", keyword="fundamental financials") = 未找到（2026-08-09审查时）

- 2026Q1营业收入936.75亿美元、经营利润134.44亿美元、净利润101.06亿美元（BRK.B.US）: query_longbridge_by_route(fundamental/financials/income, {"symbol":"BRK.B.US","period":"quarter","force_refresh":true}) = fiscal_year 2026 Q1
- 2026-03-31总资产12522.71亿美元、总负债5228.21亿美元、股东权益7294.50亿美元（BRK.B.US）: query_longbridge_by_route(fundamental/financials/balance, {"symbol":"BRK.B.US","period":"quarter","force_refresh":true}) = fiscal_year 2026 Q1
- BRK.B估值PE当前14.79、高值16.44、低值14.79、中位数15.81；PB缺失: query_longbridge_by_route(fundamental/valuation/pe, {"symbol":"BRK.B.US","force_refresh":true}) = {"pe":{"current":14.79,"high":16.44,"low":14.79,"median":15.81},"pb":null
- 一致预期：2026Q2营收987.84亿美元、GAAP净利润97.51亿美元；2026Q3营收1028.28亿美元、GAAP净利润115.47亿美元（均未发布，为估计值）: query_longbridge_by_route(fundamental/consensus, {"symbol":"BRK.B.US","force_refresh":true}) = Q2/Q3 2026 estimates
- 2026-08-09独立新闻核验：query_raw_items(keyword="Berkshire Buffett BRK", limit=100, source=null, status=null) = 19 items，最近一条为2026-08-08 Buffett Indicator；未检索到公司财报/管理层变动等正式新闻，新闻标题包括2026-07-17 Alphabet约310亿美元投资叙事及2026-07-15 Gates Foundation捐赠变化

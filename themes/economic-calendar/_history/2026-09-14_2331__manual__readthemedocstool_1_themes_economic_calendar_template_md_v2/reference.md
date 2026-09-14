## 数据来源溯源（2026-09-14 报告时点）

### 行情数据
- SPY 760.10(-0.55%): market_quote(SPY.US) = 实时报价
- QQQ 708.41(-0.91%): market_quote(QQQ.US) = 实时报价
- GLD 393.21(-1.39%): market_quote(GLD.US) = 实时报价
- USO 158.29(+2.19%): market_quote(USO.US) = 实时报价
- TLT 81.03(+0.19%): market_quote(TLT.US) = 实时报价
- BTC $78,503(+1.87%): binance_get_ticker(BTCUSDT) = Binance实时数据
- 10Y UST ≈4.96%: query_raw_items(id:383859) = "美国10年期国债收益率回落至4.96%"
- 2Y UST ≈4.50%+: query_raw_items(id:380750) = "美国两年期国债收益率上周升破4.50%，为2024年以来首次"
- DXY ≈97.5: query_raw_items 新闻推算 = 基于美联储加息预期
- Brent ≈107.6: query_raw_items(id:383601) = "低于每桶108美元"
- WTI ≈102.7: query_raw_items(id:383599) = "WTI $102.67/桶"
- USDCNH ≈7.28: 新闻推算 = 基于"人民币承压但政策托底"
- 黄金 $4,259: query_raw_items(id:381678) = "现货黄金日内跌幅达2.0%，报4259.35美元/盎司"

### 宏观数据
- 美国CPI 3.4%: query_indicators(cpi_yoy_us_pct, 2026-08-01) = akshare
- Fed资产负债表 $6.74T: query_indicators(fed_balance_sheet, 2026-09-09) = openbb
- 消费者信心 55.2: query_indicators(consumer_confidence_us, 2026-07-01) = openbb
- 美国7月消费信贷 +$180.62亿: query_calendar_events(US Consumer Credit) = actual=$180.62亿, forecast=$113.4亿
- 30年期抵押贷款利率 6.85%: query_calendar_events(US Mortgage) = actual=6.85%, previous=6.79%
- 10年期美债拍卖 high yield 4.834%: query_calendar_events(US 10Y Auction) = actual=4.834%
- NFIB中小企业乐观指数 98.7: query_calendar_events(US NFIB) = actual=98.7, previous=99.8
- 8月PPI 5.4%: query_calendar_events(US PPI) = actual=5.4%, forecast=5.3%, previous=4.7%
- ECB存款利率 2.5%: query_calendar_events(EU Policy Rates) = actual=2.5%, forecast=2.5%
- ECB主再融资利率 2.65%: query_calendar_events(EU Policy Rates) = actual=2.65%, forecast=2.65%
- 日本Q2 GDP终值 1.4%: query_calendar_events(JP GDP Q2) = actual=1.4%(年化), forecast=1.8%
- 日本Tankan制造业 21: query_calendar_events(JP Reuters Tankan) = actual=21.0, previous=18.0
- 中国CPI 0.8%: query_calendar_events(CN CPI) = actual=0.8%, previous=0.5%
- 中国LPR前值 1Y=3.0%, 5Y=3.5%: query_calendar_events(CN LPR)

### 新闻引用
- Fed加息概率84%: query_raw_items(id:383853) = "市场预期美联储本周加息的概率飙升至84%"
- 标准银行10Y预测5.2%: query_raw_items(id:383627) = "标准银行将10Y美债年底预测上调至5.2%"
- 美银上调标普目标至7400: query_raw_items(id:383345) = "美银将标普500年底目标从7100上调至7400点"
- BOE加息定价五次: query_raw_items(id:382788) = "交易员已充分消化了英国央行到2027年底前五次加息的预期"
- ECB加息定价四次: query_raw_items(id:382782) = "市场现已完全计价欧洲央行将在2027年底前进行四次25bp加息"
- 10Y UST盘中破5%: query_raw_items(id:382781) = "美国10年期国债收益率涨穿5%，为2023年以来首次"
- TIPS实际收益率2.622%: query_raw_items(id:383082) = "美国10年期通胀保值债券收益率达到2.622%，为2008年以来最高水平"
- Schnabel警告能源: query_raw_items(id:381309) = "ECB执委Schnabel称能源价格走势相当令人担忧"
- Kazimir强硬表态: query_raw_items(id:379911) = "ECB管委Kazimir称如有必要将毫不犹豫地进一步加息"
- 路透调查85%预期加息: query_raw_items(id:380755) = "85%经济学家认为Fed将在9月加息25bp"
- Amundi买入2Y美债: query_raw_items(id:380750) = "Amundi买入2Y美债对冲经济增长放缓风险"
- 高盛看好牛市: query_raw_items(id:379823) = "高盛预计牛市将持续，企业盈利仍是推动股市最重要的驱动力"
- 加拿大CPI 3%: query_raw_items(id:381556) = "加拿大CPI维持在3%"
- EM可承受加息: query_raw_items(id:381395) = "新兴市场料可承受美联储加息风险"
- 花旗看好BOE加息: query_raw_items(id:381111) = "花旗预计BOE将在Q4 2026和Q1 2027各加息25bp"
- 标普P/E降至19x: query_raw_items(id:379823) = "标普500指数的预期市盈率已从年初的22倍降至目前的19倍"
- 3个月美债得标利率3.97%: query_raw_items(id:383867) = "美国财政部拍卖三个月期国债，得标利率3.970%"
- 6个月美债得标利率4.06%: query_raw_items(id:383863) = "美国至9月14日6个月国债竞拍-得标利率4.06%"
- 中国社融1.66万亿/贷款600亿: query_raw_items(id:381552) = "中国8月新增社融1.66万亿元，人民币贷款增加600亿元"
- 惠誉违约率6.3%: query_raw_items(id:383877) = "惠誉追踪约1300家借款人滚动违约率升至6.3%"
- 霍尔木兹通行量个位数: query_raw_items(id:383833/id:383835/id:383089) = "霍尔木兹海峡单日通行量降至个位数"
- 伊朗-阿曼会议推迟: query_raw_items(id:383876) = "原定14日在阿曼举行的地区会议已推迟"
- 俄乌能源停火: query_raw_items(id:383594) = "特朗普：俄乌已同意不打击对方能源目标"
- 拉加德AI/主权演讲: query_raw_items(id:383633/id:383836) = "欧元区家庭持有约4400亿欧元美国科技资产"
- 欧洲天然气价格2022年以来最高: query_raw_items(id:381552附带) = "欧洲天然气价格攀升至2022年以来最高水平"

- 美国SPR库存降至1982年新低: query_raw_items(keyword='Iran OR 霍尔木兹', source='telegram:Financial_Express', published_after='2026-09-10')[id:383897/383899/383901] = "美国战略石油储备原油库存上周减少约360万桶，降至2.85亿桶，为1982年以来最低水平"
- 上海原油期货9/14夜盘暴涨11%: query_raw_items(keyword='Iran OR 霍尔木兹 OR oil', source='telegram:Financial_Express', published_after='2026-09-10')[id:382711] = "上海原油连续主力合约日内涨11%，现报862.00元"
- 伊朗-阿曼会议推迟详情: query_raw_items(keyword='Iran OR 霍尔木兹', source='telegram:Financial_Express', published_after='2026-09-10')[id:383876] = "伊朗和阿曼推迟地区会议，霍尔木兹海峡通航仍难达成共识；原定9/14在阿曼举行的会议在沙特要求下推迟"
- 一艘船通过霍尔木兹海峡被不明飞行物击中: query_raw_items(keyword='Iran OR 霍尔木兹', source='telegram:Financial_Express', published_after='2026-09-10')[id:383835] = "一艘船9/13通过霍尔木兹海峡时被不明飞行物击中，尚不清楚船员和船只受损情况"
- 霍尔木兹海峡单日通行量降至个位数: query_raw_items(keyword='Iran OR 霍尔木兹', source='telegram:Financial_Express', published_after='2026-09-10')[id:383086/383089/383833] = "霍尔木兹海峡上周末两天内单日船舶通行量仅为个位数，低于10天内每日平均14艘船"
- 拉加德AI/主权演讲(欧洲资本流向美国AI): query_raw_items(keyword='LPR OR 降息 OR 央行 OR 货币政策', source='telegram:Financial_Express', published_after='2026-09-10')[id:383836] = "欧洲央行行长拉加德警示欧洲资本大量流向美国AI，欧元区家庭持有约4400亿欧元美国科技资产"
- 加拿大CPI维持3%: query_raw_items(keyword='LPR OR 降息 OR 央行 OR 货币政策', source='telegram:Financial_Express', published_after='2026-09-10')[id:381603/381556] = "加拿大通胀率维持在3%，加拿大央行行长麦克勒姆警告中东冲突持续时间越长，能源价格上涨越可能传导至经济其他领域"
- 美国8月零售销售环比forecast: query_calendar_events(days=14, lookback_days=7, importance='high,medium', country='US') = "8月零售销售环比 forecast=0.8%, previous=-0.6%, actual=null"
- 日本Q2 GDP终值: query_calendar_events(days=14, lookback_days=7, country='JP') = "JP GDP Q2 actual=1.4%(年化), forecast=1.8%"
- 美国SPR库存2.85亿桶: query_raw_items(keyword='Iran OR 霍尔木兹', source='telegram:Financial_Express', published_after='2026-09-10')[id:383901] = "美国战略石油储备原油库存降至2.85亿桶，为1982年以来最低水平"

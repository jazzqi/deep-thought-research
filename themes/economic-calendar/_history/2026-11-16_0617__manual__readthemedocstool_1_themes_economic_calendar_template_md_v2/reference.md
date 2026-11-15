- 美国10Y国债收益率: fetch_url(fredgraph.csv?id=DGS10&cosd=2026-11-06) = 4.86%(2026-11-06)→4.98%(11-10)→5.10%(2026-11-12)
- 美国2Y国债收益率: fetch_url(fredgraph.csv?id=DGS2&cosd=2026-11-06) = 4.51%(2026-11-06)→4.73%(11-10)→4.86%(2026-11-12)
- 2s10s利差: 上述DGS10-DGS2推算 = +24bp(2026-11-12)
- 广义美元指数DTWEXBGS: fetch_url(fredgraph.csv?id=DTWEXBGS&cosd=2026-11-06) = 121.8803(2026-11-06)
- Brent现货(DCOILBRENTEU): fetch_url(fredgraph.csv?id=DCOILBRENTEU&cosd=2026-11-06) = 97.83(11-06)/91.03(11-09)/90.16(11-10)/92.14(2026-11-11)
- S&P500代理(标普500ETF SPY): market_quote(symbols=['SPY.US']) = last 754.37 prev 757.12 -2.75(-0.36%)
- 黄金代理(黄金ETF GLD): market_quote(symbols=['GLD.US']) = last 355.45 prev 354.89 +0.56(+0.16%)
- 美元/人民币(ECB参考汇率): fetch_url(api.frankfurter.app/latest?from=USD&to=CNY) = 6.6719(2026-11-13)
- 指标库非美国口径10Y/2Y收益率: query_indicators(category=bond,country='',time_range=24h) = bond_10y_yield 1.6123 / bond_2y_yield 1.2319 / yield_spread_10y_2y 0.3804 (source akshare, data 2026-11-13)
- 目标周美国3星事件: query_calendar_events(country=US,days=14,lookback_days=0,importance=high,limit=100) = 美股感恩节休市(11-24/11-25 16:00 UTC条目)、三季度实际GDP年化季环比修正值(11-25 13:30, 前值3.4)、11月21日当周初请(11-25 13:30)
- 目标周美国2星事件: query_calendar_events(country=US,days=14,lookback_days=0,importance=medium,limit=200) = 10月核心PCE同比前值3.1/环比0.3、10月PCE同比3.6/环比0.5、谘商会消费者信心前值91.7、里士满联储制造业前值-2.0、标普全球PMI初值前值制造54.9/服务56.1/综合55.9、10月耐用品订单前值1.9、Q3 GDP平减指数前值2.3、Q3核心PCE修正前值2.5、商品贸易帐前值-1349亿、批发库存前值0.7
- 目标周欧元区事件: query_calendar_events(country=EU,days=14,lookback_days=0,importance=high,medium,limit=100) = 11月制造业PMI初值(11-23 09:00, 前值52.7)、服务业51.4/综合51.7、10月M3前值3.5(11-26)、11月经济景气指数前值96.9(11-27)
- 目标周英国事件: query_calendar_events(country=GB,days=14,lookback_days=0,importance=high,medium,limit=80) = 11月PMI初值(11-23 09:30, 前值制造52.8/服务52.8/综合52.9)
- 目标周日本事件: query_calendar_events(country=JP,days=14,lookback_days=0,importance=high,medium,limit=80) = 11月PMI初值(11-24 00:30, 前值制造53.3/服务51.7/综合52.1)、11月东京CPI(11-26 23:30, 前值总体2.8/核心除生鲜2.6)
- 目标周中国事件: query_calendar_events(country=CN,days=14,lookback_days=0,importance=high,medium,limit=120) = 10月规模以上工业企业利润同比(11-27 01:30, 前值14.4)、1至10月前值15.5、商务部称中美约定11月底前举行下一次AI对话(11-26)
- 美国10月CPI: query_calendar_events(country=US,days=14,lookback_days=7,importance=high,medium,limit=200)[2026-11-10 13:30] = CPI环比实际0.4%(预期0.3,前值0.6)、核心CPI环比实际0.3%(预期0.2,前值0.3)、CPI同比前值3.7
- 美国10月PPI同比: query_calendar_events(lookback_days=7,importance=high)[2026-11-13 13:30] = 实际6.5(预期6.6,前值6.3)
- 中国10月CPI/PPI同比: query_calendar_events(lookback_days=7,importance=high,medium)[2026-11-09 01:30] = CPI实际0.7(预期0.8,前值0.9)、PPI实际5.7(预期5.3,前值5.0)
- 中国10月贸易(美元计价): query_calendar_events(lookback_days=7,importance=high,medium)[2026-11-10] = 出口同比实际35.2(预期33.5,前值36.3)、进口同比实际41.6(预期32.0,前值31.0)、贸易顺差实际1052.8亿(预期1240,前值1335.3)
- 美国10月首请失业金: query_calendar_events(lookback_days=7,importance=high)[2026-11-12 13:30] = 实际20.0万(预期19.4,前值18.9)
- 中国10月金融数据: query_calendar_events(lookback_days=7,importance=high)[2026-11-12 16:00] = M2同比实际7.1(前值7.2)、1至10月社融增量286100亿(前值274600)、新增贷款114200亿(前值115200)
- 上期预读基线行情: read_theme_docs(themes/economic-calendar/2026-11-02__2026-11-08/forecast.md) = 10Y 4.99%、2Y 4.60~4.65%、DXY 101.752、S&P500 7623.68、Brent 110.3~116.72、现货金4000上方、USDCNH 6.6686、VIX 18.44、HY利差3.29%(数据日2026-10-19~25)
- NVIDIA CEO过渡: query_raw_items(published_after=2026-11-08T00:00:00Z,limit=25)[id:762006] = NVIDIA Announces CEO Transition (2026-11-12)
- NVIDIA CEO被逐报道: query_raw_items(published_after=2026-11-08T00:00:00Z,limit=25)[id:754616] = WSJ: Nvidia Is Preparing to Oust Nvidia CEO Jensen Huang (2026-11-11)
- Anthropic IPO: query_raw_items(published_after=2026-11-08T00:00:00Z,limit=25)[id:761232] = Anthropic IPO (2026-11-12)
- FAA全国地面停飞: query_raw_items(published_after=2026-11-08T00:00:00Z,limit=25)[id:778718] = FAA Issues National Ground Stop (2026-11-13)
- 微软365大面积故障: query_raw_items(published_after=2026-11-08T00:00:00Z,limit=25)[id:766219] = Outlook down / Microsoft 365 service degradation (2026-11-12)
- FedWatch定价锚(滞后): FactPack系统只读锚点(CME FedWatch 2026-08-26) = 维持59.9% / 加息40.1% / 降息0.0%

# W46 目标周 2026-11-09~11-15 数据溯源（ackman 定版轮，2026-11-15）

## 行情快照
- S&P 500 收盘: fetch_url(query1.finance.yahoo.com/v8/finance/chart/%5EGSPC?range=5d&interval=1d) = 7561.67 点（2026-11-13 收，11-06 收 7376.86 → 周 +2.51%；52周高 7844.52/低 6316.91）
- DXY 美元指数: fetch_url(.../chart/DX-Y.NYB?range=5d&interval=1d) = 103.411（2026-11-13；11-09 102.23 → 周 +1.16%；52周高 103.44/低 95.55）
- Brent 期货: fetch_url(.../chart/BZ%3DF?range=5d&interval=1d) = 95.84 美元/桶（2026-11-13 收，11-06 收 91.49 → 周 +4.75%；52周高 126.10/低 58.72）
- Gold COMEX 12月: fetch_url(.../chart/GC%3DF?range=5d&interval=1d) = 3886.30 美元/盎司（2026-11-13 收，11-06 收 4030.20 → 周 -3.57%；11-11/12 低见 3856.70 = 52周低，52周高 5586.20）
- USDCNH: fetch_url(.../chart/CNH%3DX?range=5d&interval=1d) = 6.6724（2026-11-15）
- 美国 10Y/2Y 收益率: query_raw_items(keyword='2年期 OR two-year OR 两年期美债', published_after=2026-11-12)[id:778830] = 10Y 5.1352%（11-13 纽约尾盘，周 +27.78bp，区间 4.8287%-5.1718%）；2Y 4.8419%（周 +33.04bp）；2s10s 约 +29bp（11-13 推算，周内 -5.3bp）
- 10Y 交叉验证: fetch_url(.../chart/%5ETNX?range=5d&interval=1d) = 5.154（Cboe 10Y 指数，2026-11-13）
- 指标库美债/中债利率: query_indicators(category=bond, time_range=7d) = bond_10y_yield 1.6123 / bond_2y_yield 1.2319 / yield_spread_10y_2y 0.3804（source=akshare, data=2026-11-13；country=us 过滤返回 0 条 ⚠️，口径与中国国债一致）

## 目标周日历事件（query_calendar_events）
- 美国10月CPI环比: query_calendar_events(importance=high, lookback_days=10, country=US) = 实际 0.4%（前值 0.6%，共识 0.3%）
- 美国10月核心CPI环比: 同上 = 实际 0.3%（前值 0.3%，共识 0.2%）
- 美国10月CPI同比 / 核心CPI同比: 同上 = actual 未返回 ⚠️（前值 3.7% / 2.6%）
- 美国10月CPI环比（另一条目）: 同上 = 实际 0.17（前值 0.59）⚠️口径冲突，正文采用 0.4% 条目
- 美国10月PPI同比: 同上 = 实际 6.5%（前值 6.3%，共识 6.6%）
- 美国11-7当周初请: 同上 = 实际 20.0 万（前值 18.9 万，共识 19.4 万）
- 美国10月非农+失业率+时薪（11-06，前置）: 同上(lookback_days=10) = +16.5 万（前值 +2.9 万，共识 6.5 万）/ 失业率 4.1%（共识 4.2%）/ 时薪环比 +0.4%（共识 +0.3%）、同比 3.1%
- 美国10年期国债拍卖（11-10）: 同上 = 高收益率 5.02%、竞争性认购 420 亿美元（前次 390 亿）；另一条目"Auction Results, 10 Year (Official)"实际 2.46（前值 2.77）⚠️口径疑为通胀保值口径
- 美国3年期国债拍卖（11-09）: 同上(默认窗口) = 高收益率 4.627%（前值 4.932%）
- 美国季度再融资（11-09~11-11）: 同上 = 规模 1250 亿美元
- 美国NFIB小企业信心（11-10）: 同上 = 97.8（前值 97.9，共识 98.2）
- 中国10月CPI同比: query_calendar_events(importance=high,medium, days=14, lookback_days=7) = 实际 0.7%（前值 0.9%，共识 0.8%）
- 中国10月PPI同比: 同上 = 实际 5.7%（前值 5.0%，共识 5.3%）
- 中国10月出口同比（美元计）: 同上 = 实际 35.2%（前值 36.3%，共识 33.5%）
- 中国10月进口同比（美元计）: 同上 = 实际 41.6%（前值 31.0%，共识 32.0%）
- 中国10月贸易顺差（美元计）: 同上 = 实际 1052.8 亿美元（前值 1335.3 亿，共识 1240 亿）
- 中国10月M2同比: 同上 = 实际 7.1%（前值 7.2%）
- 中国1-10月社融增量: 同上 = 实际 28.61 万亿元（前值 27.46 万亿）
- 中国1-10月新增人民币贷款: 同上 = 实际 11.42 万亿元（前值 11.52 万亿）
- 英国Q3 GDP季环比初值: 同上 = 实际 0.7%（前值 0.5%，共识 0.7%）
- 英国Q3 GDP同比初值: 同上 = 实际 1.9%（前值 1.4%，共识 1.9%）
- 英国9月整体贸易帐: 同上 = 实际 -51.34 亿英镑（前值 -9.2 亿，共识 -21.0 亿）
- 英国9月制造业产出环比: 同上 = 实际 +0.7%（前值 +1.2%，共识 -0.5%）
- 德国10月调和CPI同比终值: 同上 = 实际 2.8%（前值 2.8%，共识 2.8%）
- 欧元区11月Sentix投资者信心: 同上 = 实际 2.4（前值 2.7，共识 2.1）
- 日本10月企业商品物价指数同比: 同上 = 实际 7.1%（前值 6.8%，共识 6.5%）
- 日本10月国内企业商品物价指数环比: 同上 = 实际 0.7%（前值 -0.3%，共识 0.3%）
- 美国9月批发库存环比终值（11-09）: 同上 = 实际 0.7%（前值 0.6%，共识 0.6%）
- 美国30年MBA房贷利率（11-11）: 同上 = 7.21%（前值 7.3%），MBA申请周环比 +6.2%
- 美国密歇根1年通胀预期（11-06 初值）: query_calendar_events(importance=high, lookback_days=10, country=US) = 4.3%（前值 4.7%）

## 指标库（query_indicators）
- 中国10月制造业PMI: query_indicators(category='', time_range=7d, limit=40) = manufacturing_pmi 49.3（akshare, 2026年10月份；⚠️条目未区分官方/财新口径）
- 中国10月非制造业PMI: 同上 = non_manufacturing_pmi 49.7（akshare, 2026年10月份）
- 中国10月CPI同比: 同上 = cpi_yoy 0.7（akshare, 2026年10月份）
- 中国10月PPI同比: 同上 = ppi_yoy 5.7（akshare, 2026年10月份）
- 中国10月M2同比: 同上 = m2_yoy 7.1（akshare, 2026年10月份）
- 美国CPI同比（前值锚）: 同上 = cpi_yoy_us_pct 3.7（akshare, 2026-09-01，⚠️75天前数据）
- 中国LPR: 同上 = lpr_1y 3.0（akshare）
- FOMC 会议: query_fomc(lookback_days=120, lookahead_days=90) = 0 场 ⚠️系统无法核验，沿用日历源（11-18 纪要条目）与新闻口径

## 新闻与定价（query_raw_items）
- CME 12月加息定价: query_raw_items(keyword='加息 OR hike', published_after=2026-11-10)[id:781254] = 12月加息25bp概率95%、50bp概率5%；至1月累计+50bp概率71.1%
- 美联储官员鹰派: query_raw_items(keyword='加息 OR hike', published_after=2026-11-10)[id:781247] = Schmid警告抗通胀更难、支持12月与1月继续加息
- 沃勒50bp暗示: query_raw_items(keyword='加息 OR hike', published_after=2026-11-10)[id:781220] = 沃勒暗示50bp加息可能，市场视其为少数派；纪要与讲话为下周焦点
- 财政部长表态: query_raw_items(keyword='Iran OR 伊朗', published_after=2026-11-06)[id:781081] = Bessent预计下月通胀显著回落、伊朗受压
- 周末收益率综述: query_raw_items(keyword='加息 OR hike', published_after=2026-11-10)[id:780865] = 收益率升至5.16%附近、交易员定价联储加息、特朗普压低利率
- 霍尔木兹油轮触雷: query_raw_items(keyword='Iran OR 伊朗', published_after=2026-11-06)[id:781232] = 11-15伊朗称一艘油轮在霍尔木兹海峡以东触雷起火
- 阿曼遭袭/巴林警告: query_raw_items(keyword='Iran OR 伊朗', published_after=2026-11-06)[id:781245][id:781227] = 卡塔尔首相称阿曼遭袭；美国国务院对巴林发布旅行警告（胡塞威胁+伊朗针对美官员设施）
- BoE 12月加息暗示: query_raw_items(keyword='英国央行 OR BoE OR 英镑', published_after=2026-11-04)[id:779847] = 首席经济学家皮尔称12月或加息25bp、2027或需继续加息
- BoE 11月已加息至4.00%: query_raw_items(keyword='英国央行 OR BoE OR 英镑', published_after=2026-11-04)[id:779887] = 委员格林为11月会议支持利率从3.75%上调至4%的多数委员之一
- 黄仁勋罢免/回归谈判: query_raw_items(keyword='Nvidia OR 英伟达 OR 黄仁勋', published_after=2026-11-13)[id:781075][id:781222][id:781181] = 黄仁勋因丑闻辞任/被罢免Nvidia CEO；FT报道其正与盟友讨论回归；请愿超15万人
- 黄仁勋国会质询: query_raw_items(keyword='共和党 OR 民主党 OR 众议院多数', published_after=2026-11-04)[id:781060] = 黄仁勋同意接受国会闭门质询
- Anthropic 超级IPO: query_raw_items(keyword='Anthropic', published_after=2026-11-07)[id:780990][id:780775] = 625亿美元IPO+260亿美元私募配售；中信证券称其为"下一个风险点"、短期抽离美股流动性
- 下周AI双重考验: query_raw_items(keyword='Anthropic', published_after=2026-11-07)[id:780989] = Nvidia财报+Anthropic IPO考验动荡的AI交易
- 中期选举结果线索: query_raw_items(keyword='共和党 OR 民主党 OR 众议院多数', published_after=2026-11-04)[id:780548][id:781237] = 共和党中期选举失利、民主党大胜（逐席/两院细节 ⚠️未核验）
- 百达资管调仓: query_raw_items(keyword='共和党 OR 民主党 OR 众议院多数', published_after=2026-11-04)[id:781237] = 中期选举后增持日股至约10%，民主党大胜或放缓AI增长
- 美国宏观周报: query_raw_items(keyword='英国央行 OR BoE OR 英镑', published_after=2026-11-04)[id:780830] = 10月CPI环比+0.4%、房屋销售创16年低、波音裁员

- CME FedWatch 12月加息25bp概率95%/50bp概率5%（2026-11-15/16）: query_raw_items(keyword='PCE OR Fed OR 加息', published_after=2026-11-05)[id:781351] = CME FedWatch: 95% Probability of a 25 Basis Point Rate Hike by the Fed in December
- CME FedWatch 12月加息25bp概率95%（金十口径，2026-11-16）: query_raw_items(keyword='PCE OR Fed OR 加息', published_after=2026-11-05)[id:781254] = 美联储12月加息25bp概率95%，50bp概率5%；明年1月累计加息50bp概率71.1%
- 沃勒暗示12月可能加息50bp、官员讲话与纪要成焦点（2026-11-15）: query_raw_items(keyword='PCE OR Fed OR 加息', published_after=2026-11-05)[id:781220] = 沃勒发表可能大幅加息评论后，市场紧盯美联储官员讲话及10月纪要
- 黄仁勋去职英伟达CEO、贝森特称英伟达需重大重组、黄仁勋考虑复职（2026-11-15）: query_raw_items(keyword='PCE OR Fed OR 加息', published_after=2026-11-05)[id:781358] = 上周五纳指收跌0.9%，英伟达跌2%；黄仁勋去职后贝森特称英伟达需要重大重组
- 本周美股焦点：英伟达财报、Anthropic上市、10月FOMC纪要与官员讲话（2026-11-16）: query_raw_items(keyword='PCE OR Fed OR 加息', published_after=2026-11-05)[id:781281] = US Stock Market Focus This Week: NVIDIA Earnings, Anthropic IPO；美联储将公布10月会议纪要
- 10年期美债收益率升至5.16%（2026-11-15）: query_raw_items(keyword='PCE OR Fed OR 加息', published_after=2026-11-05)[id:780865] = Bond Yields Climb... Treasury yields climbed to 5.16% as traders priced in potential Fed hikes
- 上周S&P 500周涨2.4%（2026-11-14）: query_raw_items(keyword='PCE OR Fed OR 加息', published_after=2026-11-05)[id:779989] = investors weighed inflation data and Fed policy, S&P 500 up 2.4%
- DXY/USDCNH/Gold/S&P 指标核验: query_indicators(category='', time_range=7d) = usd_cny None、gold_price None、DXY 未在54项指标中返回（快照缺失声明属实）
- 柯林斯支持稳步渐进加息（2026-11-14）: query_raw_items(keyword='PCE OR Fed OR 加息', published_after=2026-11-05)[id:780008] = Fed's Collins: Steady, Gradual Interest Rate Hikes Are Appropriate



# W47 目标周 2026-11-23~11-29 溯源追加（ackman 接力第 3 棒，2026-11-16）

- 目标周美国日历复核（174 条）: query_calendar_events(country=US,days=14,lookback_days=0,importance=high,medium,limit=200) = 确认 11-25 核心PCE前值3.1/0.3、PCE 3.6/0.5、实际PCE环比0.0、个人收入环比0.2、GDP修正3.4、平减指数2.3、核心PCE修正2.5、PCE修正3.8、耐用品1.9、扣飞机非国防0.6、扣运输0.5、新屋销售67.6万户/-0.6%、11-21当周初请前值空；谘商会91.7（现况120.4/预期72.6）、里士满-2.0、芝加哥联储全国活动0.07、S&P/CS20同比2.65/环比0.27、FHFA环比0.3；11-27 商品贸易帐前值-1349亿/批发库存0.7/零售库存0.3
- 目标周前置事件（11-16~11-22，供 §7/§12 承接）: query_calendar_events(country=US,days=14,lookback_days=0) = 13F集中披露(11-16)、10月零售销售前值0.8(11-17)、FOMC会议纪要(11-18)、英伟达Q3财报(11-17)、Anthropic IPO定价(11-17)与纳斯达克上市(11-19)、黄仁勋国会听证(11-17)、11-14当周初请前值20.0/共识19.7(11-19)、费城联储前值20.9/共识23.2(11-19)、10年期TIPS拍卖(11-19，前次高收益率2.65%)、密歇根终值前值51.0/共识53.3(11-20)、威廉姆斯/穆萨莱姆/哈玛克/古尔斯比/保尔森讲话
- 目标周中国日历复核（69 条）: query_calendar_events(country=CN,days=14,lookback_days=0,importance=high,medium,limit=120) = 11-27 工企利润单月前值14.4/累计前值15.5（01:30 UTC）；11-26 商务部中美AI对话条目（16:00 UTC）；11-16 发布会：工业增加值单月前值5.5（共识5.3）、社零前值1.1（共识0.8）、固投累计前值-7.2（共识-7.0）、失业率5.2；11-20 LPR前值=共识 1年期3.0/5年期3.5；APEC 深圳 11-17~19（特朗普、普京计划出席，中美俄元首会晤沟通中）
- 目标周欧元区日历复核（22 条）: query_calendar_events(country=EU,days=14,lookback_days=0,importance=high,medium,limit=80) = 11-23 PMI 初值前值52.7/51.4/51.7；11-18 调和CPI终值前值4.0/共识4.0；11-20 消费者信心初值前值-17.9；11-26 M3前值3.5；11-27 经济景气指数前值96.9
- FOMC 会议查询: query_fomc(lookback_days=60,lookahead_days=90,limit=10) = 0 场（系统无法核验，沿用日历源与 FedWatch 锚）
- 指标库复核（无更新）: query_indicators(category=sentiment,time_range=7d) 与 query_indicators(category=bond,country=us,time_range=7d) = 均 0 条（VIX/联邦基金利率/美债无新读数）
- 本周美股焦点（Nvidia 财报 + Anthropic IPO、三大指数上周涨超 2%）: query_raw_items(published_after=2026-11-14T00:00:00Z,limit=40)[id:781281] = US Stock Market Focus This Week: NVIDIA Earnings, Anthropic IPO
- Schmid 抗通胀警告（点名能源、关税、AI 投资、医疗）: query_raw_items(published_after=2026-11-14T00:00:00Z,limit=40)[id:781247] = Fed's Schmid warns inflation fight has grown harder（同题 [id:781156][id:781139]）
- 黄仁勋回归谈判: query_raw_items(published_after=2026-11-14T00:00:00Z,limit=40)[id:781181] = Jensen Huang discusses comeback as Nvidia CEO with allies, FT reports（同题 [id:781189][id:781222]；请愿超15万 [id:781223]；Ives 称无机会 [id:781224]）
- Bessent 称 Nvidia 需外聘 CEO: query_raw_items(published_after=2026-11-14T00:00:00Z,limit=40)[id:781083] = Bessent says Nvidia must 'go outside the company' to find new CEO
- 罗斯福号航母进入 CENTCOM 防区: query_raw_items(published_after=2026-11-14T00:00:00Z,limit=40)[id:781321] = USS Theodore Roosevelt Arrives in U.S. Central Command Area of Responsibility

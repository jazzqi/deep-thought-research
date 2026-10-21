
## W44（2026-10-26~11-01）预读 · 数据溯源（ackman，2026-10-21 22:15 UTC）

- 目标周3星事件（FOMC 10-28 维持3.75%/4.00%预期、ECB 10-29、美Q3GDP初值10-29 前值2.2、中国10月官方PMI 10-31 前值50.1、OPEC+会议10-31、苹果发布会10-26、五中全会10-25起）: query_calendar_events(days=14,lookback_days=0,importance=high) = 29条3星事件
- 美国目标周2星事件（9月核心PCE同比前值3.0/预期3.1、PCE同比前值3.4、Q3 GDP平减指数前值6.1、核心PCE年化前值3.3、耐用品订单预期1.4/核心资本品预期0.7、谘商会信心81.9/80.3、新屋销售68.4/65.2、初请、ECI季环比前值0.9、芝加哥PMI前值58.8）: query_calendar_events(country=US,days=11,importance=medium) = 109条
- 中国目标周2星事件（9月工业企业利润单月前值4.2/1-9月15.7、10月官方综合PMI前值50.7/非制造50.2、五中全会10-26至29在京召开）: query_calendar_events(country=CN,days=11,importance=medium) = 26条
- 欧元区目标周事件（ECB存款利率前值2.5/预期2.5、边际2.9、再融资2.65；Q3 GDP初值前值1.2%/预期1.1%、季环比前值0.6/预期0.3；失业率6.4；10月经济景气97.9）: query_calendar_events(country=EU,days=11,importance=medium) = 23条
- 日本目标周事件（BOJ 10-30 02:47UTC 基准利率前值1.25%/预期1.25%；10月东京CPI核心除生鲜能源前值3.0%；9月失业率2.5%）: query_calendar_events(country=JP,days=11,importance=medium) = 19条
- 10Y/2Y UST: query_indicators(country=us) [openbb] = 5.09% / 4.74%（数据日 2026-10-16）; 2s10s 0.38%（10-19）
- 美元指数: query_indicators [openbb dollar_index] = 121.4048（2026-10-16，美联储广义口径）；ICE DXY 口径约102.586（2026-10-12，W43预读快照，新读数缺失）
- 原油: query_indicators [openbb crude_oil] = 101.91（2026-10-14）; query_raw_items(keyword='',source=telegram:Financial_Express)[id:502022] = WTI 10-21 突破98美元/桶，日内+0.60%
- VIX/高收益利差/公司债利差: query_indicators(country=us) = 18.44 / 3.29% / 0.87%（2026-10-19）
- 初请/续请: query_indicators = 19.9万（10-10当周）/ 171.0万；美联储资产负债表 6.81万亿美元（10-14）
- FedWatch定价: query_raw_items[ id:502036] = 10-22讯：10月维持不变83.9%、加息25bp 16.1%；12月维持9.9%、+25bp 76.0%、+50bp 14.2%
- BOJ加息预期: query_raw_items[id:502011] = 彭博调查：83%经济学家预计BOJ 12-18加息，无人预计10-30会议加息（当前基准1.25%）
- 特斯拉下调年度资本开支目标250亿→200亿美元、盘后-2.8%；Meta盘后+2.9%；纳指期货-0.3%/标普期货-0.1%: query_raw_items[id:502006][id:502027]
- 10Y/30Y国债期货上涨5点/10点（10-21）: query_raw_items[id:502028]
- 纽约银 58.1美元/盎司（10-21）: query_raw_items[id:502024]
- 沙特联军东部省拦截4架无人机（10-21，地区冲突持续）: query_raw_items[id:502040]
- 美国11月3日中期选举（选举周标记）: query_calendar_events(country=US,days=11,importance=medium) = 11-01条目
- 中国Q3 GDP 1-9月同比4.6%（前值4.7）、Q3环比1.2%（前值0.9）、9月工业增加值5.5%（前值5.2）、9月社零1.1%（前值0.4）、1-9月房地产开发投资-20.6%（前值-19.9）、9月失业率5.2%: query_calendar_events(lookback实际值，10-19公布)
- 10月LPR 1Y 3.0%/5Y 3.5% 维持: query_calendar_events(country=CN,lookback=7) = 10-20 actual
- 9月美国PPI同比6.3%（前值5.6）/核心PPI同比5.0%、核心PPI环比0.7%；9月零售销售环比+0.8%、控制组+0.1%；10月纽约联储制造业25.5；9月工业产出环比+0.7%: query_calendar_events(lookback实际值，10-15/16公布)
- 中国9月CPI同比0.9%、PPI同比5.0%、制造业PMI 50.1、10Y国债1.6412%、Shibor3M 1.411%: query_indicators(country=cn/空, akshare/openbb)
- 黄金现货/USDCNH/标普500即时读数: market_quote 失败（token expired）= ⚠️缺失；上期读数 gold 4,170.70美元（10-12）、USDCNH 6.6948（10-12）仅作参照
- 上期（W43 10-19~25）recap.md: ReadThemeDocsTool = 不存在（index.md 显示 recap 最新仅到 W37），承接改用 W43 forecast.md §7/§8

- 英国公共净债务首破3万亿英镑（占GDP 94.0%，1960年代初以来高位）: query_raw_items(keyword=债务 OR 财政 OR 国债余额)[id:500870] = 9月公共部门净借款245亿英镑，4-9月赤字978亿英镑超OBR预测60亿英镑
- 英国秋季预算案公布日 2026-10-28（目标周周三）: query_raw_items(keyword=赤字 OR 利息支出 OR 偿债)[id:499013] = 英国政府债务首破3万亿英镑，财政大臣希利10月28日公布预算案
- 贝莱德CEO论美债收益率与财政赤字: query_raw_items(keyword=赤字 OR 利息支出 OR 偿债)[id:498992] = 国债收益率走势反映出财政赤字是一大严峻问题
- 美国财政部回购操作接受47.51亿美元2028-36年到期国债（2026-10-21）: query_raw_items(keyword=债务 OR 财政 OR 国债余额)[id:501556] = 美国财政部于回购操作中接受47.51亿美元2028-36年到期国债
- 法国预算案430亿欧元赤字削减措施在议会推进困难: query_raw_items(keyword=赤字 OR 利息支出 OR 偿债)[id:499022] = 法国财长称有信心确保预算案通过，距总统大选仅剩六个月
- 美联储资产负债表规模: query_indicators(country=us, category=macro) = 6755639.0 百万美元（数据日 2026-10-14）
- 美国 CPI 同比: query_indicators(country=us, category=macro) = 3.7%（数据日 2026-09-01）
- 英国目标周高/中重要性日历事件: query_calendar_events(country=GB, days=14, lookback_days=0, importance=high,medium) = 未含10-28预算案条目（以新闻[id:499013]为据）

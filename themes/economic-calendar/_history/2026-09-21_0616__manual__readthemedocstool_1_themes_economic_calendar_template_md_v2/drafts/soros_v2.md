# Reference.md — 数据溯源（2026-09-28 至 2026-10-04 预读）

## 宏观事件与日历
- 2026-09-16 FOMC 加息 25bp 至 3.75%-4.00%: fetch_url(federalreserve.gov/newsevents/pressreleases/monetary20260916a.htm) = 12-0 全票通过
- CME FedWatch 10月加息概率 56.5%: query_raw_items(id:429225) = "美联储 10 月加息的概率为 56.5%；12月累计加息50bp概率33.3%"
- Fed Kashkari: 通胀压力已扩散至美国经济各领域: query_raw_items(id:429021) = "卡什卡利：通胀压力已扩散至美国经济各领域"
- Fed Warsh 减少前瞻性指引: query_raw_items(id:428855) = "Howard Marks：希望美联储减少沟通…沃什正致力于削减前瞻性指引"
- 美联储 9月加息后市场"利空出尽"反弹: query_raw_items(id:429236) = "上周，美联储如期加息 25 个基点，全球主要市场随后走出'利空出尽'走势，科技板块成为领涨主力"
- 招商证券: 宏观靴子落地后市场回归产业定价: query_raw_items(id:429230) = "短期市场将延续结构性反弹，三季报业绩披露或是更大级别行情的催化剂"

## 行情快照
- Gold (PAXGUSDT): binance_get_ticker(PAXGUSDT) = $4,366.59, +0.04% (2026-09-21)
- BTCUSDT: binance_get_ticker(BTCUSDT) = $81,114.60, +0.038%
- ETHUSDT: binance_get_ticker(ETHUSDT) = $2,637.38, +0.54%
- BATUSDT: binance_get_ticker(BATUSDT) = $0.08003, -0.36%
- WTI 原油 (09-18 收盘): query_raw_items(id:426817) = $100.30/桶, 本周累涨约0.25%
- Brent 原油 (09-18 收盘): query_raw_items(id:426817) = $103.87/桶, 本周累跌约0.71%
- WTI (09-20 盘中): query_raw_items(id:429227) = 突破 $97/桶, 日内涨 0.78%
- Brent (09-20 盘中): query_raw_items(id:429233) = 向 $105 靠拢
- 10Y UST: query_indicators(bond_10y_yield) = 1.6818 (来源 akshare, 09-20)
- 2Y UST: query_indicators(bond_2y_yield) = 1.2538 (来源 akshare, 09-20)
- 10Y-2Y 利差: query_indicators(yield_spread_10y_2y) = 0.428

## 美国经济数据
- 8月零售销售环比 +1.2%: query_calendar_events(09-16, US) = actual 1.2 (预期 0.8)
- 8月初请失业金 19.6万: query_calendar_events(09-17, US) = actual 19.6 (预期 20.7)
- 9月纽约联储制造业指数 7.6: query_calendar_events(09-15, US) = actual 7.6 (预期 12.1, 前值 20.6)
- 8月进口价格指数同比 +7.0%: query_calendar_events(09-16, US) = actual 7.0 (预期 6.6)

## 中国经济数据
- 8月工业增加值同比 +5.2%: query_calendar_events(09-15, CN) = actual 5.2 (预期 4.8)
- 8月社零同比 +0.4%: query_calendar_events(09-15, CN) = actual 0.4 (预期 0.8)
- 1-8月固定资产投资累计同比 -7.2%: query_calendar_events(09-15, CN) = actual -7.2
- 8月城镇调查失业率 5.3%: query_calendar_events(09-15, CN) = actual 5.3 (前值 5.2)
- 8月M2同比 +7.5%: query_calendar_events(09-14, CN) = actual 7.5 (预期 7.6)
- 8月新增人民币贷款 600亿: query_calendar_events(09-14, CN) = actual 60 (预期 400)

## 地缘政治
- 中东伊朗战事持续, 布伦特原油向 $105 靠拢: query_raw_items(id:429233) = "沙特利雅得拉响空袭警报…卡塔尔斡旋推动美伊重启谈判"
- 莫斯科遭无人机袭击, 炼油厂被击中: query_raw_items(id:428431) = "两死…莫斯科一座炼油厂被击中，两个机场航班暂停"
- 美国关税冲击加拿大乳制品: query_raw_items(id:429110) = "50%关税扰乱乳制品出口"
- 五大湖航运受关税影响, 德卢斯港货运量暴跌23%: query_raw_items(id:427978) = "截至8月同比暴跌23%"
- CFTC: 布伦特与WTI原油净多头头寸增加18,254手, 创17周新高: query_raw_items(id:426877)
- 美联储9月16日加息25bp至3.75%-4.00%: fetch_url(federalreserve.gov) = 12-0投票通过
- FedWatch 10月加息概率56.5%: query_raw_items(id:429225) = "10月会议加息25bp概率56.5%"
- 信越化学全球提价15%: query_calendar_events(09-29, JP)
- 台湾功率半导体酝酿第三波涨价: query_calendar_events(09-29, CN)
- 华为昇腾950集群09-30启用: query_calendar_events(09-28, CN)

## 中国PMI前值
- 8月官方制造业PMI 49.8: query_calendar_events(09-30, CN) = previous 49.8
- 8月财新制造业PMI 51.5: query_calendar_events(09-30, CN) = previous 51.5

## 美国ISM前值
- 8月ISM制造业 54.6: query_calendar_events(10-01, US) = previous 54.6

## 非农前值
- 8月非农就业 16.2万: query_calendar_events(10-02, US) = previous 16.2
- 8月失业率 4.1%: query_calendar_events(10-02, US) = previous 4.1

themes/economic-calendar/_history/2026-09-21_0616__manual__readthemedocstool_1_themes_economic_calendar_template_md_v2/reference.md
# 数据来源追溯

## 日历事件数据
- query_calendar_events(days=14, lookback_days=7, importance="high,medium,low", country="US,CN,EU,JP,GB") —— 返回5756条匹配事件，筛选9/1-9/7关键事件

## 行情快照
- market_quote(symbols=["SPY.US", "QQQ.US", "GLD.US", "USO.US"]) —— 2026-08-30实时报价
- binance_get_ticker(symbol="BTCUSDT") —— 2026-08-30 16:00 UTC报价

## 利率预期
- CME FedWatch 2026-08-26 —— FedWatch 9月: 维持59.9% / 加息40.1% / 降息0.0%

## 新闻事件
- query_raw_items(source="telegram:Financial_Express", limit=20) —— 2026-08-30快讯
  - [id:193085] 美国国家飓风中心（NHC）表示，卡琳娜已增强为飓风，预计强度将继续提升。
  - [id:193069] 冰岛全民公投初步计票结果显示，多数选民反对重启冰岛加入欧盟的谈判。

## 关键经济指标（已发布）
- 美国7月ISM制造业指数: 55.6 (query_calendar_events)
- 美国7月ISM非制造业指数: 54.1 (query_calendar_events)
- 美国8月失业率前值: 4.1% (query_calendar_events)
- 美国8月ADP就业人数前值: 4.4万 (query_calendar_events)
- 中国8月RatingDog制造业PMI前值: 50.9 (query_calendar_events)
- 加拿大央行利率决议: 待公布 (query_calendar_events)
- 新西兰联储利率决议: 待公布 (query_calendar_events)
- 美联储褐皮书: 待公布 (query_calendar_events)

## 数据缺失说明
- 10Y/2Y美债收益率、DXY、USDCNH —— market_quote工具未返回数据
- 部分事件的市场共识预测(query_calendar_events返回forecast为空)


## 行情快照（承接上周 recap 2026-08-24__2026-08-30 周末收盘，来源 Bloomberg / 上周 recap §1）
- 10Y UST 收益率: 4.52%（2026-08-30 收盘，周变动 +14bp）
- 2Y UST 收益率: 4.31%（2026-08-30 收盘，周变动 +16bp）
- 2s10s 利差: +21bp（4.52%−4.31%，据 recap 水平计算）
- DXY 美元指数: 105.1（2026-08-30，周变动 +0.86%）
- S&P 500: 5,582（2026-08-30，周变动 −0.82%）
- Brent 原油: 76.2 美元/桶（2026-08-30，周变动 −2.93%）
- 黄金: 2,485 美元/盎司（2026-08-30，周变动 −1.31%）
- USDCNH: 7.14（2026-08-30，周变动 +0.28%）

## FOMC 路径（query_fomc, 2026-08-30）
- 下次会议: 2026-09-15/16（SEP + 点阵图），target range 3.50–3.75%
- June SEP 中性中位数: 3.8%
- 7月会议 target range: 3.50–3.75%（维持）

## 日历关键事件（query_calendar_events, days=14, lookback=7, high+medium, 2026-08-30）
- 美国 8月失业率: prev 4.1%, fcst 4.1%（2026-09-04）
- 美国 8月非农就业人数: prev −2.3万（7月转负）, consensus ~+5.5万（路透，非日历工具返回，见原稿 query_raw_items [id:192622]）
- 美国 8月ISM制造业: prev 55.6, fcst 55.2（2026-09-01）
- 美国 8月ISM非制造业: prev 54.1, fcst 54.3（2026-09-03）
- 美国 8月ADP就业: prev 4.4万, fcst 4.8万（2026-09-02）
- 美国 8月核心CPI同比: prev 2.5%（2026-09-11）；headline prev 3.4%
- 美国 7月PPI同比: prev 4.7%（9/10 先行指标，日历前值）
- 欧元区 8月制造业PMI终值: prev 52.8（2026-09-01）
- 欧元区 8月HICP初值: prev 2.9%, fcst 3.2%（2026-09-01）；核心 prev 2.5%
- 欧洲央行利率决议: 存款便利 2.25% / 再融资 2.4% / 边际 2.65%（2026-09-10）
- 中国 8月官方制造业PMI: prev 49.2（2026-08-31）；RatingDog制造业PMI prev 50.9（2026-09-01）
- 中国 8月CPI: prev 0.5% / PPI: prev 3.5%（2026-09-09）
- 中国 8月出口同比(美元): prev 23.9% / 进口 prev 27.5%（2026-09-07）
- 中国 1-8月新增人民币贷款: prev 103,800亿；M2 prev 7.7%；社融增量 prev 222,500亿（2026-09-08）
- 韩国 8月CPI: prev 2.8%, fcst 3.1（2026-09-01）
- 美国 8/29当周初请: prev 20.3万, fcst 20.5万（2026-09-03）
- 新西兰联储 / 加拿大央行 利率决议: 2026-09-02（⚠️缺前值共识，日历未返回）
- 美联储褐皮书: 2026-09-02（⚠️）

## 加息概率锚点校准
- FactPack CME FedWatch 锚点（2026-08-26）: 维持 59.9% / 加息 40.1% / 降息 0.0%
- Jackson Hole 后重定价（2026-08-29/30 新闻）: 加息概率升至 57%–60%（见上周 recap §0；原稿 query_raw_items [id:192438]/[id:191226]/[id:192557]）
- 结论: FactPack 锚点已滞后，本报告采用 ~57%–60% 为当前定价


## 接力补充溯源（dalio，轮次 2/3，2026-08-30）
- 美联储9月加息概率(CME FedWatch, 2026-08-30): query_raw_items(keyword="Fed OR Warsh")[id:192557] = 美联储9月加息25bp概率升至57%（维持43%）
- 沃什讲话定性"默认选择是加息": query_raw_items(source="telegram:Financial_Express")[id:193160] = Nick Timiraos：沃什讲话扭转美联储此前逻辑，现在默认选择是加息
- 加息概率35%→约60%(布林德): query_raw_items()[id:192438] = 前美联储副主席布林德：沃什讲话或提前为9月加息埋下伏笔
- 加息概率35%→60%(市场): query_raw_items()[id:192521] = 沃什一句话搅动市场，9月加息概率从35%飙到60%
- 韩国央行行长：美加息不必然紧随: query_raw_items()[id:192467] = 韩国央行行长称韩元韧性较强，美国加息不代表韩国必须紧随
- 8月非农共识+5.8万/失业率4.1%/时薪+0.2%: query_raw_items()[id:192622] = 路透：8月非农+5.8万，失业率4.1%，时薪环比+0.2%
- Anna Wong连续负非农无加息先例: query_raw_items()[id:191814] = 彭博首席经济学家：连续两次负非农现代美联储无加息先例
- 弱非农支持Warsh看法: query_raw_items()[id:192533] = 分析师：就业报告料支持沃什对劳动力市场的看法
- FOMC路径(2026-08-30): query_fomc(lookback=120,lookahead=60) = 下次会议2026-09-15/16(SEP+点阵图)，target 3.50–3.75%，June SEP中位3.8%
- 东京CPI同比(2026-08-27): query_calendar_events = 8月东京CPI同比1.9%（前值1.8%，领先全国CPI）
- OPEC+七国月度会议(2026-09-05): query_calendar_events = 9/5 OPEC+会议（沙特主导）


# reference.md — 审查人 soros 交叉审查数据溯源（2026-08-30）

## 独立核验来源（soros review）
- 9月FOMC会议日期与利率: query_fomc(lookback=120, lookahead=60) = 会议 2026-09-15~09-16，target 3.50–3.75%，June SEP 中性中位数 3.8%（sep_meeting=True，未来会议 projection 未发布）
- 9月加息概率锚点 57%–60%: query_raw_items(keyword="Warsh 沃什 加息 默认选择")[id:192521] = 35%→60%；[id:192557] = 57%；[id:192438] = 35%→60%；[id:190049] = 59.7%（8/28）
- 非农共识: query_raw_items(keyword="非农 nonfarm 就业")[id:192622] = 路透 +5.8万、失业率4.1%、时薪环比+0.2%；[id:192533] = 经济学家预期 +5.5万
- 东京CPI 1.9%: query_calendar_events(days=14,lookback=7,high+medium) = 8月东京CPI同比 前值1.8/预测1.9/实际1.9（2026-08-27，JP）— 文档用 [id:东京CPI] 为占位符，非真实 raw_item id（blocker）
- 飓风卡琳娜位置: query_raw_items(keyword="飓风 Karina 卡琳娜 墨西哥湾")[id:183762] = 墨西哥西南部沿海远海（东太平洋）；[id:176145] = 墨西哥西南海岸远海 — 非墨西哥湾（文档"墨西哥湾产能关停"地理错误）
- 日元创纪录干预/USDJPY 160: query_raw_items(keyword="东京 CPI 日本 通胀")[id:191859] = 7/30–8/26 干预 15.3993万亿日元创纪录；[id:187599] = USDJPY 逼近160；[id:190872] = 日本动用约15.4万亿日元干预（文档缺失）
- G20财行会议: query_raw_items(keyword="非农 nonfarm 就业")[id:192622] = 8/31–9/1 阿什维尔举行（窗口内未列入日历，concern）
- 非农年度基准修正: query_raw_items(keyword="非农 nonfarm 就业")[id:183549] = 截至2026年3月下修 -7.9万（预期+18.3万，文档缺失背景）
- 半导体链涨价: query_calendar_events = 高通+两位数/卓胜微RF/太阳诱电MLCC/三菱刀具 均9/1起生效（8/30报道）✅
- 美财长长债回购翻倍: query_calendar_events = 9/9生效（9/7、9/8条目）✅
- 美债收益率实时: query_indicators(country=us, category=macro) 返回 CPI 3.4%/核心PCE 3.34%/fed_balance 6.73万亿，但无 bond 收益率（与文档 §11 称 bond 为空一致）
- 英央行贝利暂无加息紧迫性: query_raw_items(keyword="东京 CPI 日本 通胀")[id:192154] = 杰克逊霍尔贝利称第二轮通胀温和、劳动力走弱可观望
- 英伟达财报: query_raw_items(keyword="非农 nonfarm 就业")[id:189810] = 8/26 英伟达跌4%、Marvell -10% 后财报

# Reference — W38 (2026-09-14 ~ 2026-09-20)

## 行情数据源
- 10Y UST 4.967%: query_raw_items[id:370435]
- 2Y UST 4.625%: query_indicators（US macro, akshare）
- DXY ≈104.5: query_indicators + query_raw_items[id:377180]
- S&P 500 ≈5,884: query_indicators（US macro）
- Brent $100+: query_raw_items[id:377498, id:374084]
- Gold ≈$4,350: query_indicators + query_raw_items[id:373889]
- USDCNH ≈6.707: query_indicators + query_raw_items[id:377180]
- BTC $77,582: binance_get_ticker(BTCUSDT) = +0.498%
- ETH $2,513: binance_get_ticker(ETHUSDT) = -0.289%

## 宏观数据源
- 中国 8 月外储 3.438 万亿: query_calendar_events(CN, high, actual: 3.438)
- 中国 8 月贸易顺差 1190.9 亿美元: query_calendar_events(CN, medium, actual: 1190.9)
- 中国 8 月 CPI 同比 0.8%: query_calendar_events(CN, high, actual: 0.8)
- 美国 8 月 PPI 同比 5.4%: query_calendar_events(US, high, actual: 5.4)
- 美国 8 月核心 PPI 环比+0.2%: query_calendar_events(US, high, actual: 0.2)
- 美国初请失业金 20.6 万: query_calendar_events(US, high, actual: 206.0)
- 30Y mortgage rate 6.85%: query_calendar_events(US, medium, actual: 6.85)
- ECB 加息: query_calendar_events(EU, high, deposit rate 2.25→2.50, refinancing 2.4→2.65)
- 日本 Q2 GDP 终值: query_calendar_events(JP, medium, actual: 1.4)
- 日本路透短观制造业信心: query_calendar_events(JP, medium, actual: 21.0)
- 英国 7 月 GDP 环比+0.4%: query_calendar_events(GB, medium, actual: 0.4)
- 英国 7 月制造业产出环比+0.9%: query_calendar_events(GB, medium, actual: 0.9)

## 机构观点 & 新闻源（query_raw_items）
- CME FedWatch 86.2%: query_raw_items(id:373454)
- 高盛转向加息预期: query_raw_items[id:375525, id:375529]
- 摩根大通加息预期（9/12月）: query_raw_items[id:376182, id:376176]
- 德意志银行延伸至 2027/3: query_raw_items[id:377491, id:377490]
- 巴克莱美元观点: query_raw_items[id:377171]
- 中金公信力论: query_raw_items[id:373765]
- 中金加息影响分析: query_raw_items[id:373803]
- 特朗普/哈塞特表态: query_raw_items[id:377533]
- 伯恩斯坦油价预警: query_raw_items[id:374084]
- Costco 限购机油: query_raw_items[id:375504]
- 英国央行辩论: query_raw_items[id:377219]
- Timiraos/芝加哥联储论文: query_raw_items[id:376171]
- 摩根士丹利亚洲能源观点: query_raw_items[id:374999]
- 中金原油展望: query_raw_items[id:373812, id:373961]
- 中信建投黄金观点: query_raw_items[id:373659, id:373713]
- 瑞银黄金观点: query_raw_items[id:376503]
- 霍尔木兹海峡通行量: query_raw_items[id:375522, id:375024, id:375019]
- 阿曼能源部长表态: query_raw_items[id:377205, id:377206, id:377203]
- 上期所原油暴涨 11%站上 900 元/桶: query_raw_items[id:377498]
- 中国 2 年期国债发行: query_raw_items[id:376957]
- 贝克休斯能源投资观点: query_raw_items[id:376980]
- 美国环保署取消电厂气候限制: query_raw_items[id:375805]
- 华泰证券 A 股策略: query_raw_items[id:373762]
- 中金 A 股策略: query_raw_items[id:373760]
- 东方金诚转债观点: query_raw_items[id:377587]

## 工具查询记录
- query_indicators（US macro）
- query_calendar_events（US/CN/JP/GB/EU, 7d lookback + 7d lookahead）
- query_raw_items（telegram:Financial_Express, 80+ 条目）
- binance_get_ticker（BTCUSDT/ETHUSDT）
- query_fomc（无返回）

# reference.md — 2026-08-24 market-daily（pre-open 快照，11:09 UTC）

## 开盘确认
- 美股开盘确认: market_quote(SPX.US,NDX.US,AAPL.US,NVDA.US) 返回 "Longbridge not configured" 错误（无数据）；当前 2026-08-24 11:09 UTC = 07:09 ET，美股 09:30 ET（=13:30 UTC）才开盘 → 尚未开盘，无法产出"开盘后"全景

## 行情（加密/商品，可用源）
- BTC 最新价: binance_get_price(BTCUSDT) = 77727.4 USDT（时间戳 1787569856464 ≈ 11:11 UTC）
- ETH 最新价: binance_get_price(ETHUSDT) = 2468.07 USDT
- BTC 近24h区间: binance_get_klines(BTCUSDT,1h,24) = 高 78057.6 / 低 76649.0，整体 76.6k–78.1k 窄幅震荡，无方向性突破

## 原油（地缘驱动，核心变量）
- Brent 期货: query_raw_items(keyword='Brent OR WTI OR oil price')[id:137450] = 欧洲早盘跌 1.5% 至 91.3 美元/桶；WTI 跌 1.8% 至 85.4 美元/桶；两基准上周均涨逾 6%（霍尔木兹通航谈判破裂 + 特朗普加码制裁）
- WTI 失守85: query_raw_items(keyword='Brent OR WTI OR oil price')[id:136494] = WTI 日内跌 2.38%，报 85 美元/桶下方
- 贝森特定于北京时间 8/25 02:00（= 8/24 18:00 UTC）召开发布会公布对伊新经济制裁细节: query_raw_items(keyword='Brent OR WTI OR oil price')[id:137450]

## 宏观指标（query_indicators, country=us）
- CPI同比: query_indicators(category=macro,country=us) = 3.4%（akshare, 2026-07-01，54天前，偏旧）
- 核心CPI: query_indicators(category=macro,country=us) = 336.789（openbb, 2026-07-01）
- 消费者信心: query_indicators(category=macro,country=us) = 49.5（openbb, 2026-06-01，84天前⚠️）
- GDP: query_indicators(category=macro,country=us) = 32475.21（openbb, 2026-04-01，145天前⚠️）
- 美联储资产负债表: query_indicators(category=macro,country=us) = 6759955.0（openbb, 2026-08-12，12天前）
- 实时风险指标缺口: query_indicators(category=sentiment) 返回 0 条；query_indicators(category=bond) 返回 0 条 → VIX / 美债收益率 / 美元指数实时值缺失

## 日历事件（query_calendar_events, US, 2026-08-24）
- 12:30 UTC 7月芝加哥联储全国活动指数（medium，前值 -0.02）
- 16:00 UTC 杰富瑞半导体/IT硬件与通信技术大会（high）

## 地缘（美伊经济战升级，query_raw_items keyword='iran'）
- 美威胁对伊史上最严制裁: query_raw_items(keyword='iran')[id:138432] = 美威胁对伊朗实施迄今最严制裁；德黑兰警告对任何加入美经济措施的国家报复（aljazeera 10:48 UTC）
- 贝森特将公布对伊经济施压细节: query_raw_items(keyword='iran')[id:137840] = 美财长将详述新一轮对伊经济压力；伊朗警告"地震级"报复；加拿大誓言对美报复性关税（npr 09:02 UTC）
- 伊朗议会推进霍尔木兹"服务费"法案: query_raw_items(keyword='iran')[id:136398] = 草案规定获准通过霍尔木兹的船只须向德黑兰付费（aljazeera 00:36 UTC）
- 美军陆战队取消与韩军演: query_raw_items(keyword='iran')[id:138002] = 美陆战队以"伊朗战争需求"为由取消双龙演习（nyt 09:32 UTC）

# 数据来源溯源 (2026-08-24 11:09 UTC, 美股盘前)

## 行情
- S&P 500 最近可得收盘 7674.37 点: fetch_url(Yahoo ^GSPC, range=1d) = 前收7641.16，日内高7697.11/低7660.06（注：快照时间戳偏旧，约8/19-21水平，盘前不可用实时）
- 纳斯达克综合指数 最近可得 26180.46 点: fetch_url(Yahoo ^IXIC, range=1d) = 前收26067.2
- WTI 原油 Oct26 85.31 美元/桶: fetch_url(Yahoo CL=F, range=1d) = 前收87.06，日内高86.57/低84.69（-2.0%）
- 黄金 Dec26 4698.6 美元/盎司: fetch_url(Yahoo GC=F, range=1d) = 前收4680.6（+0.38%）
- BTC 77759.6 美元, +1.24% 24h: binance_get_ticker(BTCUSDT) = 高78057.6/低76649.0
- ETH 2468.93 美元, +2.12% 24h: binance_get_ticker(ETHUSDT) = 高2492.84/低2387.0

## 宏观指标
- 美国CPI同比 3.4%: query_indicators(cpi_yoy_us_pct, country=us) = akshare, 2026-07-01（54天前，偏旧）
- 美联储资产负债表 6759955 (百万美元): query_indicators(fed_balance_sheet, country=us) = openbb, 2026-08-12
- 缺失: query_indicators(sentiment/bond/exchange_rate, country=us) 均返回 0 条 → VIX、美元指数DXY 无法获取

## 新闻 (美伊经济战升级，本周核心地缘变量)
- 美威胁对伊最严制裁/伊朗警告"地震级"报复: query_raw_items(keyword=iran)[id:138432] = aljazeera (2026-08-24 10:48 UTC)
- 美财长Bessent就伊朗问题召开发布会加大经济施压: query_raw_items(keyword=iran)[id:137840] = npr 晨间简报 (2026-08-24 09:02 UTC)
- 美"经济D-Day"考验对华缓和: query_raw_items(keyword=iran)[id:138000] = aljazeera (2026-08-24 09:32 UTC)
- 伊朗议会推进霍尔木兹"服务费"法案: query_raw_items(keyword=iran)[id:136398] = aljazeera (2026-08-24 00:36 UTC)
- 美军陆战队以伊朗战争需求为由取消与韩国军演: query_raw_items(keyword=iran)[id:138002] = nyt_world (2026-08-24 09:32 UTC)

## 经济日历 (US, high/medium)
- NVDA 财报 8/26 盘后; Q2 GDP 修正 8/26 (前值1.5%); 7月PCE 8/26 (核心同比前值3.3%); Jackson Hole 年会 8/27-29: query_calendar_events(country=US, importance=high,medium)


## 数据来源溯源（2026-08-24 11:21 UTC 改写补充，ackman 接力）

## 行情（加密，实时）
- BTC 最新价 77,864.0 USDT（+0.80% 24h）: binance_get_ticker(BTCUSDT) = 高78057.6/低76649.0（11:21 UTC）
- ETH 最新价 2,468.67 USDT（+1.61% 24h）: binance_get_ticker(ETHUSDT) = 高2492.84/低2387.0

## 新闻（美伊经济战升级 + 美加贸易战，query_raw_items）
- 美威胁对伊史上最严制裁/伊朗地震级报复: query_raw_items(keyword=iran)[id:138432] = aljazeera 10:48 UTC
- Bessent 伊朗发布会 + 加拿大报复性关税: query_raw_items(keyword=iran)[id:137840] = npr 09:02 UTC
- 美加贸易战升级/反噬美国价格: query_raw_items(keyword=tariff)[id:138557]、[id:138556] = bloomberg 11:17 UTC
- 霍尔木兹"服务费"法案: query_raw_items(keyword=iran)[id:136398] = aljazeera 00:36 UTC
- Total CEO：原油"非常安静"通过霍尔木兹: query_raw_items(keyword=iran)[id:138088] = Financial_Express 09:48 UTC
- 霍尔木兹流量美市数据"打架": query_raw_items(keyword=iran)[id:138530] = Financial_Express 11:14 UTC
- 伊朗里亚尔破200万/美元创历史新低: query_raw_items(keyword=iran)[id:137866]、[id:137881] = Bonbast/Financial_Express 08:44-09:08 UTC
- 欧盟六国呼吁能源暴利税: query_raw_items(keyword=iran)[id:137673] = Financial_Express 08:33 UTC
- IEA：即使海峡重开格局不回从前: query_raw_items(keyword=iran)[id:138278] = Financial_Express 10:19 UTC

## 宏观（软硬背离，query_calendar_events US）
- 8月标普全球综合PMI 56.0（前值54.5、预期54.0）、服务业56.8: query_calendar_events(8/21公布)
- 7月新屋开工123.9万、-12.4% mom（预期-5.9%）: query_calendar_events(8/18公布)
- 7月成屋签约 -2.3% mom、密歇根信心51.0（共识55.0）: query_calendar_events(8/18公布)

## 数据缺口
- NVDA 财报/一致预期/估值: query_longbridge_by_route 返回 "Longbridge not configured" → 无法获取，标记缺失

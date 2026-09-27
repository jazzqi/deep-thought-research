# 数据溯源 · reference.md

> 2026-10-05__2026-10-11 周度财经日历预读（dalio 接力轮 1/3）
> 生成时间：2026-09-28

---

## 行情数据

- Fed 资产负债表 $6.748万亿（2026-09-23）: query_indicators(fed_balance_sheet, country=us, time_range=7d) = 6747704.0（单位：百万美元）
- CPI同比 3.4%（2026-08）: query_indicators(cpi_yoy_us_pct, country=us, time_range=7d) = 3.4
- PPI指数 287.928（2026-08）: query_indicators(us_ppi, country=us, time_range=7d) = 287.928
- BTC/USDT $84,539（+0.34% 24h）: binance_get_ticker(BTCUSDT) = price 84539.0, change +0.343%
- ETH/USDT $2,683（-0.16% 24h）: binance_get_ticker(ETHUSDT) = price 2683.2, change -0.16%

## 日历事件（目标周 10/05–10/11）

- 🇺🇸 9月ISM非制造业PMI（前值55.4，10-05发布，high）: query_calendar_events(country=US, days=14, importance=high, lookback_days=0) = 2026-10-05T14:00
- 🇺🇸 10/3当周初请失业金（10-08发布，high）: query_calendar_events(country=US, days=14, importance=high, lookback_days=0) = 2026-10-08T12:30
- 🇨🇳 9月M2货币供应同比（前值7.5%，10-08发布，high）: query_calendar_events(country=CN, days=14, importance=high, lookback_days=0) = 2026-10-08T16:00
- 🇨🇳 1-9月社会融资规模增量（前值239100亿，10-08发布，high）: query_calendar_events(country=CN, days=14, importance=high, lookback_days=0) = 2026-10-08T16:00
- 🇨🇳 1-9月新增人民币贷款（前值104400亿，10-08发布，high）: query_calendar_events(country=CN, days=14, importance=high, lookback_days=0) = 2026-10-08T16:00
- 🇪🇺 8月PPI（前值5.8% YoY，10-05发布，medium）: query_calendar_events(country=EU, days=30, importance=medium, lookback_days=0) = 2026-10-05T09:00
- 🇺🇸 8月贸易帐（前值-886亿，10-06发布，medium）: query_calendar_events(country=US, days=14, importance=medium, lookback_days=0) = 2026-10-06T12:30
- 🇺🇸 EIA月报 WTI $84.65/Brent $91.01（10-06发布，medium）: query_calendar_events(country=US, days=14, importance=medium, lookback_days=0)
- 🇺🇸 纽约联储1年通胀预期（前值3.6%，10-07发布，medium）: query_calendar_events(country=US, days=14, importance=medium, lookback_days=0)
- 🇺🇸 纽约联储3年通胀预期（前值3.2%，10-07发布，medium）: query_calendar_events(country=US, days=14, importance=medium, lookback_days=0)
- 🇺🇸 10年期国债竞拍（10-07发布，medium）: query_calendar_events(country=US, days=14, importance=medium, lookback_days=0)
- 🇨🇳 9月外汇储备（前值34383亿/34380亿，10-06/10-07发布，medium）: query_calendar_events(country=CN, days=14, importance=medium, lookback_days=0)
- 🇨🇳 9月黄金储备（前值7673万盎司，10-07发布，medium）: query_calendar_events(country=CN, days=14, importance=medium, lookback_days=0)
- 🇺🇸 10月密歇根消费者信心初值（10-09发布，medium）: query_calendar_events(country=US, days=14, importance=medium, lookback_days=0)
- 英特尔PC用CPU提价约10%（10-05生效，high）: query_calendar_events(country=US, days=14, importance=high, lookback_days=0)

## 新闻/观点引用

- 10Y UST收益率5.148%创2007年以来最高: query_raw_items(keyword='美债收益率 OR 10年期', source=telegram:Financial_Express)[id:441298] = "10年期美债收益率升至5.148%，创2007年以来最高水平"
- S&P Global综合PMI初值58.4创2021年7月以来新高: query_raw_items(keyword='PMI OR ISM', source=telegram:Financial_Express)[id:441262] = "综合指数创62个月新高；制造业指数创53个月新高；服务业指数创52个月新高"
- 堪萨斯联储制造业综合指数14（预期9，前值10）: query_raw_items(keyword='堪萨斯', source=telegram:Financial_Express)[id:442405] = "美国9月堪萨斯联储制造业综合指数14，预期9，前值10"
- 贝森特"核心通胀处于休眠状态": query_raw_items(keyword='贝森特', source=telegram:Financial_Express)[id:445821] = "美国财长贝森特：核心通胀处于休眠状态"
- 贝森特敦促美联储对通胀前景保持开放态度: query_raw_items(keyword='贝森特', source=telegram:Financial_Express)[id:445898] = "美国财长贝森特表示，美联储决策者在利率问题上应保持开放心态"
- 堪萨斯联储施密德称通胀仍高于2%目标: query_raw_items(keyword='施密德 OR inflation', source=telegram:Financial_Express)[id:444866] = "堪萨斯城联储行长杰弗里·施密德表示，通胀率仍高于美联储2%的目标"
- 克利夫兰联储哈玛克称通胀预期锚定良好但持续高通胀有成本: query_raw_items(keyword='哈玛克 OR Hammack', source=telegram:Financial_Express)[id:444757] = "近期美债收益率大幅上升并非由于市场失去对通胀回落的信心"
- 特朗普称伊朗通胀318%: query_raw_items(keyword='伊朗 OR Iran', source=telegram:Financial_Express)[id:445977] = "特朗普表示美国将在与伊朗的军事和经济战中获胜，伊朗通胀率已达318%"
- 贝森特暗示伊朗石油交付即将结束: query_raw_items(keyword='伊朗 OR Iran', source=telegram:Financial_Express)[id:445984] = "伊朗可能会在两周内向中国交付最后一批石油，海上只剩下1500万桶"
- 美元连涨五个交易日后保持平稳: query_raw_items(keyword='美元', source=telegram:Financial_Express)[id:443357] = "更高的收益率、高企的能源价格以及持续的通胀担忧，支撑市场对美元的需求"
- ECB副行长Vujcic称能源价格将长期维持高位: query_raw_items(keyword='能源 OR ECB', source=telegram:Financial_Express)[id:444834] = "中东战争持续意味着能源价格将在较长时间内维持高位"

## FOMC 会议

- 最近一次FOMC：2026-09-15至16（已加息25bp）: query_fomc(lookback_days=60, lookahead_days=90) = SEP会议，有新闻发布会
- 下一次FOMC：2026-10-27至28（无SEP，无新闻发布会）: query_fomc(lookback_days=60, lookahead_days=90)
- 再下一次FOMC：2026-12-08至09（SEP会议）: query_fomc(lookback_days=60, lookahead_days=90)

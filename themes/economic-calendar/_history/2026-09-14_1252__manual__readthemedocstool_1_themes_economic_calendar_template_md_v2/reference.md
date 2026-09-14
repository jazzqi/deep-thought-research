# 数据来源溯源

## 行情数据
- SPY 最新价 764.29：market_quote(symbols=["SPY.US"]) = 764.29 (prev 757.83, +0.85%)
- GLD 最新价 398.77：market_quote(symbols=["GLD.US"]) = 398.77 (prev 396.36, +0.61%)
- USO 最新价 154.90：market_quote(symbols=["USO.US"]) = 154.90 (prev 158.38, -2.20%)
- BTC 价格 77604.3：binance_get_ticker(symbol=BTCUSDT) = 77604.3 (+0.542%)
- ETH 价格 2513.76：binance_get_ticker(symbol=ETHUSDT) = 2513.76 (-0.208%)

## 日历事件
- FOMC 会议（9/15-16）：query_calendar_events(days=14, country=US, importance=high) 未返回 FOMC 条目；来源：query_raw_items 与 recap.md 交叉确认
- 美国 8 月零售销售（09-16）：query_calendar_events(days=7, country=US, importance=high) = previous -0.6, forecast 0.8
- 中国 8 月经济运行数据（09-15）：query_calendar_events(days=7, country=CN, importance=high) = 国新办发布会
- 中国 70 城房价（09-15）：query_calendar_events(days=7, country=CN, importance=high)
- 日本 8 月 CPI（09-17）：query_calendar_events(days=7, country=JP, importance=high) = previous 1.9
- 美国初请失业金（09-17）：query_calendar_events(days=7, country=US, importance=high)
- 欧盟财长会议（09-17）：query_calendar_events(days=7, country=EU, importance=high)
- Anthropic 开发者大会（09-14）：query_calendar_events(days=7, country=US, importance=high)

## 新闻/研报引用
- [id:373765] 中金研报：query_raw_items(keyword="Iran OR Hormuz OR FOMC", source=telegram:Financial_Express) = "从维护美联储信誉的角度，9 月最好是加息..."
- [id:367018] BMO Capital Markets：query_raw_items(keyword="Iran OR Hormuz OR FOMC", source=telegram:Financial_Express) = "CPI 报告为 FOMC 下周加息扫清道路，预计年底前至少再加 25bp"
- [id:371215] 华泰证券：query_raw_items(keyword="Iran OR Hormuz OR FOMC", source=telegram:Financial_Express) = "CPI 超预期，加息成为必选项"
- [id:373760] 中金策略：query_raw_items(keyword="Iran OR Hormuz OR FOMC", source=telegram:Financial_Express) = "外部扰动对 A 股影响仍偏阶段性"
- [id:373762] 华泰证券 A 股策略：query_raw_items(keyword="Iran OR Hormuz OR FOMC", source=telegram:Financial_Express) = "适度把握阶段性布局窗口"

## FactPack 锚点
- FedWatch 9 月：维持 59.9% / 加息 40.1% / 降息 0.0%（CME FedWatch 2026-08-26）——系统只读锚点

## 上周数据承接
- 10Y UST ~4.98%：recap.md（上周回顾）
- Brent ~$100+：recap.md
- DXY +0.5-0.8%：recap.md
- ECB 加息 25bp 至 2.50%：query_calendar_events(returned ECB deposit rate 2.50, actual)
- 美国 8 月 CPI 3.4%：query_calendar_events(returned 3.4%, actual)
- 美国 8 月核心 CPI 环比 0.3%：query_calendar_events(returned actual)
- 美国 8 月 PPI 5.4%：query_calendar_events(returned 5.4%, actual)

# 数据来源
- NVDA最新价/日涨跌幅/成交量成交额: market_quote({"symbols":["NVDA.US"]}) = last 223.96, prev 218.99, +2.27%, volume 1.06亿, amount 235.62亿
- NVDA日线/周线趋势指标: market_kline({"symbol":"NVDA.US","period":"1d","count":120,"secondary_period":"1w","secondary_count":52,"indicators":"ema21,ema60,macd,rsi14,boll20"}) = EMA21 207.73, EMA60 204.55, RSI14 64.42, Bollinger upper 224.05, 日线判定上升·高位；周线 EMA21<EMA60 盘整
- NVDA最新季度利润表: query_longbridge_by_route(fundamental/financials/income,{"symbol":"NVDA.US","period":"quarter","force_refresh":true}) = FY2027 Q1报告日2026-04-26，收入816.15亿美元，经营利润535.36亿美元，净利润583.21亿美元，基本EPS2.39
- NVDA一致预期: query_longbridge_by_route(fundamental/consensus,{"symbol":"NVDA.US","force_refresh":true}) = FY2027 Q1收入实际816.15亿美元/估计791.16亿美元、GAAP EPS实际2.39/估计1.7413，均Beat；FY2027 Q2/Q3/Q4收入预期918.46/1031.31/1161.05亿美元，EPS预期2.0573/2.3397/2.6555
- 美国宏观指标: query_indicators({"category":"macro","country":"us","time_range":"7d","limit":20}) = Fed资产负债表6748567（数据日2026-08-05）；美国CPI同比3.5（数据日2026-06-01，已标过时），其余相关指标同样多为旧数据
- 美国未来CPI日历: query_calendar_events({"country":"US","days":30,"importance":"high,medium","limit":30}) = 2026-08-12美国7月CPI同比预期3.4%、核心CPI同比预期2.5%，前值分别3.5%、2.6%
- 美国国债标售日历: query_calendar_events({"country":"US","days":30,"importance":"high,medium","limit":30}) = 2026-08-11至13美国财政部计划标售逾千亿美元国债
- NVIDIA公司新闻: query_longbridge_by_route(news/company,{"symbol":"NVDA.US","force_refresh":true}) = 2026-08-08报道拟最多30亿美元投资Lancium；SpaceX据报道明年AI平台 exclusively使用NVIDIA硬件；Firebird亚美尼亚AI工厂计划2027部署逾70000 GPUs（新闻描述）

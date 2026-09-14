# Ackman 交叉审查 — 独立数据核验记录（2026-09-14）

## 用工具独立核验的数据点

- 密歇根消费者信心指数初值 9/11 14:00: query_calendar_events(US, medium, actual: 47.8, forecast: 51.0, previous: 51.7) ✅
- 密歇根消费者预期指数初值: query_calendar_events(US, medium, actual: 45.8, previous: 51.5) ✅
- 密歇根消费者现况指数初值: query_calendar_events(US, medium, actual: 50.9, previous: 51.9) ✅
- 密歇根1年通胀预期初值: query_calendar_events(US, low, actual: 4.6, forecast: 4.2, previous: 4.0) — ⚠️ 文档仅笼统提及"通胀预期仍在高位"，未引用具体数字4.6%
- 密歇根5年通胀预期初值: query_calendar_events(US, low, actual: 3.4, forecast: 3.3, previous: 3.3)
- 8月核心CPI环比: query_calendar_events(US, medium, actual: 0.3, forecast: 0.2, previous: 0.2) ✅
- 8月CPI环比: query_calendar_events(US, medium, actual: 0.4, forecast: 0.4, previous: 0.1) ✅
- 8月PPI同比: query_calendar_events(US, high, actual: 5.4, forecast: 5.3, previous: 4.7) ✅
- 核心PPI环比: query_calendar_events(US, high, actual: 0.2, forecast: 0.3, previous: 0.2) ✅
- 10Y国债拍卖竞争性投标: query_calendar_events(US, high, actual: 39000040000, previous: 52623557100) ✅
- 10Y拍卖高配额百分比: query_calendar_events(US, medium, actual: 89.25, previous: 65.27)
- 30Y mortgage rate: query_calendar_events(US, medium, actual: 6.85, previous: 6.79) ✅
- 中国8月CPI同比: query_calendar_events(CN, high, actual: 0.8, forecast: 0.8, previous: 0.5) ✅
- 中国8月外储: query_calendar_events(CN, high, actual: 3.438, forecast: 3.425, previous: 3.419) ✅
- 中国贸易顺差: query_calendar_events(CN, high, actual: 119.09, forecast: 119.05, previous: 112.5) ✅
- FOMC利率: query_calendar_events(US, medium) — 下限 previous 3.5/forecast 3.5, 上限 previous 3.75/forecast 3.75 — ⚠️ 与文档声称的5.25-5.50%存在显著口径差异
- 英国8月调和CPI前值: query_calendar_events(GB, low, previous: 3.1) — ⚠️ 文档称前值2.9%，可能为标准CPI vs HICP口径差异
- US宏观指标快照: query_indicators(country=us, category=macro) — consumer_confidence_us=55.2（Conference Board, 75天前）, CPI_yoy=3.4, fed_balance_sheet=67406亿（5天前）

# Reference — buffett 分析溯源

## 财务数据
- FY2025 Revenue $60.53B / Net Income $13.71B / EPS $9.25: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US)
- FY2024 Revenue $54.70B / Net Income $15.62B / EPS $10.56: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US)
- FY2023 Revenue $34.72B / Net Income $8.42B / EPS $5.77: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US)
- FY2022 Revenue $19.29B / Net Income $4.66B / EPS $3.24: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US)

## 季度一致预期（已发布）
- Q1 2026: Revenue $15.37B (Miss, est $15.83B) / Net Income $1.82B (Miss, est $3.20B) / EPS $1.23 (Miss, est $2.13): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q4 2025: Revenue $17.71B (Miss) / Net Income $3.51B (Miss, est $4.07B): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q3 2025: Revenue $15.21B (Miss) / Net Income $4.12B (Beat, est $3.23B): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q2 2025: Revenue $14.50B (Beat) / Net Income $4.29B (Beat, est $2.88B): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q1 2025: Revenue $13.17B (Miss) / Net Income $2.03B (Miss, est $3.72B): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)

## 估值
- 当前 PE: 9.81x (Low 9.81, High 12.99, Median 10.59): query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)

## 资产负债表
- FY2025: Total Assets $90.06B, Total Liabilities $30.97B, Shareholders' Equity $59.09B, Debt Ratio 34.4%: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US)
- FY2024: Total Assets $69.19B, Total Liabilities $26.27B, Shareholders' Equity $42.92B: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US)

## 分析师评级
- 2026-07-29: Strong Buy 18 / Buy 4 / Hold 14 / Sell 1 (首次出现 Sell): query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 2025-05-30 峰值: Strong Buy 24 / Buy 5 / Hold 12 / Sell 1: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 2024-03 峰值: Strong Buy 34 / Buy 7 / Hold 2 / Sell 0: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 当前平均目标价 $116.27 (最低 $80.09, 最高 $170.33, 2026-07-27): query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)

## 近期重大新闻
- EU Commission charges Temu for obstructing investigation under Foreign Subsidies Regulation (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US)
- EU searches Temu European HQ in Ireland, accuses company of failing to cooperate (2026-08-01): query_longbridge_by_route(news/company, symbol=PDD.US)
- Temu shuts down multiple domestic warehouses in Guangdong, builds warehouses in Germany/Poland — strategic shift from cross-border direct mail to localized logistics (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US)
- PDD Xiong'an company employees exceed 3,000, plans to recruit 5,000 in coming year (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US)
- GOME Retail offshore debt restructuring, negotiations with Pinduoduo remain unresolved (2026-07-30): query_longbridge_by_route(news/company, symbol=PDD.US)

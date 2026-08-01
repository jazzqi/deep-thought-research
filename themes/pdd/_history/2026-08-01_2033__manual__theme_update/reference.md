# 数据溯源记录 — pdd

## 宏观指标
- China GDP Q1-Q2 2026: 4.7%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = gdp_quarterly=4.7
- China Manufacturing PMI July 2026: 49.2 (收缩): query_indicators(category=macro, country=china, limit=20, time_range=7d) = manufacturing_pmi=49.2
- China Non-Manufacturing PMI July 2026: 49.0 (收缩): query_indicators(category=macro, country=china, limit=20, time_range=7d) = non_manufacturing_pmi=49.0
- China Retail Sales YoY June 2026: +1.0%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = retail_sales_yoy=1.0
- China Consumer Confidence June 2026: 89.4: query_indicators(category=macro, country=china, limit=20, time_range=7d) = consumer_confidence=89.4
- China FAI YoY June 2026: -15.6%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = fai_yoy=-15.6
- China New Loans YoY June 2026: -25.2%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = new_loan_yoy=-25.21
- China 10Y Bond Yield July 31 2026: 1.7141%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = bond_10y_yield=1.7141
- China 2Y Bond Yield July 31 2026: 1.2606%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = bond_2y_yield=1.2606
- China LPR 1Y: 3.0%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = lpr_1y=3.0
- China Shibor 3M July 31 2026: 1.43%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = shibor_3m=1.43
- China PPI YoY 2025-08: -3.6%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = ppi_yoy=-3.6

## 估值数据
- PE TTM current=9.81, high=12.99, low=9.81, median=10.59: query_longbridge_by_route(fundamental/valuation/pe, {"symbol": "PDD.US"})

## 财务数据 - 损益表 (年度)
- FY2025 Revenue $60.53B, Op Income $13.05B, Net Income $13.71B, EPS $9.25: query_longbridge_by_route(fundamental/financials/income, {"symbol": "PDD.US", "count": 6})
- FY2024 Revenue $54.70B, Op Income $15.06B, Net Income $15.62B, EPS $10.56: query_longbridge_by_route(fundamental/financials/income, {"symbol": "PDD.US", "count": 6})
- FY2023 Revenue $34.72B, Op Income $8.23B, Net Income $8.42B, EPS $5.77: query_longbridge_by_route(fundamental/financials/income, {"symbol": "PDD.US", "count": 6})
- FY2022 Revenue $19.29B, Op Income $4.49B, Net Income $4.66B, EPS $3.24: query_longbridge_by_route(fundamental/financials/income, {"symbol": "PDD.US", "count": 6})

## 财务数据 - 季度一致预期
- Q1 2026 Actual: Revenue $15.37B vs Est $15.83B (Miss), Net Income $1.82B vs Est $3.20B (Miss 43%), EPS $1.23 vs Est $2.13 (Miss 42%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q2 2026 Estimate: Revenue $16.86B, Net Income $3.66B, EPS $2.53: query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q3 2026 Estimate: Revenue $17.88B, Net Income $3.68B, EPS $2.55: query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q4 2026 Estimate: Revenue $20.13B, Net Income $4.04B, EPS $2.95: query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q4 2025 Actual: Revenue $17.71B vs Est $17.84B (Miss), Net Income $3.51B vs Est $4.07B (Miss 14%), EPS $2.36 vs Est $2.79 (Miss 15%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q3 2025 Actual: Revenue $15.21B vs Est $15.27B (Miss), EBIT $3.80B vs Est $3.42B (Beat), Net Income $4.12B vs Est $3.23B (Beat 28%), EPS $2.77 vs Est $2.09 (Beat 32%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q2 2025 Actual: Revenue $14.50B vs Est $14.39B (Beat), EBIT $3.87B vs Est $3.07B (Beat 26%), Net Income $4.29B (Beat), EPS $2.89 vs Est $1.72 (Beat 68%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q1 2025 Actual: Revenue $13.17B vs Est $14.19B (Miss 7%), Net Income $2.03B, EPS $1.37 vs Est $2.40 (Miss 43%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})

## 分析师评级
- Latest (07/29/2026): Strong Buy 18, Buy 4, Hold 14, Sell 0: query_longbridge_by_route(analyst/rating_detail, {"symbol": "PDD.US"})
- Average Target Price: $116.27 (range $80-$170): query_longbridge_by_route(analyst/rating_detail, {"symbol": "PDD.US"})
- Trend: Strong Buy declining from peak of 34 (2024) to 18, Hold rising from 0 to 14: query_longbridge_by_route(analyst/rating_detail, {"symbol": "PDD.US"})

## EPS 预测
- FY2026 Normalized EPS estimate: $11.71 median (range $8.22-$12.88): query_longbridge_by_route(analyst/forecast_eps, {"symbol": "PDD.US"})

## 公司新闻
- EU Commission charges Temu for obstructing investigation (2026-08-01): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "count": 15}) - https://longportapp.cn/news/294577628
- EU Commission accuses Temu of obstructing investigation during search at European HQ in Ireland (2026-08-01): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "count": 15}) - https://longportapp.cn/news/294541903
- Temu shuts down domestic warehouses in Guangdong, builds own warehouses in Germany, Poland (2026-07-31): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "count": 15}) - https://longportapp.cn/news/294452061
- PDD Xiong'an company employees exceed 3,000, plan to recruit 5,000 more (2026-07-31): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "count": 15}) - https://longportapp.cn/news/294451407
- GOME Retail debt restructuring involves PDD negotiations unresolved (2026-07-30): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "count": 15}) - https://longportapp.cn/news/294329012

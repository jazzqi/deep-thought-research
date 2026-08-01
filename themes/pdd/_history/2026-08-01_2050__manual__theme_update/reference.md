# Data Sources Reference

## 估值数据
- PE TTM current=9.81, high=12.99, low=9.81, median=10.59: query_longbridge_by_route(fundamental/valuation/pe, {"symbol": "PDD.US"})

## 财务数据 - 季度一致预期
- Q1 2026 Actual: Revenue $15.37B vs Est $15.83B (Miss), Net Income $1.82B vs Est $3.20B (Miss 43%), EPS $1.23 vs Est $2.13 (Miss 42%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q2 2026 Estimate: Revenue $16.86B, Net Income $3.66B, EPS $2.53: query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q3 2026 Estimate: Revenue $17.88B, Net Income $3.68B, EPS $2.55: query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q4 2026 Estimate: Revenue $20.13B, Net Income $4.04B, EPS $2.95: query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q4 2025 Actual: Revenue $17.71B vs Est $17.84B (Miss), Net Income $3.51B vs Est $4.07B (Miss 14%), EPS $2.36 vs Est $2.79 (Miss 15%)
- Q3 2025 Actual: Revenue $15.21B vs Est $15.27B (Miss), Net Income $4.12B vs Est $3.23B (Beat 28%), EPS $2.77 vs Est $2.09 (Beat 32%)
- Q2 2025 Actual: Revenue $14.50B vs Est $14.39B (Beat), Net Income $4.29B, EPS $2.89 vs Est $1.72 (Beat 69%)
- Q1 2025 Actual: Revenue $13.17B vs Est $14.19B (Miss), Net Income $2.03B, EPS $1.37 vs Est $2.40 (Miss 43%)

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

## 新闻事件
- EU Commission charges Temu for not cooperating in December raid (2026-07-31): query_longbridge_by_route(news/company, {"symbol": "PDD.US"})
- Temu Responds To European Commission Statement Of Grounds Under FSR (2026-08-01): query_longbridge_by_route(news/company, {"symbol": "PDD.US"})
- Temu has changed by shutting down a number of domestic warehouses (2026-07-31): query_longbridge_by_route(news/company, {"symbol": "PDD.US"})
- PDD Xiong'an company's employees exceed 3,000 (2026-07-31): query_longbridge_by_route(news/company, {"symbol": "PDD.US"})
- GOME Retail weighs holistic offshore debt restructuring, negotiations with PDD unresolved (2026-07-30): query_longbridge_by_route(news/company, {"symbol": "PDD.US"})


## 新增数据源（relay buffett 补充）
- PDD FY2020 Revenue $8.67B, Op Income -$1.37B, Net Income -$1.05B, EPS -$0.88: query_longbridge_by_route(fundamental/financials/income, {"symbol": "PDD.US", "count": 6})
- PDD FY2021 Revenue $14.53B, Op Income $1.07B, Net Income $1.20B, EPS $0.84: query_longbridge_by_route(fundamental/financials/income, {"symbol": "PDD.US", "count": 6})
- PDD FY2022 Revenue $19.29B, Op Income $4.49B, Net Income $4.66B, EPS $3.24: query_longbridge_by_route(fundamental/financials/income, {"symbol": "PDD.US", "count": 6})
- PDD FY2023 Revenue $34.72B, Op Income $8.23B, Net Income $8.42B, EPS $5.77: query_longbridge_by_route(fundamental/financials/income, {"symbol": "PDD.US", "count": 6})
- PDD FY2024 Revenue $54.70B, Op Income $15.06B, Net Income $15.62B, EPS $10.56: query_longbridge_by_route(fundamental/financials/income, {"symbol": "PDD.US", "count": 6})
- PDD FY2025 Revenue $60.53B, Op Income $13.05B, Net Income $13.71B, EPS $9.25: query_longbridge_by_route(fundamental/financials/income, {"symbol": "PDD.US", "count": 6})
- Q1 2025 Consensus: Revenue $14.19B Est vs $13.17B Actual (Miss -7.2%), EPS $2.40 Est vs $1.37 Actual (Miss -43%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q2 2025 Consensus: Revenue $14.39B Est vs $14.50B Actual (Beat +0.8%), EPS $1.72 Est vs $2.89 Actual (Beat +69%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q3 2025 Consensus: Revenue $15.27B Est vs $15.21B Actual (Miss -0.4%), EPS $2.09 Est vs $2.77 Actual (Beat +32%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q4 2025 Consensus: Revenue $17.84B Est vs $17.71B Actual (Miss -0.7%), EPS $2.79 Est vs $2.36 Actual (Miss -15%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q1 2026 Consensus: Revenue $15.83B Est vs $15.37B Actual (Miss -2.9%), Net Income $3.20B Est vs $1.82B Actual (Miss -43%), EPS $2.13 Est vs $1.23 Actual (Miss -42%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q2 2026E: Revenue $16.86B, Net Income $3.66B, EPS $2.53: query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q3 2026E: Revenue $17.88B, Net Income $3.68B, EPS $2.55: query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q4 2026E: Revenue $20.13B, Net Income $4.04B, EPS $2.95: query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- China GDP Q1-Q2 2026: 4.7%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = gdp_quarterly=4.7
- China Manufacturing PMI July 2026: 49.2: query_indicators(category=macro, country=china, limit=20, time_range=7d) = manufacturing_pmi=49.2
- China Non-Manufacturing PMI July 2026: 49.0: query_indicators(category=macro, country=china, limit=20, time_range=7d) = non_manufacturing_pmi=49.0
- China Retail Sales YoY June 2026: +1.0%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = retail_sales_yoy=1.0
- China Consumer Confidence June 2026: 89.4: query_indicators(category=macro, country=china, limit=20, time_range=7d) = consumer_confidence=89.4
- China FAI YoY June 2026: -15.6%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = fai_yoy=-15.6
- China New Loans YoY June 2026: -25.2%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = new_loan_yoy=-25.21
- China 10Y Bond Yield July 31 2026: 1.7141%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = bond_10y_yield=1.7141
- China 2Y Bond Yield July 31 2026: 1.2606%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = bond_2y_yield=1.2606
- China Yield Spread 10Y-2Y July 31 2026: 45.35bp: query_indicators(category=macro, country=china, limit=20, time_range=7d) = yield_spread_10y_2y=0.4535
- China LPR 1Y: 3.0%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = lpr_1y=3.0
- China Shibor 3M July 31 2026: 1.43%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = shibor_3m=1.43
- China PPI YoY 2025-08: -3.6%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = ppi_yoy=-3.6
- EU Commission charges Temu for not cooperating in December raid (2026-07-31): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "limit": 15})
- Temu Responds To European Commission Statement Of Grounds Under FSR (2026-08-01): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "limit": 15})
- Temu has changed by shutting down a number of domestic warehouses (2026-07-31): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "limit": 15})
- PDD Xiong'an company's employees exceed 3,000 (2026-07-31): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "limit": 15})
- GOME Retail weighs holistic offshore debt restructuring, negotiations with PDD unresolved (2026-07-30): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "limit": 15})


## buffett 审查补充数据源

- PDD FY2025 Shareholders Equity $59.09B: query_longbridge_by_route(fundamental/financials/balance, {"symbol": "PDD.US", "count": 3}) = shareholders_equity=59088787307
- PDD FY2024 Shareholders Equity $42.92B: query_longbridge_by_route(fundamental/financials/balance, {"symbol": "PDD.US", "count": 3}) = shareholders_equity=42923722000
- PDD FY2023 Shareholders Equity $26.38B: query_longbridge_by_route(fundamental/financials/balance, {"symbol": "PDD.US", "count": 3}) = shareholders_equity=26380231480
- PDD Q1 2025 EBIT Actual $2.51B vs Est $3.59B (Miss -30%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- PDD Q2 2025 EBIT Actual $3.87B vs Est $3.07B (Beat +26%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- PDD Q1 2026 EBIT Actual $3.05B vs Est $3.22B (Miss -5%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- PDD Q1 2026 Normalized Net Income $2.04B vs Est $3.53B (Miss -42%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- PDD Q2 2025 Normalized Net Income $4.56B vs Est $2.88B (Beat +59%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- PDD Q3 2025 Normalized Net Income $4.41B vs Est $3.47B (Beat +27%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- PDD Q4 2025 Normalized Net Income $3.76B vs Est $4.51B (Miss -17%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- China CPI YoY: stale (data: 2025-08-09, ⚠️ 357 days old): query_indicators(category=macro, country=china, limit=20, time_range=7d) = cpi_yoy=0.0
- PDD news - "free shipping to villages" agricultural initiative (2026-07-30): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "limit": 20})
- PDD news - "Capital Pivots to Defense and AI" mentioning legacy consumer platforms (2026-07-31): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "limit": 20})

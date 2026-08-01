# PDD Holdings - 数据溯源 (Roundtable 2026-08-01)

## 宏观指标
- China GDP Q1-Q2 2026: 4.7%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = gdp_quarterly=4.7
- China Manufacturing PMI July 2026: 49.2 (收缩): query_indicators(category=macro, country=china, limit=20, time_range=7d) = manufacturing_pmi=49.2
- China Non-Manufacturing PMI July 2026: 49.0 (收缩): query_indicators(category=macro, country=china, limit=20, time_range=7d) = non_manufacturing_pmi=49.0
- China Retail Sales YoY June 2026: +1.0%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = retail_sales_yoy=1.0
- China Consumer Confidence June 2026: 89.4: query_indicators(category=macro, country=china, limit=20, time_range=7d) = consumer_confidence=89.4
- China FAI YoY June 2026: -15.6%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = fai_yoy=-15.6
- China New Loans YoY June 2026: -25.2%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = new_loan_yoy=-25.21
- China 10Y Bond Yield July 31 2026: 1.7141%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = bond_10y_yield=1.7141
- China LPR 1Y: 3.0%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = lpr_1y=3.0
- China Shibor 3M July 31 2026: 1.43%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = shibor_3m=1.43
- China PPI YoY 2025-08: -3.6%: query_indicators(category=macro, country=china, limit=20, time_range=7d) = ppi_yoy=-3.6

## 估值数据
- PE TTM current=9.81, high=12.99, low=9.81, median=10.59: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)

## 财务数据 - 损益表
- FY2025 Revenue $60.53B, Op Income $13.05B, Net Income $13.71B, EPS $9.25: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) historical actuals
- FY2024 Revenue $54.70B, Op Income $15.06B, Net Income $15.62B, EPS $10.56: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) historical actuals
- Q1 2026 Actual: Revenue $15.37B vs Est $15.83B (Miss), Net Income $1.82B vs Est $3.20B (Miss 43%), EPS $1.23 vs Est $2.13 (Miss): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q2 2026E: Revenue $16.86B, Net Income $3.66B, EPS $2.53: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q3 2026E: Revenue $17.91B, Net Income $3.69B, EPS $2.54: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q4 2026E: Revenue $20.13B, Net Income $4.04B, EPS $2.95: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)

## 分析师评级
- 2026-07-29 Rating Distribution: SB18/B4/H14/S0/U1, Total 37: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 2026-07-27 Target Price: avg $116.27, max $170.33, min $80.09: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- Analyst coverage trend: Strong Buy declining from 34 (2024 peak) to 18 (current); Hold rising from 0 to 14: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)

## 公司新闻
- EU Commission formally accused Temu of obstructing investigation during December 2025 raid (2026-08-01): query_longbridge_by_route(news/company, symbol=PDD.US)
- Temu shuts domestic warehouses (Guangdong etc.), builds European own warehouses in Germany/Poland - strategic shift from full custody to localized logistics (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US)
- PDD Xiong'an company employees exceed 3,000, plan to recruit 5,000 more (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US)
- GOME Retail debt restructuring involving PDD/Pinduoduo - negotiations unresolved (2026-07-30): query_longbridge_by_route(news/company, symbol=PDD.US)

## 数据溯源 — buffett relay (2026-08-01)

### 宏观指标
- GDP 4.7% (2026 Q1-Q2): query_indicators(category=macro, country=china, time_range=24h, limit=20) = gdp_quarterly=4.7
- Manufacturing PMI 49.2 (2026年7月): query_indicators(category=macro, country=china, time_range=24h, limit=20) = manufacturing_pmi=49.2
- Non-Manufacturing PMI 49.0 (2026年7月): query_indicators(category=macro, country=china, time_range=24h, limit=20) = non_manufacturing_pmi=49.0
- Retail Sales YoY +1.0% (2026年6月): query_indicators(category=macro, country=china, time_range=24h, limit=20) = retail_sales_yoy=1.0
- Consumer Confidence 89.4 (2026年6月): query_indicators(category=macro, country=china, time_range=24h, limit=20) = consumer_confidence=89.4
- New Loans YoY -25.21% (2026年6月): query_indicators(category=macro, country=china, time_range=24h, limit=20) = new_loan_yoy=-25.21186441
- FAI YoY -15.6% (2026年6月): query_indicators(category=macro, country=china, time_range=24h, limit=20) = fai_yoy=-15.6
- CPI YoY 0.0% (2025-08, ⚠️ stale): query_indicators(category=macro, country=china, time_range=24h, limit=20) = cpi_yoy=0.0
- PPI YoY -3.6% (2025-08, ⚠️ stale): query_indicators(category=macro, country=china, time_range=24h, limit=20) = ppi_yoy=-3.6

### 估值数据
- PE TTM current 9.81, high 12.99, low 9.81, median 10.59: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)
- PE 历史走势 2021-2026: query_longbridge_by_route(fundamental/valuation/history, symbol=PDD.US)

### 财务数据 — 损益表
- FY2025 Revenue $60.53B, Op Income $13.05B, Net Income $13.71B, EPS $9.25: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=6)
- FY2024 Revenue $54.70B, Op Income $15.06B, Net Income $15.62B, EPS $10.56: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=6)
- FY2023 Revenue $34.72B, Op Income $8.23B, Net Income $8.42B, EPS $5.77: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=6)
- FY2022 Revenue $19.29B, Op Income $4.49B, Net Income $4.66B, EPS $3.24: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=6)

### 财务数据 — 资产负债表
- FY2025 Total Assets $90.06B, Total Liabilities $30.97B, Shareholders' Equity $59.09B: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=4)
- FY2024 Total Assets $69.19B, Total Liabilities $26.27B, Shareholders' Equity $42.92B: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=4)
- FY2023 Total Assets $49.04B, Total Liabilities $22.66B, Shareholders' Equity $26.38B: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=4)

### 一致预期
- Q1 2026 Actual: Revenue $15.37B vs Est $15.83B(Miss), Net Income $1.82B vs Est $3.20B(Miss 43%), EPS $1.23 vs Est $2.13(Miss): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q2 2026E: Revenue $16.86B, EBIT $3.94B, Net Income $3.66B, EPS $2.53: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q3 2026E: Revenue $17.88B, EBIT $4.08B, Net Income $3.68B, EPS $2.55: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q4 2026E: Revenue $20.13B, EBIT $4.79B, Net Income $4.04B, EPS $2.95: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)

### 分析师评级
- 2026-07-29 评级分布: SB18/B4/H14/S0/U1, Total 37: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 2026-07-27 目标价: avg $116.27, max $170.33, min $80.09: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)

### 公司新闻
- EU FSR Statement of Grounds - Temu accused of obstructing Dec raid (2026-08-01): query_longbridge_by_route(news/company, symbol=PDD.US, count=20)
- Temu shuts domestic warehouses, builds European own warehouses (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US, count=20)
- PDD Xiong'an company employees exceed 3,000 (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US, count=20)
- GOME Retail debt restructuring involving PDD/Pinduoduo (2026-07-30): query_longbridge_by_route(news/company, symbol=PDD.US, count=20)

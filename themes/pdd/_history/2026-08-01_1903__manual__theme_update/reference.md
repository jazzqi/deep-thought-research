# 数据来源追溯

## 宏观指标
- GDP 4.7% (2026 Q1-Q2): query_indicators(category=macro, country=china) = gdp_quarterly=4.7
- Manufacturing PMI 49.2 (2026年7月): query_indicators(category=macro, country=china) = manufacturing_pmi=49.2
- Non-Manufacturing PMI 49.0 (2026年7月): query_indicators(category=macro, country=china) = non_manufacturing_pmi=49.0
- Retail Sales YoY +1.0% (2026年6月): query_indicators(category=macro, country=china) = retail_sales_yoy=1.0
- Consumer Confidence 89.4 (2026年6月): query_indicators(category=macro, country=china) = consumer_confidence=89.4
- New Loans YoY -25.2% (2026年6月): query_indicators(category=macro, country=china) = new_loan_yoy=-25.21186441
- FAI YoY -15.6% (2026年6月): query_indicators(category=macro, country=china) = fai_yoy=-15.6
- 10Y Bond Yield 1.7141 (2026-07-31): query_indicators(category=macro, country=china) = bond_10y_yield=1.7141
- LPR 1Y 3.0%: query_indicators(category=macro, country=china) = lpr_1y=3.0
- Shibor 3M 1.43% (2026-07-31): query_indicators(category=macro, country=china) = shibor_3m=1.43

## 估值数据
- PE TTM current 9.81, high 12.99, median 10.59: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)

## 一致预期
- Q1 2026 Actual: Revenue $15.37B vs Est $15.83B(Miss), Net Income $1.82B vs Est $3.20B(Miss 43%), EPS $1.23 vs Est $2.13(Miss): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q2 2026E: Revenue $16.86B, Net Income $3.66B, EPS $2.53: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q3 2026E: Revenue $17.91B, Net Income $3.69B, EPS $2.54: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q4 2026E: Revenue $20.13B, Net Income $4.04B, EPS $2.95: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q4 2025 Actual: Revenue $17.71B vs Est $17.84B(Miss), Net Income $3.51B vs Est $4.07B(Miss): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)

## 分析师评级
- 2026-07-29 评级分布: SB18/B4/H14/S0/U1, Total 37: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 2026-07-27 目标价: avg $116.27, max $170.33, min $80.09: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)

## 公司新闻
- EU FSR Statement of Grounds - Temu accused of obstructing Dec raid (2026-08-01): query_longbridge_by_route(news/company, symbol=PDD.US)
- Temu shuts domestic warehouses, builds European own warehouses (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US)
- PDD Xiong'an company employees exceed 3,000 (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US)
- GOME Retail debt restructuring involving PDD/Pinduoduo (2026-07-30): query_longbridge_by_route(news/company, symbol=PDD.US)

# Reference — PDD Holdings Analysis

## 数据溯源

### 估值数据
- PE TTM current: 9.81, high: 12.99, low: 9.81, median: 10.59: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)
- PE 历史走势 2021-2026: 从 2022 年高点 63x 一路压缩至当前 ~9x — query_longbridge_by_route(fundamental/valuation/history, symbol=PDD.US)

### 财务数据 — 损益表
- FY2025 Revenue $60.53B, Op Income $13.05B, Net Income $13.71B, EPS $9.25: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8)
- FY2024 Revenue $54.70B, Op Income $15.06B, Net Income $15.62B, EPS $10.56: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8)
- FY2023 Revenue $34.72B, Op Income $8.23B, Net Income $8.42B, EPS $5.77: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8)
- FY2022 Revenue $19.29B, Op Income $4.49B, Net Income $4.66B, EPS $3.24: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8)

### 财务数据 — 资产负债表
- FY2025 Total Assets $90.06B, Total Liabilities $30.97B, Shareholders' Equity $59.09B: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=4)
- FY2024 Total Assets $69.19B, Total Liabilities $26.27B, Shareholders' Equity $42.92B: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=4)
- FY2023 Total Assets $49.04B, Total Liabilities $22.66B, Shareholders' Equity $26.38B: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=4)

### 财务数据 — 现金流
- FY2025 OCF $14.99B, FCF $12.00B: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US, count=4)
- FY2024 OCF $16.94B, FCF $14.33B: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US, count=4)
- FY2023 OCF $13.20B, FCF $11.63B: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US, count=4)

### 一致预期
- Q1 2026: Revenue $15.37B (actual) vs $15.83B (estimate) = Miss; Net Income $1.82B vs $3.20B = Miss 43%; EPS $1.23 vs $2.13 = Miss: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q2 2026E: Revenue $16.86B, EBIT $3.94B, Net Income $3.66B, EPS $2.53: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q3 2026E: Revenue $17.91B, EBIT $4.09B, Net Income $3.69B, EPS $2.54: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q4 2026E: Revenue $20.13B, EBIT $4.79B, Net Income $4.04B, EPS $2.95: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)

### 分析师评级
- 2026-07-29 评级分布: SB18/B4/H14/S0/U1, Total 37: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 2026-07-27 目标价: avg $116.27, max $170.33, min $80.09: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)

### 公司新闻
- EU FSR Statement of Grounds - Temu accused of obstructing Dec raid (2026-08-01): query_longbridge_by_route(news/company, symbol=PDD.US, count=20)
- Temu shuts domestic warehouses, builds European own warehouses (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US, count=20)
- PDD Xiong'an company employees exceed 3,000 (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US, count=20)
- GOME Retail debt restructuring involving PDD/Pinduoduo (2026-07-30): query_longbridge_by_route(news/company, symbol=PDD.US, count=20)

### 宏观指标（中国）
- GDP 4.7% (2026 Q1-Q2): query_indicators(category=macro, country=china, time_range=24h)
- Manufacturing PMI 49.2 (2026年7月): query_indicators(category=macro, country=china, time_range=24h)
- Non-Manufacturing PMI 49.0 (2026年7月): query_indicators(category=macro, country=china, time_range=24h)
- Retail Sales YoY +1.0% (2026年6月): query_indicators(category=macro, country=china, time_range=24h)
- Consumer Confidence 89.4 (2026年6月): query_indicators(category=macro, country=china, time_range=24h)
- New Loan YoY -25.2% (2026年6月): query_indicators(category=macro, country=china, time_range=24h)
- LPR 1Y 3.0% (2026-08-01): query_indicators(category=macro, country=china, time_range=24h)
- 10Y Bond Yield 1.71% (2026-07-31): query_indicators(category=macro, country=china, time_range=24h)
- FAI YoY -15.6% (2026年6月): query_indicators(category=macro, country=china, time_range=24h)
- House Price Index 0.5 (2026-08-01): query_indicators(category=macro, country=china, time_range=24h)

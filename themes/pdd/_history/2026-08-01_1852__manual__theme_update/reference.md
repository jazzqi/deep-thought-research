# PDD Holdings 数据来源汇总

## 估值数据
- PE TTM current: 9.81, high: 12.99, low: 9.81, median: 10.59: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)

## 财务数据
- FY2025 Revenue $60.53B, Op Income $13.05B, Net Income $13.71B, EPS $9.25: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=4)
- FY2024 Revenue $54.70B, Op Income $15.06B, Net Income $15.62B, EPS $10.56: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=4)
- FY2023 Revenue $34.72B, Op Income $8.23B, Net Income $8.42B, EPS $5.77: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=4)

## 一致预期
- Q1 2026: Revenue $15.37B(actual) vs $15.83B(estimate) = Miss; Net Income $1.82B vs $3.20B = Miss 43%; EPS $1.23 vs $2.13 = Miss: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q2 2026E: Revenue $16.86B, Net Income $3.66B, EPS $2.53: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q3 2026E: Revenue $17.91B, Net Income $3.69B, EPS $2.54: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q4 2026E: Revenue $20.13B, Net Income $4.04B, EPS $2.95: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- FY2025 Q4: Revenue $17.71B vs $17.84B = Miss; Net Income $3.51B vs $4.07B = Miss: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- FY2025 Q3: Revenue $15.21B vs $15.27B = Miss; Net Income $4.12B vs $3.23B = Beat: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- FY2025 Q2: Revenue $14.50B vs $14.39B = Beat; Net Income $4.29B = Beat: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)

## 分析师评级
- 2026-07-29 评级分布: SB18/B4/H14/S0/U1, Total 37: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 2026-07-27 目标价: avg $116.27, max $170.33, min $80.09: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)

## 公司新闻
- EU FSR Statement of Grounds - Temu accused of obstructing Dec raid (2026-08-01): query_longbridge_by_route(news/company, symbol=PDD.US)
- Temu shuts domestic warehouses, builds European own warehouses (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US)
- PDD Xiong'an company employees exceed 3,000 (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US)
- GOME Retail debt restructuring involving PDD/Pinduoduo (2026-07-30): query_longbridge_by_route(news/company, symbol=PDD.US)

## 宏观指标
- GDP 4.7% (2026 Q1-Q2): query_indicators(category=macro, country=china)
- Manufacturing PMI 49.2 (2026年7月): query_indicators(category=macro, country=china)
- Non-Manufacturing PMI 49.0 (2026年7月): query_indicators(category=macro, country=china)
- Retail Sales YoY +1.0% (2026年6月): query_indicators(category=macro, country=china)
- Consumer Confidence 89.4 (2026年6月): query_indicators(category=macro, country=china)
- LPR 1Y 3.0% (2026-08-01): query_indicators(category=macro, country=china)
- Bond 10Y yield 1.7141% (2026-07-31): query_indicators(category=macro, country=china)
- New Loans YoY -25.2% (2026年6月): query_indicators(category=macro, country=china)
- PPI YoY -3.6% (2025-08-09): query_indicators(category=macro, country=china)
- Fixed Asset Investment YoY -15.6% (2026年6月): query_indicators(category=macro, country=china)

- FY2025 Revenue $60.53B / Operating Income $13.05B / Net Income $13.71B / EPS $9.25: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8)
- FY2024 Revenue $54.70B / Operating Income $15.06B / Net Income $15.62B / EPS $10.56: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8)
- FY2023 Revenue $34.72B / Operating Income $8.23B / Net Income $8.42B / EPS $5.77: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8)
- FY2025 Total Assets $90.06B / Total Liabilities $30.97B / Shareholders' Equity $59.09B: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=4)
- FY2025 Operating CF $14.99B / FCF $12.00B: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US, count=4)
- PE TTM current 9.81, high 12.99, low 9.81, median 10.59: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)
- Analyst consensus: Buy, target $170.20, distribution SB18/B4/H14/U1: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) + query_longbridge_by_route(market/institutional_rating, symbol=PDD.US)
- FY2026E Q2 Revenue $169B estimate, Net Income $36.6B, EPS $2.53: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- FY2026E Q3 Revenue $179B estimate, Net Income $36.9B, EPS $2.54: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- FY2026E Q4 Revenue $201B estimate, Net Income $40.4B, EPS $2.95: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q1 2026 Actual: Revenue $153.7B vs Est $158.3B (Miss), Net Income $18.2B vs Est $32.0B (Miss 43%), EPS $1.23 vs $2.13 (Miss): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- News: EU Commission accuses Temu of obstructing investigation (2026-08-01): query_longbridge_by_route(news/company, symbol=PDD.US)
- News: Temu shuts domestic warehouses, builds European own warehouses (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US)
- News: PDD Xiong'an company employees exceed 3,000 (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US)
- News: GOME Retail debt restructuring involving PDD (2026-07-30): query_longbridge_by_route(news/company, symbol=PDD.US)
- China Manufacturing PMI 49.2 (July 2026): query_indicators(category=macro, country=china)
- China Non-Manufacturing PMI 49.0 (July 2026): query_indicators(category=macro, country=china)
- China Retail Sales YoY +1.0% (June 2026): query_indicators(category=macro, country=china)
- China Consumer Confidence 89.4 (June 2026): query_indicators(category=macro, country=china)
- China GDP 4.7% (2026 Q1-Q2): query_indicators(category=macro, country=china)
- China New Loans YoY -25.2% (June 2026): query_indicators(category=macro, country=china)
- China LPR 1Y 3.0% (2026-08-01): query_indicators(category=macro, country=china)
- China Bond 10Y yield 1.7141% (2026-07-31): query_indicators(category=macro, country=china)

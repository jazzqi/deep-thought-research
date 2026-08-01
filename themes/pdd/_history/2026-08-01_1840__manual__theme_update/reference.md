# Data Sources Reference

## 财务数据
- FY2025 总收入 $605.3亿 / 经营利润 $130.5亿 / 净利润 $137.1亿 / EPS $9.25: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8)
- FY2024 总收入 $547.0亿 / 经营利润 $150.6亿 / 净利润 $156.2亿 / EPS $10.56: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8)
- FY2023 总收入 $347.2亿 / 经营利润 $82.3亿 / 净利润 $84.2亿 / EPS $5.77: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8)
- FY2022 总收入 $192.9亿 / 经营利润 $44.9亿 / 净利润 $46.6亿 / EPS $3.24: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8)
- FY2025 总资产 $900.6亿 / 总负债 $309.7亿 / 股东权益 $590.9亿: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=8)
- FY2024 总资产 $691.9亿 / 总负债 $262.7亿 / 股东权益 $429.2亿: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=8)
- FY2025 经营现金流 $149.9亿 / 自由现金流 $120.0亿: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US, count=8)
- FY2024 经营现金流 $169.4亿 / 自由现金流 $143.3亿: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US, count=8)

## 估值
- PE TTM current 9.81, high 12.99, low 9.81, median 10.59: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)

## 一致预期
- Q1 2026: Revenue $153.7亿(actual) vs $158.3亿(estimate) = Miss; Net Income $18.2亿 vs $32.0亿 = Miss 43%; EPS $1.23 vs $2.13 = Miss: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q4 2025: Revenue $177.1亿 vs $178.4亿 = Miss; Net Income $35.1亿 vs $40.7亿 = Miss; EPS $2.36 vs $2.79 = Miss: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q3 2025: Revenue $152.1亿 vs $152.7亿 = Miss; Net Income $41.2亿 vs $32.3亿 = Beat; EPS $2.77 vs $2.09 = Beat: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q2 2025: Revenue $145.0亿 vs $143.9亿 = Beat; Net Income $42.9亿 vs ~$28.8亿 = Beat; EPS $2.89 vs $1.72 = Beat: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q1 2025: Revenue $131.7亿 vs $141.9亿 = Miss; EPS $1.37 vs $2.40 = Miss: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- FY2026E 全年预期: Revenue ~$701亿, Net Income ~$155亿, EPS ~$10.8: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- FY2026E Q2: Revenue $169亿, Net Income $36.6亿, EPS $2.53: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- FY2026E Q3: Revenue $179亿, Net Income $36.9亿, EPS $2.54: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- FY2026E Q4: Revenue $201亿, Net Income $40.4亿, EPS $2.95: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)

## 分析师评级
- 2026-07-29 评级分布: SB18/B4/H14/S0/U1, Total 37: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 2026-07-27 目标价: avg $116.27, max $170.33, min $80.09: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)

## 机构评级
- 聚合评级: Buy, target $170.20: query_longbridge_by_route(market/institutional_rating, symbol=PDD.US)

## 公司基本信息
- 员工数 25,474: query_longbridge_by_route(company/profile, symbol=PDD.US)
- 公司描述: multinational commerce group, owns Pinduoduo and Temu: query_longbridge_by_route(company/profile, symbol=PDD.US)

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

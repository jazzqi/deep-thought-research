# Reference Data Sources

## Valuation Data
- PE TTM current=9.81, high=12.99, low=9.81, median=10.59: query_longbridge_by_route(fundamental/valuation/pe, {"symbol": "PDD.US"})
- PE History (weekly from 2021-08 to 2026-07): query_longbridge_by_route(fundamental/valuation/history, {"symbol": "PDD.US"}) — PE dropped from ~30x (2023Q4) to current 9.81x (2026-07-27), all-time low

## Financial Data — Annual Income
- FY2024: Revenue $54.70B, Operating Profit $15.06B, Net Profit $15.62B, EPS $10.56: query_longbridge_by_route(fundamental/financials/income, {"symbol": "PDD.US"})
- FY2025: Revenue $60.53B, Operating Profit $13.05B, Net Profit $13.71B, EPS $9.25: query_longbridge_by_route(fundamental/financials/income, {"symbol": "PDD.US"})
- Revenue growth deceleration: FY2023 +80% → FY2024 +57.5% → FY2025 +10.6%
- First annual profit decline since 2020: Net income dropped from $15.62B to $13.71B (-12.2%)

## Financial Data — Balance Sheet
- FY2025: Total Assets $90.06B, Total Liabilities $30.97B, Shareholders' Equity $59.09B: query_longbridge_by_route(fundamental/financials/balance, {"symbol": "PDD.US"})
- FY2024: Total Assets $69.19B, Total Liabilities $26.27B, Shareholders' Equity $42.92B
- Book value grew 37.7% YoY, D/E ratio = 0.52 (conservative leverage)

## Financial Data — Quarterly Consensus & Actuals
- Q1 2026 Actual: Revenue $15.37B vs Est $15.83B (Miss), Net Income $1.82B vs Est $3.20B (Miss 43%), EPS $1.23 vs Est $2.13 (Miss 42%): query_longbridge_by_route(fundamental/consensus, {"symbol": "PDD.US"})
- Q2 2026 Estimate: Revenue $16.86B, Net Income $3.66B, EPS $2.53
- Q3 2026 Estimate: Revenue $17.88B, Net Income $3.68B, EPS $2.55
- Q4 2026 Estimate: Revenue $20.13B, Net Income $4.04B, EPS $2.95
- Q4 2025 Actual: Revenue $17.71B vs Est $17.84B (Miss), Net Income $3.51B vs Est $4.07B (Miss 14%), EPS $2.36 vs Est $2.79 (Miss 15%)
- Q3 2025 Actual: Revenue $15.21B vs Est $15.27B (Miss), Net Income $4.12B vs Est $3.23B (Beat 28%)
- Q2 2025 Actual: Revenue $14.50B vs Est $14.39B (Beat), Net Income $4.29B, EPS $2.89 vs Est $1.72 (Beat 69%)
- Q1 2025 Actual: Revenue $13.17B vs Est $14.19B (Miss), Net Income $2.03B, EPS $1.37 vs Est $2.40 (Miss 43%)

## Analyst Ratings
- Aggregated Buy rating (SB18/B4/H14/U1), Target Price $170.20: query_longbridge_by_route(market/institutional_rating, {"symbol": "PDD.US"})
- Rating date: 2026-07-29

## Macro Indicators (China)
- China GDP Q1-Q2 2026: 4.7%: query_indicators(category=macro, country=china, limit=20, time_range=7d)
- China Manufacturing PMI July 2026: 49.2 (contraction zone): query_indicators(category=macro, country=china)
- China Non-Manufacturing PMI July 2026: 49.0 (contraction zone): query_indicators(category=macro, country=china)
- China Retail Sales YoY June 2026: +1.0%: query_indicators(category=macro, country=china)
- China Consumer Confidence June 2026: 89.4: query_indicators(category=macro, country=china)

## News Events
1. EU Commission charges Temu for obstructing December raid (FSR investigation escalation): query_longbridge_by_route(news/company, {"symbol": "PDD.US", "count": 20}) — published 2026-08-01
2. Temu shutting down domestic warehouses in Guangdong, building European warehouses in Germany/Poland: query_longbridge_by_route(news/company, {"symbol": "PDD.US", "count": 20}) — published 2026-07-31
3. PDD Xiong'an company exceeded 3,000 employees, plan to recruit 5,000 more: query_longbridge_by_route(news/company, {"symbol": "PDD.US", "count": 20}) — published 2026-07-31
4. GOME Retail debt restructuring, negotiations with PDD unresolved: query_longbridge_by_route(news/company, {"symbol": "PDD.US", "count": 20}) — published 2026-07-30
5. Temu responds to EU Commission statement of grounds under FSR: query_longbridge_by_route(news/company, {"symbol": "PDD.US", "count": 20}) — published 2026-08-01


---

## buffett 审查补充数据源

- FY2025 Income: Revenue $60,529,636,024 | Operating Income $13,049,656,238 | Net Income $13,714,095,324 | EPS $9.2509: query_longbridge_by_route(fundamental/financials/income, {"symbol":"PDD.US","period":"annual","count":5})
- FY2024 Income: Revenue $54,703,209,149 | Operating Income $15,059,763,546 | Net Income $15,616,975,367 | EPS $10.5563: query_longbridge_by_route(fundamental/financials/income, {"symbol":"PDD.US","period":"annual","count":5})
- FY2023 Income: Revenue $34,724,006,923 | Operating Income $8,230,749,320 | Net Income $8,416,931,113 | EPS $5.7696: query_longbridge_by_route(fundamental/financials/income, {"symbol":"PDD.US","period":"annual","count":5})
- FY2025 Balance: Total Assets $90,057,794,025 | Total Liabilities $30,969,006,718 | Shareholders' Equity $59,088,787,307: query_longbridge_by_route(fundamental/financials/balance, {"symbol":"PDD.US","period":"annual","count":5})
- FY2025 Cashflow: Operating CF $14,989,056,943 | Free CF $12,002,190,317: query_longbridge_by_route(fundamental/financials/cashflow, {"symbol":"PDD.US","period":"annual","count":5})
- FY2024 Cashflow: Operating CF $16,935,785,248 | Free CF $14,330,206,676: query_longbridge_by_route(fundamental/financials/cashflow, {"symbol":"PDD.US","period":"annual","count":5})
- FY2023 Cashflow: Operating CF $13,203,484,393 | Free CF $11,626,694,378: query_longbridge_by_route(fundamental/financials/cashflow, {"symbol":"PDD.US","period":"annual","count":5})
- PE: current=9.81, high=12.99, low=9.81, median=10.59: query_longbridge_by_route(fundamental/valuation/pe, {"symbol":"PDD.US"})
- Q1 2026 Actual: Revenue $15,367,667,269 | Est $15,826,531,035 (Miss -2.9%); Net Income $1,815,117,541 | Est $3,197,501,531 (Miss -43.2%); EPS(GAAP) $1.2268 | Est $2.1285 (Miss -42.4%); Normalized EPS $1.3758 | Est $2.3676 (Miss -41.9%): query_longbridge_by_route(fundamental/consensus, {"symbol":"PDD.US"})
- Q2 2026 Est: Revenue $16,863,654,752 | Net Income(GAAP) $3,655,626,660 | EPS(GAAP) $2.5306 | Normalized EPS $2.7107: query_longbridge_by_route(fundamental/consensus, {"symbol":"PDD.US"})
- Q3 2026 Est: Revenue $17,882,343,370 | Net Income(GAAP) $3,683,111,970 | EPS(GAAP) $2.5475 | Normalized EPS $2.7441: query_longbridge_by_route(fundamental/consensus, {"symbol":"PDD.US"})
- Q4 2026 Est: Revenue $20,128,612,149 | Net Income(GAAP) $4,038,382,624 | EPS(GAAP) $2.9471 | Normalized EPS $3.0119: query_longbridge_by_route(fundamental/consensus, {"symbol":"PDD.US"})
- Q4 2025 Actual: Revenue $17,711,863,065 | Est $17,841,448,698 (Miss -0.7%); Net Income(GAAP) $3,507,861,492 | Est $4,068,147,793 (Miss -13.8%); EPS(GAAP) $2.3599 | Est $2.7910 (Miss -15.5%): query_longbridge_by_route(fundamental/consensus, {"symbol":"PDD.US"})
- Q3 2025 Actual: Net Income(GAAP) $4,119,474,113 | Est $3,230,387,274 (Beat +27.5%): query_longbridge_by_route(fundamental/consensus, {"symbol":"PDD.US"})
- Q2 2025 Actual: Net Income(GAAP) $4,287,988,985 | Est (null); Normalized EPS $3.0772 | Est $2.0634 (Beat +49.1%): query_longbridge_by_route(fundamental/consensus, {"symbol":"PDD.US"})
- GDP Q1-Q2 2026: 4.7%: query_indicators(category=macro, country=china)
- Consumer Confidence Jun 2026: 89.4: query_indicators(category=macro, country=china)
- Retail Sales YoY Jun 2026: 1.0%: query_indicators(category=macro, country=china)
- Manufacturing PMI Jul 2026: 49.2: query_indicators(category=macro, country=china)
- Non-Manufacturing PMI Jul 2026: 49.0: query_indicators(category=macro, country=china)
- LPR 1Y: 3.0%: query_indicators(category=macro, country=china)
- Shibor 3M: 1.43%: query_indicators(category=macro, country=china)
- New Loan YoY Jun 2026: -25.2%: query_indicators(category=macro, country=china)

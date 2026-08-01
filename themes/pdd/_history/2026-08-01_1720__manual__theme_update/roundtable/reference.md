# Data Sources Reference — PDD Holdings Roundtable (2026-08-01)

## Financial Data Sources

### Income Statement (Annual)
- FY2025 Revenue: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $60,529,636,024
- FY2025 Net Income: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $13,714,095,324
- FY2025 EPS (Basic): query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $9.25
- FY2025 Operating Income: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $13,049,656,238
- FY2024 Revenue: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $54,703,209,149
- FY2024 Net Income: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $15,616,975,367
- FY2024 EPS (Basic): query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $10.56
- FY2023 Revenue: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $34,724,006,923
- FY2023 Net Income: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $8,416,931,113
- FY2023 EPS (Basic): query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $5.77

### Quarterly Consensus vs Actual
- Q1 2026 Revenue Actual: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $15,367,667,269
- Q1 2026 Revenue Estimate: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $15,826,531,035
- Q1 2026 EPS Actual: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $1.23
- Q1 2026 EPS Estimate: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $2.13
- Q1 2026 Revenue Miss: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = -$458,863,766 (-2.9%)
- Q1 2026 EPS Miss: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = -$0.90 (-42.4%)
- Q4 2025 Revenue Actual: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $17,711,863,065
- Q4 2025 EPS Actual: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $2.36
- Q4 2025 EPS Estimate: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $2.79

### Balance Sheet
- FY2025 Shareholders' Equity: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US) = $59,088,787,307
- FY2025 Total Assets: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US) = $90,057,794,025
- FY2025 Total Liabilities: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US) = $30,969,006,718
- FY2025 Debt-to-Equity Ratio: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US) = 34.4%
- FY2024 Shareholders' Equity: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US) = $42,923,722,001

### Cash Flow
- FY2025 Operating Cash Flow: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US) = $14,989,056,943
- FY2025 Free Cash Flow: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US) = $12,002,190,317
- FY2024 Free Cash Flow: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US) = $14,330,206,676
- FY2023 Free Cash Flow: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US) = $11,626,694,378

### Valuation
- Current PE (TTM): query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US) = 9.81
- PE 12-Month High: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US) = 12.99
- PE 12-Month Low: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US) = 9.81
- PE 12-Month Median: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US) = 10.59
- PE All-Time Low (2026-06-29): query_longbridge_by_route(fundamental/valuation/history, symbol=PDD.US) = 7.83

### Analyst Ratings
- Current Strong Buy: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = 18 (as of 2026-07-29)
- Current Buy: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = 4
- Current Hold: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = 14
- Current Sell: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = 0
- Current Underperform: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = 1
- Peak Strong Buy (2024-03-22): query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = 34
- Average Target Price: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = $116.27
- Min Target Price: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = $80.09
- Max Target Price: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = $170.33

### Forward Consensus Estimates
- Q2 2026E Revenue: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $16,863,654,752
- Q2 2026E EPS: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $2.53
- Q3 2026E Revenue: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $17,909,553,105
- Q3 2026E EPS: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $2.54
- Q4 2026E Revenue: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $20,128,612,149
- Q4 2026E EPS: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $2.95

## News Sources

### EU Regulatory Risk
- EU searches Temu European HQ: query_longbridge_by_route(news/company, symbol=PDD.US, count=20) = "The European Commission accused the Chinese e-commerce platform Temu of obstructing an investigation during a surprise search at its headquarters in Ireland"
- EU FSR charges: query_longbridge_by_route(news/company, symbol=PDD.US, count=20) = "Temu Responds To European Commission Statement Of Grounds Under Foreign Subsidies Regulation"
- EU formal charges: query_longbridge_by_route(news/company, symbol=PDD.US, count=20) = "EU Commission charges Temu for not cooperating in December raid"

### Business Strategy
- Temu warehouse restructuring: query_longbridge_by_route(news/company, symbol=PDD.US, count=20) = "Temu has recently closed multiple domestic warehouses in Guangdong and other regions... Temu is building and operating its own warehouses in Germany, Poland, and other locations"

### Organizational
- PDD Xiong'an employees: query_longbridge_by_route(news/company, symbol=PDD.US, count=20) = "PDD Xiong'an Company has surpassed 3,000 employees"

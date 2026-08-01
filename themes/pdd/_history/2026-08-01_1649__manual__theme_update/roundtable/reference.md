# PDD 数据来源记录 — Roundtable Session 2026-08-01_1649

## 一致预期数据（query_longbridge_by_route）

- Q1 2026 收入 (actual): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $15,367,667,269
- Q1 2026 收入 (estimate): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $15,826,531,035
- Q1 2026 净利润 GAAP (actual): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $1,815,117,541
- Q1 2026 净利润 GAAP (estimate): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $3,197,501,531
- Q1 2026 EPS GAAP (actual): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $1.2268
- Q1 2026 EPS GAAP (estimate): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $2.1285
- Q4 2025 净利润 GAAP (actual): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $3,507,861,492
- Q4 2025 净利润 GAAP (estimate): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $4,068,147,793
- Q2 2026E 收入: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $16,863,654,752
- Q3 2026E 收入: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $17,909,553,105
- Q4 2026E 收入: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) = $20,128,612,149

## 年度财务数据（query_longbridge_by_route）

- FY2025 总收入: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $60,529,636,024
- FY2025 营业利润: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $13,049,656,238
- FY2025 净利润: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $13,714,095,324
- FY2025 EPS: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $9.2509
- FY2024 总收入: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $54,703,209,149
- FY2024 净利润: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $15,616,975,367
- FY2024 EPS: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $10.5563
- FY2023 总收入: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $34,724,006,923
- FY2023 净利润: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US) = $8,416,931,113

## 估值数据（query_longbridge_by_route）

- 当前 P/E: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US) = 9.81
- P/E 52周高点: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US) = 12.99
- P/E 52周低点: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US) = 9.81
- P/E 中位数: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US) = 10.59

## 分析师评级（query_longbridge_by_route）

- Strong Buy 数量: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = 18 (截至 2026-07-29)
- Buy 数量: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = 4
- Hold 数量: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = 14
- Sell 数量: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = 1
- Underperform 数量: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = 1
- 平均目标价: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = $116.27
- 最新参考股价: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) = $88.56

## 中国宏观经济数据（query_indicators）

- 消费者信心指数: query_indicators(country=china, category=macro, time_range=7d) = 89.4 (2026年6月)
- 社零同比增速: query_indicators(country=china, category=macro, time_range=7d) = 1.0% (2026年6月)
- GDP 增速: query_indicators(country=china, category=macro, time_range=7d) = 4.7% (2026年第1-2季度)
- 制造业PMI: query_indicators(country=china, category=macro, time_range=7d) = 49.2 (2026年7月)
- 非制造业PMI: query_indicators(country=china, category=macro, time_range=7d) = 49.0 (2026年7月)
- 新增贷款同比: query_indicators(country=china, category=macro, time_range=7d) = -25.21% (2026年6月)
- 固定资产投资同比: query_indicators(country=china, category=macro, time_range=7d) = -15.6% (2026年6月)
- 10年期国债收益率: query_indicators(country=china, category=macro, time_range=7d) = 1.7141% (2026-07-31)
- Shibor 3M: query_indicators(country=china, category=macro, time_range=7d) = 1.43% (2026-07-31)
- LPR 1Y: query_indicators(country=china, category=macro, time_range=7d) = 3.0%

## 新闻数据

- PDD 相关新闻: query_raw_items(source=PDD, status=pending) = 无相关条目
- Temu 相关新闻: query_raw_items(source=Temu, status=pending) = 无相关条目



## buffett 交叉审查补充数据来源（2026-08-01）

| 数据点 | 来源工具 | 关键参数 | 值 |
|--------|----------|----------|-----|
| FY2022 收入 | query_longbridge_by_route | fundamental/financials/income, symbol=PDD.US | $19,287,243,583 |
| FY2022 营业利润 | query_longbridge_by_route | fundamental/financials/income, symbol=PDD.US | $4,491,269,027 |
| FY2022 净利润 | query_longbridge_by_route | fundamental/financials/income, symbol=PDD.US | $4,659,110,884 |
| FY2022 EPS | query_longbridge_by_route | fundamental/financials/income, symbol=PDD.US | $3.2401 |
| FY2022 经营现金流 | query_longbridge_by_route | fundamental/financials/cashflow, symbol=PDD.US | $7,166,055,368 |
| FY2022 自由现金流 | query_longbridge_by_route | fundamental/financials/cashflow, symbol=PDD.US | $5,717,848,780 |
| FY2025 总资产 | query_longbridge_by_route | fundamental/financials/balance, symbol=PDD.US | $90,057,794,025 |
| FY2025 总负债 | query_longbridge_by_route | fundamental/financials/balance, symbol=PDD.US | $30,969,006,718 |
| FY2025 股东权益 | query_longbridge_by_route | fundamental/financials/balance, symbol=PDD.US | $59,088,787,307 |
| FY2024 经营现金流 | query_longbridge_by_route | fundamental/financials/cashflow, symbol=PDD.US | $16,935,785,248 |
| FY2024 自由现金流 | query_longbridge_by_route | fundamental/financials/cashflow, symbol=PDD.US | $14,330,206,676 |
| FY2026E 全年 EPS (mean) | query_longbridge_by_route | analyst/forecast_eps, symbol=PDD.US | $11.102 (2026-07-27) |
| FY2026E 全年 EPS (median) | query_longbridge_by_route | analyst/forecast_eps, symbol=PDD.US | $11.706 (2026-07-27) |
| Q2 2025 GAAP EPS 实际 | query_longbridge_by_route | fundamental/consensus, symbol=PDD.US | $2.8932 |
| Q2 2025 Normalized EPS 实际 | query_longbridge_by_route | fundamental/consensus, symbol=PDD.US | $3.0772 |
| Q3 2025 GAAP EPS 实际 | query_longbridge_by_route | fundamental/consensus, symbol=PDD.US | $2.7671 |
| Q3 2025 Normalized EPS 实际 | query_longbridge_by_route | fundamental/consensus, symbol=PDD.US | $2.9609 |
| Q4 2025 GAAP EPS 实际 | query_longbridge_by_route | fundamental/consensus, symbol=PDD.US | $2.3599 |
| Q4 2025 Normalized EPS 实际 | query_longbridge_by_route | fundamental/consensus, symbol=PDD.US | $2.5286 |
| Q1 2026 GAAP EPS 实际 | query_longbridge_by_route | fundamental/consensus, symbol=PDD.US | $1.2268 |
| Q1 2026 Normalized EPS 实际 | query_longbridge_by_route | fundamental/consensus, symbol=PDD.US | $1.3758 |
| Q1 2025 Normalized EPS 实际 | query_longbridge_by_route | fundamental/consensus, symbol=PDD.US | $1.5708 |
| Q3 2025 净利润 GAAP | query_longbridge_by_route | fundamental/consensus, symbol=PDD.US | $4,119,474,113 |
| Q1 2026 净利润 GAAP | query_longbridge_by_route | fundamental/consensus, symbol=PDD.US | $1,815,117,541 |

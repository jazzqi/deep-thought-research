# Reference — PDD Holdings (buffett 分析)

> Agent: buffett | Session: 2026-08-01_1733__manual__theme_update

## 宏观指标

- GDP 同比 4.7% (2026 H1): query_indicators(category=macro, country=china) = 4.7
- 消费者信心指数 89.4 (2026-06): query_indicators(category=macro, country=china) = 89.4
- 社零同比 +1.0% (2026-06): query_indicators(category=macro, country=china) = 1.0
- 制造业 PMI 49.2 (2026-07): query_indicators(category=macro, country=china) = 49.2
- 非制造业 PMI 49.0 (2026-07): query_indicators(category=macro, country=china) = 49.0
- 固定资产投资同比 -15.6% (2026-06): query_indicators(category=macro, country=china) = -15.6
- 新增贷款同比 -25.2% (2026-06): query_indicators(category=macro, country=china) = -25.21
- LPR 1年期 3.0% (2026-08-01): query_indicators(category=macro, country=china) = 3.0
- 10Y 国债收益率 1.71% (2026-07-31): query_indicators(category=macro, country=china) = 1.7141
- CPI 同比 0.0% (2025-08-09, ⚠️ 过时): query_indicators(category=macro, country=china) = 0.0

## 财务数据

- FY2025 Revenue $60.53B / Net Income $13.71B / EPS $9.25 / Operating Income $13.05B: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US)
- FY2024 Revenue $54.70B / Net Income $15.62B / EPS $10.56 / Operating Income $15.06B: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US)
- FY2023 Revenue $34.72B / Net Income $8.42B / EPS $5.77: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US)
- FY2022 Revenue $19.29B / Net Income $4.66B / EPS $3.24: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US)
- FY2021 Revenue $14.53B / Net Income $1.20B / EPS $0.84: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US)

## 资产负债表

- FY2025: Total Assets $90.06B, Total Liabilities $30.97B, Shareholders' Equity $59.09B, Debt Ratio 34.4%: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US)
- FY2024: Total Assets $69.19B, Total Liabilities $26.27B, Shareholders' Equity $42.92B, Debt Ratio 38.0%: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US)
- FY2023: Total Assets $49.04B, Total Liabilities $22.66B, Shareholders' Equity $26.38B: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US)

## 估值

- 当前 PE 9.81x (Low 9.81, High 12.99, Median 10.59): query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)
- 分析师平均目标价 $116.27 (Low $80.09, High $170.33, 2026-07-27): query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)

## 季度一致预期

- Q1 2026: Revenue $15.37B (Miss, est $15.83B) / Net Income $1.82B (Miss, est $3.20B, 57% of target) / EPS $1.23 (Miss, est $2.13): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q4 2025: Revenue $17.71B (Miss) / Net Income $3.51B (Miss, est $4.07B): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q3 2025: Revenue $15.21B (Miss) / Net Income $4.12B (Beat, est $3.23B): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q2 2025: Revenue $14.50B (Beat) / Net Income $4.29B (Beat, est $2.88B): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q2 2026E: Revenue $16.86B / Net Income $3.66B / EPS $2.53: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q3 2026E: Revenue $17.91B / Net Income $3.69B / EPS $2.54: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q4 2026E: Revenue $20.13B / Net Income $4.04B / EPS $2.95: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)

## 分析师评级

- 2026-07-29: Strong Buy 18 / Buy 4 / Hold 14 / Sell 1 (首次出现 Sell): query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 2024-03 峰值: Strong Buy 34 / Buy 7 / Hold 2 / Sell 0: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 2025-05: Strong Buy 24 / Buy 5 / Hold 12 / Sell 1: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 最近一次目标价数据 (2026-07-27): avg $116.27, min $80.09, max $170.33, price $88.56: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)

## 近期重大新闻

- EU Commission charges Temu for not cooperating in investigation under Foreign Subsidies Regulation (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US) — URL: https://longportapp.cn/news/294491041
- EU searches Temu European HQ in Ireland, accuses company of obstructing investigation (2026-08-01): query_longbridge_by_route(news/company, symbol=PDD.US) — URL: https://longportapp.cn/news/294541903
- Temu Responds To European Commission Statement Of Grounds Under Foreign Subsidies Regulation (2026-08-01): query_longbridge_by_route(news/company, symbol=PDD.US) — URL: https://longportapp.cn/news/294577628
- Temu shuts down domestic warehouses, builds warehouses in Germany/Poland — strategic shift from cross-border direct mail to localized logistics (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US) — URL: https://longportapp.cn/news/294452061
- PDD Xiong'an company employees exceed 3,000, plans to recruit 5,000 in coming year (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US) — URL: https://longportapp.cn/news/294451407
- GOME Retail offshore debt restructuring, negotiations with Pinduoduo remain unresolved (2026-07-30): query_longbridge_by_route(news/company, symbol=PDD.US) — URL: https://longportapp.cn/news/294329012
- PDD and Li Auto saw slight declines on 2026-07-31; NASDAQ Golden Dragon China Index closed up 1.05% (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US) — URL: https://longportapp.cn/news/294411664

## 数据说明

- query_raw_items(source=PDD) 和 query_raw_items(source=Temu) 在查询时均返回空结果，新闻数据主要通过 query_longbridge_by_route(news/company, symbol=PDD.US) 获取。
- 宏观数据中部分指标（CPI、PPI、进出口等）数据期在 2025-08，超过 90 天，已标记为过时，不用于核心判断。

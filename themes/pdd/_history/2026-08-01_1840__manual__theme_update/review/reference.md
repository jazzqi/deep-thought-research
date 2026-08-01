# Buffett 审查数据来源

## 财务数据（交叉核验）
- FY2025 总收入 $605.3亿: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8) = $60,529,636,024
- FY2025 经营利润 $130.5亿: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8) = $13,049,656,238
- FY2025 净利润 $137.1亿: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8) = $13,714,095,324
- FY2025 EPS $9.25: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8) = 9.2509
- FY2025 总资产 $900.6亿: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=8) = $90,057,794,025
- FY2025 总负债 $309.7亿: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=8) = $30,969,006,718
- FY2025 股东权益 $590.9亿: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=8) = $59,088,787,307
- FY2025 经营现金流 $149.9亿: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US, count=8) = $14,989,056,943
- FY2025 自由现金流 $120.0亿: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US, count=8) = $12,002,190,317

## 估值
- PE TTM 当前 9.81, median 10.59, high 12.99, low 9.81: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)
- PE 历史低点 7.83 (2026-06-29), 历史高点 63.14 (2022-01-24): query_longbridge_by_route(fundamental/valuation/history, symbol=PDD.US)

## 一致预期
- Q1 2026 GAAP: Revenue $153.7亿 actual vs $158.3亿 est (Miss), NI $18.2亿 vs $32.0亿 (Miss 43%), EPS $1.23 vs $2.13 (Miss): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q3 2025 EPS $2.77 actual vs $2.09 est (Beat +32%): query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q2-Q4 2026E 季度预期: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- ⚠️ FY2026E 年度汇总（GAAP 季度求和）: Revenue ~$703亿, NI ~$132亿, EPS ~$9.25 — 与文档声称的 $155亿/$10.8 不符

## 分析师评级
- SB18/B4/H14/S0/U1, Total 37, 2026-07-29: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US, count=20)
- 目标价 avg $116.27, max $170.33, min $80.09, 2026-07-27: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 聚合评级 Buy, target $170.20: query_longbridge_by_route(market/institutional_rating, symbol=PDD.US)

## 公司新闻
- EU FSR Statement of Grounds (2026-08-01): query_longbridge_by_route(news/company, symbol=PDD.US, count=30)
- EU Commission charges Temu for obstructing December raid (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US, count=30)
- Temu 关闭国内仓库/建设欧洲自有仓储 (2026-07-31): query_longbridge_by_route(news/company, symbol=PDD.US, count=30)

## 宏观指标
- GDP 4.7% (2026 Q1-Q2): query_indicators(category=macro, country=china, limit=20, time_range=7d) = gdp_quarterly 4.7
- 制造业PMI 49.2 (2026年7月): query_indicators(category=macro, country=china) = manufacturing_pmi 49.2
- 非制造业PMI 49.0 (2026年7月): query_indicators(category=macro, country=china) = non_manufacturing_pmi 49.0
- 社零同比 +1.0% (2026年6月): query_indicators(category=macro, country=china) = retail_sales_yoy 1.0
- 消费者信心 89.4 (2026年6月): query_indicators(category=macro, country=china) = consumer_confidence 89.4
- 1年期LPR 3.0%: query_indicators(category=macro, country=china) = lpr_1y 3.0
- 10年期国债 1.7141% (2026-07-31): query_indicators(category=macro, country=china) = bond_10y_yield 1.7141
- 新增贷款同比 -25.2% (2026年6月): query_indicators(category=macro, country=china) = new_loan_yoy -25.21186441

# buffett 审查数据来源

## 财务数据
- FY2021-FY2025 利润表（收入/净利润/EPS/经营利润）: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US)
- FY2022-FY2025 资产负债表（总资产/总负债/股东权益）: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US)
- FY2016-FY2025 现金流量表（经营现金流/自由现金流）: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US)

## 估值
- PE TTM 当前值/历史区间: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US) = current 9.81, high 12.99, low 9.81, median 10.59
- PE 完整历史时间序列（2021-2026）: query_longbridge_by_route(fundamental/valuation/history, symbol=PDD.US) — 显示 PE 实际低至 7.83（2026-06-29），高至 63.14（2022-01-24）

## 一致预期
- Q1 2026 实际 vs 预期: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) — Revenue $15.37B vs $15.83B (Miss), Net Income $1.82B vs $3.20B (Miss), EPS $1.23 vs $2.13 (Miss)
- Q4 2025 实际 vs 预期: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) — EPS $2.36 vs $2.79 (Miss -15%)
- Q3 2025 实际 vs 预期: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) — EPS $2.77 vs $2.09 (Beat +32%)
- Q2 2025 实际 vs 预期: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US) — EPS $2.89 vs $1.72 (Beat +69%)
- Q2-Q4 2026E 季度预期: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)

## 分析师评级
- 评级历史趋势（2021-2026）: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) — 2026-07-29: SB18/B4/H14/S0/U1, Total 37
- 目标价趋势: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US) — 2026-07-27: avg $116.27, max $170.33, min $80.09

## 机构评级
- 最新聚合评级: query_longbridge_by_route(market/institutional_rating, symbol=PDD.US) — Buy (SB18/B4/H14/U1), target $170.20

## 新闻
- PDD/Temu 最新新闻（30条）: query_longbridge_by_route(news/company, symbol=PDD.US, count=30)
  - EU FSR Statement of Grounds (2026-08-01)
  - EU Commission charges Temu for obstructing December raid (2026-07-31)
  - Temu 关闭国内仓库/建设欧洲自有仓储 (2026-07-31)
  - PDD 雄安公司员工突破 3000 (2026-07-31)

## 宏观指标
- 中国宏观指标（GDP/PMI/CPI/PPI/社零/消费者信心/LPR/国债/SHIBOR）: 无法从 query_indicators 获取（数据库无快照），数字来源待确认

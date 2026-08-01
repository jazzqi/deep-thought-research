# 参考数据源 — PDD Holdings (buffett 审查交叉核验)

## 财务数据
- FY2022-FY2025 利润表（收入、净利润、EPS、经营利润）: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=5)
- FY2023-FY2025 资产负债表（总资产、总负债、股东权益）: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=5)

## 估值数据
- PE (TTM) 9.81x, 区间 Low 9.81 / Median 10.59 / High 12.99: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)

## 分析师一致预期
- Q2-Q4 2026E 收入/净利润/EPS 预期及 Q1 2026 实际: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US, count=10)
- Q2-Q4 2025 实际/预期: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US, count=10)

## 分析师评级与目标价
- Strong Buy 从 34→18, Hold 2→14, Sell 0→1 趋势; 目标价均值 $116.27, 区间 $80.09-$170.33: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)

## 新闻事件
- EU 反补贴调查（Temu Ireland raid, 不配合指控, 正式回应）: query_longbridge_by_route(news/company, symbol=PDD.US, count=30)
- Temu 物流转型（关闭国内仓/建海外仓）: query_longbridge_by_route(news/company, symbol=PDD.US, count=30)
- 雄安招聘 3,000+ 人: query_longbridge_by_route(news/company, symbol=PDD.US, count=30)
- 国美零售离岸债务重组: query_longbridge_by_route(news/company, symbol=PDD.US, count=30)

## 宏观指标（中国）
- GDP 同比 4.7% (2026 H1): query_indicators(category=macro, country=china)
- 消费者信心指数 89.4 (2026年6月): query_indicators(category=macro, country=china)
- 社零同比 +1.0% (2026年6月): query_indicators(category=macro, country=china)
- 制造业 PMI 49.2, 非制造业 PMI 49.0 (2026年7月): query_indicators(category=pmi, country=china)
- 固定资产投资同比 -15.6% (2026年6月): query_indicators(category=macro, country=china)
- 新增贷款同比 -25.2% (2026年6月): query_indicators(category=macro, country=china)
- LPR 1年期 3.0%: query_indicators(category=macro, country=china)
- 10Y 国债收益率 1.71% (2026-07-31): query_indicators(category=macro, country=china)

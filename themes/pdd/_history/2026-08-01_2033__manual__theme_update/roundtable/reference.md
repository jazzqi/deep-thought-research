# 数据来源参考

## 损益表数据
- FY2022 收入 $192.9亿 / 经营利润 $44.9亿 / 净利润 $46.6亿 / EPS 3.24: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=5)
- FY2023 收入 $347.2亿 / 经营利润 $82.3亿 / 净利润 $84.2亿 / EPS 5.77: 同上
- FY2024 收入 $547.0亿 / 经营利润 $150.6亿 / 净利润 $156.2亿 / EPS 10.56: 同上
- FY2025 收入 $605.3亿 / 经营利润 $130.5亿 / 净利润 $137.1亿 / EPS 9.25: 同上

## 资产负债表数据
- FY2025 股东权益 $590.9亿 / 总资产 $900.6亿 / 总负债 $309.7亿 / 资产负债率 34.4%: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=3)

## 估值数据
- PE TTM 9.81x / Low 9.81 / High 12.99 / Median 10.59: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)
- PE 历史序列 (2021-2026): query_longbridge_by_route(fundamental/valuation/history, symbol=PDD.US)

## 分析师一致预期
- Q1 2026 实际: 收入 $153.7亿 / EBIT $30.5亿 / 净利润 $18.2亿 / EPS 1.23: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q1 2026 预期: 收入 $158.3亿 / EBIT $32.2亿 / 净利润 $32.0亿 / EPS 2.13: 同上
- Q2 2026 预期: 收入 $168.6亿 / 净利润 $36.6亿 / EPS 2.53: 同上
- Q3 2026 预期: 收入 $178.8亿 / 净利润 $36.8亿 / EPS 2.55: 同上
- Q4 2026 预期: 收入 $201.3亿 / 净利润 $40.4亿 / EPS 2.95: 同上

## 分析师评级
- 07/29/2026 Strong Buy 18 / Buy 4 / Hold 14 / Sell 0: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 07/27/2026 平均目标价 $116.27 / Low $80.09 / High $170.33: 同上

## 公司新闻 (重大事件)
- 欧盟 FSR 指控 Temu 阻挠调查 (2026-08-01): query_longbridge_by_route(news/company, symbol=PDD.US, count=20)
- Temu 关闭国内仓、建欧洲仓 (2026-07-31): 同上
- PDD 雄安公司扩招超 3,000 人 (2026-07-31): 同上
- 国美零售债务重组涉及 PDD (2026-07-30): 同上

## 宏观数据
- 中国宏观指标 (GDP/社零/PMI/信贷等): query_indicators(category=macro, country=china) — 未返回数据，待验证
- 中国 PMI 数据: query_indicators(category=pmi, country=china) — 未返回数据，待验证

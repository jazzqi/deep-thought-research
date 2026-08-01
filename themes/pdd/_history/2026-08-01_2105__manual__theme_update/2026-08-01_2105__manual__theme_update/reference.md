# reference.md — PDD 圆桌数据溯源记录
# Updated: 2026-08-01

## 宏观数据

- 消费者信心指数 89.4（2026年06月）: query_indicators(category=macro, country=china)
- 零售销售同比 +1.0%（2026年06月）: query_indicators(category=macro, country=china)
- CPI同比 0.0%（数据日期2025-08-09，⚠️已过时）: query_indicators(category=macro, country=china)
- 制造业PMI 49.2（2026年07月）: query_indicators(category=macro, country=china)
- 非制造业PMI 49.0（2026年07月）: query_indicators(category=macro, country=china)
- LPR 1年期 3.0%（2026-08-01）: query_indicators(category=macro, country=china)
- 10年期国债收益率 1.7141%（2026-07-31）: query_indicators(category=macro, country=china)
- Shibor 3个月 1.43%（2026-07-31）: query_indicators(category=macro, country=china)
- GDP季度同比 4.7%（2026年第1-2季度）: query_indicators(category=macro, country=china)
- 社融同比 +6245.0（2026年04月）: query_indicators(category=macro, country=china)
- 固定资产投资同比 -15.6%（2026年06月）: query_indicators(category=macro, country=china)
- 新增贷款同比 -25.21%（2026年06月）: query_indicators(category=macro, country=china)

## 公司财务数据（长期桥路证券）

- FY2025营收 $605.3亿 / 营业利润 $130.5亿 / 净利润 $137.1亿 / EPS $9.25: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, period=annual)
- FY2024营收 $547.0亿 / 营业利润 $150.6亿 / 净利润 $156.2亿 / EPS $10.56: 同上
- FY2023营收 $347.2亿 / 营业利润 $82.3亿 / 净利润 $84.2亿 / EPS $5.77: 同上
- FY2025总资产 $900.6亿 / 净资产 $590.9亿 / 总负债 $309.7亿: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, period=annual)
- FY2025经营现金流 $149.9亿 / 自由现金流 $120.0亿: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US, period=annual)
- FY2024经营现金流 $169.4亿 / 自由现金流 $143.3亿: 同上

## Q1 2026 财报（一致预期对比）

- Q1 2026 营收实际 $153.7亿 vs 预期 $158.3亿（Miss）: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q1 2026 净利润实际 $18.2亿 vs 预期 $32.0亿（Miss，差距43.2%）: 同上
- Q1 2026 EPS实际 $1.23 vs 预期 $2.13（Miss）: 同上

## 分析师一致预期

- Q2 2026 预期营收 $168.6亿 / 净利润 $36.6亿 / EPS $2.53: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- Q3 2026 预期营收 $178.8亿 / 净利润 $36.8亿 / EPS $2.55: 同上
- Q4 2026 预期营收 $201.3亿 / 净利润 $40.4亿 / EPS $2.95: 同上
- 2026全年预期Normalized EPS: Q1 $1.38 + Q2 $2.71 + Q3 $2.74 + Q4 $3.01 = ~$9.84: 同上

## 估值数据

- 当前PE 9.81x（区间低点9.81x / 高点12.99x / 中位数10.59x）: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)

## 公司近期新闻事件

- 欧盟指控Temu在2025年12月爱尔兰总部搜查中不配合调查，或面临年营收1%罚款（2026-08-01）: query_longbridge_by_route(news/company, symbol=PDD.US)
- 欧盟此前已因Temu平台销售违法商品对其罚款€2亿（新闻提及）: 同上
- 欧盟自2026年7月起取消对中国小包裹免税政策（新闻提及）: 同上
- Temu关闭国内多个仓库，同时在德国、波兰等地自建海外仓，从"全托管/Y2直邮"向本地仓储转型（2026-07-31）: 同上
- PDD雄安公司员工超3000人，计划2026年招聘5000人才（2026-07-31）: 同上
- PDD美股盘前涨0.4%（2026-07-31）: 同上

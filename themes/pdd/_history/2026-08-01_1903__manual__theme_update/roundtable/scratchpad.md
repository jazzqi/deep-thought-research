# buffett 交叉审查 — PDD Holdings

## 审查日期: 2026-08-01

### 分级审查结果

#### 🚫 blocker (3)

1. **Q4 2025 净利润 miss 数值来源错误** — 文档写 "Miss $0.56B"，GAAP miss 确为 $560M，但表格中 "实际 vs 预期" 列写 Norm $3.72B vs $4.12B 与 consensus 数据不符（consensus Q4 2025 normalized estimate = $4,509M, actual = $3,759M）。数值来源需核实。

2. **"卖出评级始终为零"与事实不符** — 2025-05-30 至 2026-06-19 期间 sell=1，当前 sell=0。应修正为"当前卖出评级为零"。

3. **"自 2020 年首次盈利以来"应为 FY2021** — FY2020 净亏损 $10.47 亿，FY2021 才是首次盈利（$12.01 亿）。

#### ⚠️ concern (5)

4. Q1 2025 净利润混合使用 GAAP 和 normalized 口径，建议统一
5. FCF 收益率计算中 $1,200 亿市值推导过程未注明
6. 悲观情景 PE 10x × $13B ≠ $88 目标价，内部逻辑需检查
7. FY2026E $13.2B 未明确标注 GAAP basis
8. GOME 与 PDD 债务谈判新闻未提及（影响小）

#### 🔧 nit (4)

9. PE 历史区间基本准确
10. 股价 $88 需注明数据日期
11. 资产负债表可补充 FY2022 数据
12. 宏观数据建议注明发布日期

#### ✅ pass (13)

13-25. 损益表、资产负债表、现金流、PE 估值、一致预期、评级分布、Q1 2026 数据、全部宏观指标、欧盟监管新闻、物流转型、雄安扩张、投资框架、预测时间线 — 均已交叉验证通过。

### 数据来源记录
- 损益表: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=8)
- 资产负债表: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=5)
- 现金流: query_longbridge_by_route(fundamental/financials/cashflow, symbol=PDD.US, count=5)
- PE 估值: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)
- PE 历史: query_longbridge_by_route(fundamental/valuation/history, symbol=PDD.US)
- 一致预期: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- 分析师评级: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 公司新闻: query_longbridge_by_route(news/company, symbol=PDD.US, count=20)
- 宏观指标: query_indicators(category=macro, country=china, limit=15, time_range=24h)

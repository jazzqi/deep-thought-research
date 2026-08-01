# buffett 交叉审查 — PDD 主题文档

**审查时间**: 2026-08-01
**审查对象**: drafts/current.md
**审查范围**: 全篇（叙事/基本面/宏观/事件追踪/估值/一致性）

---

## 审查结论（分级列表）

### 🚫 blocker
（无）

### ⚠️ concern

1. **场景定价自相矛盾**：文档内存在两套不同的情景假设。"估值与目标价" section 给出悲观 $120亿 / 基准 $140亿 / 乐观 $160亿；但"分歧地图" section 给出悲观 $130亿 / 基准 $150亿 / 乐观 $170亿。两套假设的净利润和目标价均不同，读者会困惑于哪个是 buffett 的真实判断。建议统一为一套，并在分歧地图中标注"buffett 偏保守估计"。

2. **"PE 9.81x 是盈利以来的历史最低"——与数据不符**：查询 fundamental/valuation/history 路由返回的 PE 历史数据显示，2026年6月29日 PE 曾低至 7.83，2026年6月22日为 7.99，2025年4月21日为 8.39，均低于当前 9.81。因此"盈利以来历史最低"的说法不成立。实际应为"近期区间低位"或"近两个月反弹后的水平"。该表述若被读者直接引用会产生误导。

3. **中国宏观数据未交叉验证**：宏观背景表中列出 GDP 4.7%、社零 +1.0%、消费者信心 89.4、制造业 PMI 49.2、非制造业 PMI 49.0、新增贷款 -25.2%、固投 -15.6%、10Y 国债 1.71%、1年期 LPR 3.0% 等九项指标，但通过 query_indicators(category='macro'/'pmi', country='china') 均未返回数据。这些数字的准确性无法从可用工具确认。建议在参考文献中标注来源（如 Wind/统计局/央行），或在无法确认时加注"⚠️ 数据待验证"。

### 🔧 nit

1. **"2023 年营销费用同比增长 44%"**：此数据出自 lynch 视角，但无法从可用工具（query_longbridge_by_route 返回的 income statement 中无 marketing expense 分项）验证。建议标注来源或移除具体数字。

2. **FY2024 收入增速四舍五入偏差**：实际计算 (54.70-34.72)/34.72 = 57.66%，文档写 +58%。虽在合理四舍五入范围内，但与前一年的 +80%（实际 79.9%）精度不一致。建议统一保留一位小数：+57.7%。

3. **Q1 2026 EBIT margin 精度**：实际 30.51/153.68 = 19.85%，文档写 19.9%。建议标注为 ~19.9% 或 19.85%。

4. **分析师评级日期标注**：文档写"分析师评级 (07/29/2026)"，数据源确认该日期对应 SB:18, B:4, H:14, S:0，数据准确。但建议补充 Underperform/Sell 合计为 0 的说明（当前只写了 S:0，未提 U:0）。

### ✅ pass

1. **FY2022-FY2025 损益表全部数据点经验证通过**：收入、经营利润、净利润、EPS 四项 × 四年 = 16 个数据点全部与 query_longbridge_by_route(fundamental/financials/income) 返回值匹配。

2. **FY2025 资产负债表数据通过**：股东权益 $591亿（实际 $590.9亿）、资产负债率 34.4%（实际 30,969/90,058 = 34.4%）均准确。

3. **FY2026 Q1 "double miss" 数据完全匹配**：收入 $153.7亿 vs 预期 $158.3亿（miss 2.9%）、EBIT $30.5亿 vs $32.2亿（miss 5.2%）、净利润 $18.2亿 vs $32.0亿（miss 43.2%）、EPS 1.23 vs 2.13（miss 42.3%）——所有数字与 consensus 数据源一致。

4. **Q2-Q4 2026 分析师一致预期四季度数据全部匹配**：收入/EBIT/净利润/EPS 各四季度共 16 个数据点全部准确。

5. **PE TTM 9.81x 及其区间（Low 9.81, High 12.99, Median 10.59）与 fundamental/valuation/pe 路由返回值一致**。（但见 concern #2 关于"历史最低"的表述问题。）

6. **分析师目标价 $116.27（Low $80, High $170）与 fundamental/consensus 路由最新数据一致**（07/27/2026: avg 116.27, min 80.09, max 170.33）。

7. **重大事件追踪四项全部与 news/company 路由返回的最新新闻匹配**：
   - 欧盟 FSR 指控 Temu（2026-08-01）✓ 多条新闻确认
   - Temu 关闭国内仓、建欧洲仓（2026-07-31）✓
   - PDD 雄安公司扩招（2026-07-31）✓
   - 国美零售债务重组涉及 PDD（2026-07-30）✓
   未发现被遗漏的重大新闻事件。

8. **叙事框架"消费降级的全球化"逻辑自洽**，三位 agent 视角互补，分歧地图清晰。

9. **预测时间线合理**，置信度标注恰当，未做过度确定性承诺。

---

## 数据来源汇总

以下为审查中使用的数据查询：

- FY2022-FY2025 损益表: query_longbridge_by_route(fundamental/financials/income, symbol=PDD.US, count=5)
- FY2022-FY2025 资产负债表: query_longbridge_by_route(fundamental/financials/balance, symbol=PDD.US, count=3)
- PE TTM 及区间: query_longbridge_by_route(fundamental/valuation/pe, symbol=PDD.US)
- PE 历史: query_longbridge_by_route(fundamental/valuation/history, symbol=PDD.US)
- 分析师一致预期: query_longbridge_by_route(fundamental/consensus, symbol=PDD.US)
- 分析师评级: query_longbridge_by_route(analyst/rating_detail, symbol=PDD.US)
- 公司新闻: query_longbridge_by_route(news/company, symbol=PDD.US, count=20)
- 宏观指标: query_indicators(category=macro/pmi, country=china) — 未返回数据

---

## 总结

文档整体质量很高，财务数据准确率接近 100%，重大事件覆盖完整，叙事逻辑清晰。主要改进点是统一两套场景定价假设、修正"PE 历史最低"的不准确表述、以及对宏观数据标注来源。无 blocker，不阻塞发布。

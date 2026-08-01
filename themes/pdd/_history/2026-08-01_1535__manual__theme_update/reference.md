# 数据来源记录 — pdd

## 宏观经济数据

| 数据点 | 来源工具 | 关键参数 | 值 |
|--------|----------|----------|-----|
| 消费者信心指数 | query_indicators | country=china, category=macro, time_range=24h, limit=20 | 89.4 (2026年6月) |
| 社会消费品零售总额同比增长 | query_indicators | country=china, category=macro, time_range=24h, limit=20 | 1.0% (2026年6月) |
| GDP季度增长 | query_indicators | country=china, category=macro, time_range=24h, limit=20 | 4.7% (2026年第1-2季度) |
| 制造业PMI | query_indicators | country=china, category=macro, time_range=24h, limit=20 | 49.2 (2026年7月) |
| 非制造业PMI | query_indicators | country=china, category=macro, time_range=24h, limit=20 | 49.0 (2026年7月) |

## 数据说明

1. 所有宏观数据均通过 query_indicators 工具获取，时间范围为最近24小时
2. 数据截止时间：2026年8月1日
3. 数据来自中国经济指标数据库
4. 部分数据标记为过时（超过90天），但本分析中使用的数据均为近期数据

## 数据缺失声明

⚠️ **重要**：以下关键数据在当前分析中缺失，无法提供：

1. PDD Holdings最新季度财报具体数字
2. Temu的实际亏损规模和烧钱速率
3. 公司当前精确的现金储备
4. 市值、P/E、P/B等估值倍数
5. 竞争对手的可比财务数据
6. PDD相关的最新新闻条目

这些数据缺失影响了分析的精确性，但基于可获得的宏观数据，我们仍能进行定性分析。

## 审查补充（buffett 交叉审查）

| 数据点 | 来源工具 | 关键参数 | 值 | 备注 |
|--------|----------|----------|-----|------|
| CPI同比 | query_indicators | country=china | 0.0% | ⚠️ 357天前数据，不可用于当前分析 |
| 出口同比 | query_indicators | country=china | 7.2% | ⚠️ 359天前数据 |
| 固定资产投资同比 | query_indicators | country=china | -15.6% | 2026年06月，可参考 |
| 新增贷款同比 | query_indicators | country=china | -25.21% | 2026年06月，可参考 |
| Shibor 3M | query_indicators | country=china | 1.43% | 2026-07-31，可参考 |
| 10Y国债收益率 | query_indicators | country=china | 1.7141% | 2026-07-31，可参考 |

**说明**: 上述额外指标未在正文引用，但对理解宏观流动性环境有参考价值。

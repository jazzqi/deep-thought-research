---
slug: disruptive-innovation
lead_agent: kevin_kelly
depends_on: []
---
# 颠覆式创新扫描

> 持续扫描可能出现的颠覆式创新投资机会。跨越 AI、生物科技、新能源/材料、新商业模式等领域的早期信号监测。

## 范围

持续扫描可能出现的颠覆式创新投资机会。跨越 AI、生物科技、新能源/材料、新商业模式等领域的早期信号监测。

## 分析框架

- **技术成熟度** — 从学术论文→原型→产品→早期 adopt→主流渗透的转化进度（S-curve 定位）
- **"Demo vs Product" 检验** — 区分技术演示和可量产产品；无产品化证据一律按早期信号处理
- **范式迁移信号** — 识别何时一个技术/模式可能重塑行业格局，区分技术进展与商业成功
- **交叉领域融合** — 不同技术的结合创造的新可能性（如 AI+生物、AI+能源、AI+机器人）

## 报告结构

报告结构蓝本见 `template.md`（v1，2026-08-08 冷启动）。核心约定：

- **顶层节**（SEED FORMAT，publish 精确匹配）：`## Big Picture` / `## 共识` / `## 各维度分析` / `## 预测时间线` / `## 分歧地图` / `## 更新日志`
- **各维度分析**按领域组织：AI/前沿技术、生物科技/医疗、能源/材料、消费/商业模式、其他前沿
- 每领域子节必答三件事：**当前状态**（带来源与日期）→ **成熟度定位**（S-curve + Demo vs Product 检验）→ **投资信号**（方向 + 跟踪指标 + 时间窗口 + 置信度）
- `## 信号强度汇总` 表：领域/方向/信号强度/时间窗口/置信度/备注

## 典型参与 Agent

- kevin_kelly（lead — 技术趋势前瞻 / 5-30 年范式转换判断）
- ai_specialist（AI/前沿技术趋势评估）
- karpathy（工程可实现性的现实检验）

## 数据源

- 新闻/进展：`query_raw_items`（关键词覆盖领域+公司+技术词；source 优先 `telegram:Financial_Express`，次选 hackernews/solidot/36kr/longbridge）
- 可交易标的：`QueryLongbridgeByRouteTool`（NVDA/TSLA/NVO/LLY/CRSP 等受影响上市公司基本面/估值/一致预期/新闻）
- 宏观：`query_indicators`（利率/流动性；部分分类当前无有效指标需诚实标注）
- 行情：`market_quote` / `binance_get_price`

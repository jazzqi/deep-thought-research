# buffett 交叉审查数据来源

## 核验工具使用记录

### 1. 财务数据核验
- **工具**: query_longbridge_by_route
- **路径**: fundamental/financials/income
- **参数**: symbol=PDD.US
- **验证数据**:
  - FY2022收入: $19.29B (实际: $19,287,243,582.6557)
  - FY2023收入: $34.72B (实际: $34,724,006,922.9747)
  - FY2024收入: $54.70B (实际: $54,703,209,148.8562)
  - FY2025收入: $60.53B (实际: $60,529,636,024.1173)
  - FY2022净利润: $4.66B (实际: $4,659,110,884.1547)
  - FY2023净利润: $8.42B (实际: $8,416,931,113.2228)
  - FY2024净利润: $15.62B (实际: $15,616,975,367.0029)
  - FY2025净利润: $13.71B (实际: $13,714,095,324.0064)

### 2. 资产负债表核验
- **工具**: query_longbridge_by_route
- **路径**: fundamental/financials/balance
- **参数**: symbol=PDD.US
- **验证数据**:
  - FY2025总资产: $90.06B (实际: $90,057,794,025.1572)
  - FY2025总负债: $30.97B (实际: $30,969,006,718.1246)
  - FY2025股东权益: $59.09B (实际: $59,088,787,307.03259)
  - FY2024股东权益: $42.92B (实际: $42,923,722,000.73981)

### 3. 分析师评级核验
- **工具**: query_longbridge_by_route
- **路径**: analyst/rating_detail
- **参数**: symbol=PDD.US
- **验证数据**:
  - 2024-03-22: Strong Buy 34, Buy 7, Hold 2, Sell 0
  - 2025-05-30: Strong Buy 24, Buy 5, Hold 12, Sell 1
  - 2026-07-29: Strong Buy 18, Buy 4, Hold 14, Sell 1

### 4. 新闻事件核验
- **工具**: query_longbridge_by_route
- **路径**: news/company
- **参数**: symbol=PDD.US
- **验证事件**:
  1. "Temu Responds To European Commission Statement Of Grounds Under Foreign Subsidies Regulation" (2026-08-01)
  2. "The EU suddenly searches the European headquarters of Chinese e-commerce platform Temu, accusing the company of obstructing the investigation" (2026-08-01)
  3. "EU Commission charges Temu for not cooperating in December raid" (2026-07-31)
  4. "Temu has changed by shutting down a number of domestic warehouses" (2026-07-31)
  5. "PDD Xiong'an company's employees exceed 3,000" (2026-07-31)

### 5. 股价参考
- **数据来源**: 分析师评级数据中的price字段
- **最新数据点**: 2026-07-27 price: $88.56
- **文档中引用**: "股价约 $88"

## 未查询的数据
- **宏观指标**: query_indicators对China数据查询无返回结果
- **实时股价**: 未查询最新实时价格，使用文档中提供的$88作为参考
- **季度业绩详细数据**: 文档中引用的季度数据来源为"query_longbridge_by_route, fundamental/consensus"，但未提供具体查询参数

## 数据验证结论
所有核心财务数据、分析师评级数据、新闻事件均与工具查询结果一致。文档数据准确可靠。
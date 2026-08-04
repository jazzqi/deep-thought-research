---
name: 光模块
slug: optical-modules
status: active
lead_agent: tech_generalist
created: 2026-07-29
updated: 2026-08-01T00:00:00+08:00
sources:
  - path: "调研: AI 硬件市场周期 (2026-07-31)"
    agent: librarian
    summarized: true
  - path: "调研: 光模块技术路线图 (2026-07-31)"
    agent: librarian
    summarized: true
  - path: "调研: 产业链公司定位 (2026-07-31)"
    agent: librarian
    summarized: true
---
# 光模块

> 动态分析文档。稳定结构知识（产业链分层/技术路线/BOM）见 README.md。

## 全景概要

光模块处于 **AI 硬件 capex 周期的"capex 消化期"早期**。2026 年 capex 仍在加速（Big4 ~$725B，+77%），但市场已出现第一批转弱信号（Meta 卖 GPU、FCF 崩塌）。光模块因配比↑+速率叠加↑+EML 缺货↑，是链条中最"后衰减"的一环。

## 各维度分析

### AI 硬件周期位置（2026-07）

- **capex**：Amazon ~$200B、Microsoft ~$190B、Alphabet $195-205B、Meta $125-145B；75% 为 AI 相关
- **转弱信号**（2026 Q2-Q3）：Meta 成 GPU 净卖家、Alphabet 上调 capex 反跌 7%、Amazon FCF -95% QoQ、xAI Colossus 利用率仅 11%
- **判断**：稀缺周期 → capex 消化周期；风险窗口 2027-2028（折旧 ~$40B vs 收入 $15-20B）

### 供需格局（2026）

- **800G**：2026 出货 33-49M 只（估算口径不一），2026-27 量高峰
- **1.6T**：2026 量产元年（10-18M 只），**短缺 ~30%**；NVIDIA 占需求 >80%
- **EML 激光器**：供给缺口 ~30% 至 2027；Lumentum 唯一量产 200G/lane
- **光纤**：2026 新瓶颈，G.652.D 价格一年 ~5x（15.5→82 元/芯公里）

### 竞争格局

- **模块层**：旭创 #1（1.6T 份额 50%+）、新易盛 #2（Amazon 主供+LPO 领先）、Coherent、华工正源、光迅
- **芯片层**：Broadcom/Marvell DSP 双寡头；Lumentum/Coherent/Mitsubishi/Sumitomo EML
- **新变量**：NVIDIA 投资 $2B×2 于 Lumentum/Coherent + $2B Marvell 锁定产能

## 预测时间线

| 时间窗 | 预测 | 置信度 | 提出者 | 提出日期 | 验证 |
|--------|------|--------|--------|----------|------|
| 短期(2026H2) | 1.6T 量产爬坡，短缺维持 | 7/10 | Lead | 2026-08-01 | 待验证 |
| 中期(2027) | 800G 见顶 + 1.6T 放量交汇，市场 3×2025 | 6/10 | Lead | 2026-08-01 | 待验证 |
| 长期(2028+) | CPO 规模爬坡，Feynman 光需求跳增 | 5/10 | Lead | 2026-08-01 | 待验证 |

## 分歧地图

| 维度 | 观点 A | 观点 B | 分歧根因 | 状态 |
|------|--------|--------|---------|------|
| CPO 放量时点 | 2026 已量产爬坡（TrendForce） | 推迟至 2028-29（SemiAnalysis） | 良率/先进封装瓶颈判断不同 | ⚡未解决 |
| 1.6T 供需缺口 | 2027 仍短缺 30%（Jefferies） | 2026 底 EML 缓解（LightCounting） | EML 扩产节奏假设不同 | ⚡未解决 |
| 3.2T 技术路线 | EML 回归主导（Jefferies） | SiPh 延续（400G/lane 新平台） | 对 SiPh 调制频率上限的评估差异 | ⚡未解决 |

## 更新日志

| 日期 | 操作者 | 变更摘要 |
|------|--------|---------|
| 2026-08-01 | Lead | 基于 4 路调研初始化：产业链、技术路线、周期定位、供需 |
| 2026-07-29 | 人类 | 创建 theme 骨架 |

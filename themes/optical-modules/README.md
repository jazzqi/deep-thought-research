---
slug: optical-modules
lead_agent: tech_generalist
depends_on:
  - semiconductor
  - global-macro
---
# 光模块

> **⚠️ 重要提示：本文档的初始版本是基于大语言模型的历史数据创建。Agent 应根据最新信息持续更新。**

## 范围

AI 驱动的高速光模块需求：800G→1.6T→3.2T 升级周期、EML/SiPh/LPO/CPO 技术路线竞争、上下游产业链格局。

## 产业链分层（稳定结构）

```
上游芯片层（利润集中地，稀缺）         中游组装层（量大利薄）          下游客户
──────────────────────────           ──────────────────────        ──────────
EML/InP 激光器（<5 家）               模块厂（中国 7/10 席）           Hyperscalers
  Lumentum / Coherent /               旭创 / 新易盛 / 华工正源         (MSFT/META/GOOG/
  Mitsubishi / Sumitomo /             光迅 / AAOI / Molex             AMZN/ORCL/xAI)
  Broadcom                           代工（Fabrinet 泰国产能）
DSP 双寡头（~30% BOM）
  Broadcom ~68%毛利 / Marvell ~59%
SiPh 代工
  TSMC COUPE / GlobalFoundries /
  Tower / Intel
光纤（2026 新瓶颈）
  Corning / YOFC / 亨通
```

**核心判断**：超额利润集中在 <5 家的 EML 激光器和 Broadcom/Marvell DSP 双寡头。中国占 800G 出货 >80% 但芯片几乎全进口——"组装强国、芯片沙漠"。模块厂毛利（27-48%）是短缺周期现象，本质是"零件成本+组装+margin"模式，竞争加剧即压缩。

## 技术演进路线图（稳定结构）

```
800G（EML 主导）→ 1.6T（SiPh 主导 ~60-70%）→ 3.2T（EML 回归? 400G/lane）
  2024-2027          2026 量产、短缺 ~30%       样品 2026Q4 → 2029-30 放量
  "workhorse"        2027 放量 ~55M 只
```

- **架构分层**：可插拔（scale-out，2030 TAM ~$25B）vs CPO（scale-up，~$5B）——共存不替代
- **LPO**：800G 基本失败；1.6T 让位 LRO（保留 TX DSP 的中间路线）
- **关键转换点**：NVIDIA Blackwell 强制 1.6T；Rubin Ultra（2027H2）scale-up CPO；Feynman（2028H2）机架内 CPO

## 光模块 BOM 成本分布（800G EML，估算）

| 组件 | 占比 | 供应商 |
|------|------|--------|
| 光芯片（8×EML+8×PD） | ~37% | Lumentum ~70%、Coherent ~25% |
| DSP | ~28% | Broadcom ~80%、Marvell ~15% |
| 驱动/TIA/PCB/封装/测试 | ~35% | 分散 |

SiPh 方案整体便宜 ~20-25%（光源 CW ~$30 vs 8 颗 EML ~$88）。封装/测试占 SiPh 制造成本 70-80%。

## 护城河本质

1. **EML 激光器**：InP 外延 + 量子阱设计 + 良率（InP 晶圆良率仅 15-50%）；Lumentum 唯一量产 200G/lane
2. **DSP**：高速 ADC/DAC + 先进制程（3nm）+ 光电协同设计；无国产替代
3. **认证周期**：12-24 个月、单平台认证、≤3 家供应商——护城河 = 时间
4. **封装良率**：0.5µm 对准精度；85% vs 87-90% 良率差距 = 毛利差距

## 分析框架

- **AI 集群带宽需求** — 每 GPU 光模块配比（H100 1:3 → B300 1:4.5 → ASIC 1:8）、集群规模
- **周期定位** — AI 硬件 capex 周期（2026-07 处于"capex 消化期"早期，见 index.md 动态内容）
- **供需缺口** — EML 缺货 ~30%、1.6T 短缺、光纤 2026 新瓶颈
- **技术迁移** — 800G→1.6T→3.2T 节奏和 ASP 曲线
- **竞争格局** — 上游芯片 vs 中游组装；中国 vs 美国；垂直整合 vs 纯组装

## 典型参与 Agent

- tech_generalist（技术路线与供应链）
- ai_specialist（AI 集群架构演进）

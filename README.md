# deep-thought-research

[Deep Thought](https://github.com/qfei/deep-thought) 项目中 AI 智能体产出的研究报告仓库。所有报告由多个专家型智能体（Agent Personas）自动生成、交叉验证，并由 CIO 智能体综合研判后归档于此。

## 目录结构

```
deep-thought-research/
├── macro/                  # 宏观经济分析
│   ├── dalio/              # 桥水达利欧范式 — 宏观周期/债务周期分析
│   ├── soros/              # 索罗斯范式 — 反身性/宏观叙事分析
│   └── zhou_jintao/        # 周金涛范式 — 康波周期/大类资产配置
├── sentimental/            # 市场情绪分析
│   ├── kahneman/           # 卡尼曼范式 — 行为金融/认知偏误检测
│   └── shiller/            # 席勒范式 — 非理性繁荣/极端信号检测
├── sector/                 # 行业/赛道分析
│   ├── tech_generalist/    # 科技行业全景扫描
│   └── ai_specialist/      # AI 赛道专项深度扫描
├── fundamental/            # 基本面分析
│   └── buffett/            # 巴菲特范式 — 尾部风险/安全边际评估
├── portfolio/              # 投资组合综合研判
│   └── cio/                # CIO 综合 — 多源信号聚合与决策建议
├── advisory/               # 投资顾问
│   └── munger/             # 芒格范式 — 多元思维模型/逆向思考（预留）
├── foresight/              # 前瞻研究
│   ├── karpathy/           # Karpathy 范式 — AI 技术趋势（预留）
│   └── kevin_kelly/        # KK 范式 — 长期技术预言（预留）
├── risk_management/        # 风险管理
│   └── taleb/              # 塔勒布范式 — 黑天鹅/反脆弱（预留）
├── .research_index/        # 报告索引（自动维护）
│   └── RESEARCH_MANIFEST.yaml
└── README.md
```

## 报告规范

每篇报告为 Markdown 文件，命名格式：`YYYY-MM-DD-{slug}.md`，包含 YAML frontmatter 元数据：

```yaml
---
agent:        # 生成智能体代号（dalio / soros / kahneman / cio 等）
type:         # 报告类型（scan / analysis / deep_dive / report）
topic:        # 主题
status:       # 状态（final / draft）
signal:       # 核心信号判定
confidence:   # 置信度（0-1）
time_horizon: # 时间跨度
tags:         # 标签列表
collaborators: # 协作智能体列表
references:   # 参考来源
invalidation: # 观点失效条件
---
```

### 报告类型

| 类型 | 说明 |
|------|------|
| `scan` | 快速扫描 — 对当前市场/行业的快速信号检测 |
| `analysis` | 单视角分析 — 某个智能体基于自身范式的深度分析 |
| `deep_dive` | 深度研究 — 对特定问题的详细推演与论证 |
| `report` | 综合报告 — 多源聚合后的研判结论（通常由 CIO 产出） |

### 智能体范式

| 智能体 | 对应思想家 | 核心框架 |
|--------|-----------|---------|
| `dalio` | Ray Dalio | 债务周期 / 宏观周期定位 |
| `soros` | George Soros | 反身性理论 / 叙事经济学 |
| `zhou_jintao` | 周金涛 | 康波周期 / 资产配置 |
| `kahneman` | Daniel Kahneman | 行为金融 / 认知偏误 |
| `shiller` | Robert Shiller | 非理性繁荣 / 情绪极端值 |
| `buffett` | Warren Buffett | 安全边际 / 尾部风险 |
| `cio` | — | 综合研判 / 多源信号融合 |
| `munger` | Charlie Munger | 多元思维模型 / 逆向思考 |
| `karpathy` | Andrej Karpathy | AI 技术趋势判断 |
| `kevin_kelly` | Kevin Kelly | 长期技术预言 |
| `taleb` | Nassim Taleb | 反脆弱 / 黑天鹅 |

## 工作流

1. `scan` 智能体并行扫描市场，产出快速信号
2. `analysis` / `deep_dive` 智能体按主题深入分析
3. `cio` 聚合多源信号，产出综合研判报告
4. 所有报告自动注册到 `.research_index/RESEARCH_MANIFEST.yaml`

## 报告示例

- **[市场情绪综合诊断：系统性悲观与多重极端信号]** — CIO 整合卡尼曼与席勒的情绪分析
- **[中国宏观场景分析：通缩型信用收缩]** — 达利欧、索罗斯、周金涛三方宏观研判
- **[Tech/AI 叙事扫描]** — AI 赛道每周叙事变化与信号检测

## 关联项目

- [deep-thought](https://github.com/qfei/deep-thought) — 核心项目，驱动智能体生成这些报告

## License

MIT

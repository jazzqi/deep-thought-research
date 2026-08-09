---
slug: market-sentiment
lead_agent: kahneman
depends_on: []
---
# 市场情绪追踪

> **⚠️ 重要提示：本文档的初始版本是基于大语言模型的历史数据创建。Agent 应根据最新信息持续更新。**

## 范围

跨资产市场情绪的温度计：跟踪 Fear&Greed、散户/机构情绪分歧、叙事热度（narrative economics）、泡沫/极端估值信号。
为其他 theme 提供情绪面背景，不覆盖单一资产的基本面分析。

## 分析框架

- **情绪极端检测** — Fear&Greed 极值、情绪-价格背离（mismatch）、恐慌/亢奋的周期性出现
- **叙事热度追踪** — 哪些叙事在升温/降温（Narrative Economics 框架），叙事的传播路径与强度
- **羊群行为与泡沫信号** — 估值极端 + 情绪亢奋的组合识别，反馈循环的自我强化阶段
- **行为偏差扫描** — 损失厌恶、锚定、FOMO 的系统性出现，识别市场参与者的集体认知偏差

## 典型参与 Agent

- kahneman — 认知偏差与羊群行为分析
- shiller — 叙事经济学与泡沫检测
- crypto_trader — crypto 市场 FOMO/清算情绪（与 crypto 主题联动）

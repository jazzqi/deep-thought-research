---
slug: podcast-digest
lead_agent: tech_generalist
depends_on:
  - ai-industry
  - market-daily
---
# 播客/访谈学习文档（Podcast Digest）

> 把已抓取的 podcast / YouTube 长视频（访谈）转录稿蒸馏为中文学习文档。
> 数据同源：raw_items `content_type='podcast'` 的 `transcript` 字段
> （D96：youtube_caption / happyscribe_podcast 采集器写入）。

## 范围

英文访谈类长内容（投资、科技、宏观、时事），面向作者本人与团队成员的二次学习——
蒸馏浓缩、金字塔结构、保留关键细节，非投资建议。

## 分析框架（学习文档结构，唯一真源 = template.md）

- **总览**（2-3 段引用块）— 核心论点链 + 最有价值洞察，1 分钟掌握全集脉络
- **TL;DR**（3-5 条）— 每条一句话结论
- **核心论点**（3-5 个，金字塔）— 结论 → 论据 → 理解（演绎解释，必要时适当）
- **关键细节** — 数字/时间线/人名/观点交锋/反共识（可溯源，保留精度）
- **Key Takeaways（核心精华）** — 每条一句可直接带走并影响判断的认知

## 频道固定分工（D96 §6，不预筛）

| source 前缀 | 内容定位 | Lead/写手 |
|---|---|---|
| `youtube:@ILTB_Podcast` | 投资/商业访谈 | tech_generalist |
| `happyscribe:all-in*` | 科技+宏观圆桌 | tech_generalist |
| `happyscribe:the-daily` | 时事/政策/社会 | **ackman（统揽全局）** |

## 写作铁律

- 金字塔原理（硬约束）：结论先行，禁止「本集讨论了…」式开场白
- 避免转述式刻意口吻：直接叙事，禁止「主持人问道…嘉宾回答说…」
- 中文为主，信达优先：禁止生造词；仅保留必要术语英文，不保留金句原文+翻译
- 演绎解释：必要时适当、不冗余（1-2 句，删掉能理解就删）
- 长度：转录稿每 10KB ≈ 350-400 字中文，仅为推荐值非硬限制
- 溯源：数字/事实必须来自转录稿，禁止虚构

## 典型参与 Agent

- tech_generalist（Lead，科技/投资全景判断）
- ai_specialist（AI 产业深度）
- kevin_kelly（前瞻扫描）
- soros（宏观）
- karpathy（技术趋势）
- geopolitics_agent（地缘时事）
- buffett（基本面价值）
- kahneman（行为金融）

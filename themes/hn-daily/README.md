---
slug: hn-daily
lead_agent: tech_generalist
depends_on:
  - ai-industry
  - disruptive-innovation
  - market-daily
---
# HN 书摘 · 每日扫描快报

> 每天从 Hacker News 汇总高价值帖子，以"社区书摘"形态呈现——摘文章、批注价值、摘录评论。
> 数据同源：raw_items `source='hackernews'`（D88 v3：hnrss `?points=60`，metadata 带 hn_points/hn_comments）。

## 范围

科技行业每日扫描：AI 模型与基础设施、开发者工具生态、开源项目、创业与融资、技术评论与社区讨论。

## 分析框架（5 栏目）

- **头条深读（1-2 条）** — 今天最值得花 5 分钟的一篇：摘要 + 为什么值得读批注 + 评论风味
- **值得一读（4-6 条）** — 扫一眼不亏：标题 + 一句话摘要 + 元数据
- **技术雷达（2-3 条）** — 新工具 / 新库 / 新论文 / Show HN
- **社区之声（1-2 条）** — Ask HN 好问题 + 高赞回答摘要
- **数据速览** — 当日 Top10 纯榜单快照（供补漏）

## 选帖标准（两级筛选）

1. **机械初筛**：raw_items `source='hackernews'`，UTC 日窗口，`metadata.hn_points ≥ 60`，同 URL 去重，跨天去重（对 index.md 往期标题比对）
2. **LLM 精筛**（四维打分 1-5）：信息密度 / 一手性 / 讨论深度 / 行业相关性；≥4 入选、3 分递补、<3 淘汰；每日 8-12 条

## 质量铁律

- 摘要必须基于实际抓取正文（raw_items.full_text 优先，缺失用 fetch_url 抓原文），抓不到标注"未能抓取"不虚构
- 标题格式：英文原文 + 中文翻译副标题（无域名后缀）；摘要/批注直奔主题，禁"标题宣布"类开场白
- 每条带原文链接可追溯（原文 + 评论）
- 禁止 session 目录名 / internal / manual 等内部元数据出现在正文
- emoji 克制；数字带单位/时间/口径

## 典型参与 Agent

- tech_generalist（Lead，科技全景判断）
- tech_scout（早期技术信号、开发者生态）
- ai_specialist（AI 产业深度）
- kevin_kelly（前瞻扫描）

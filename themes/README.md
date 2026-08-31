# themes — 主题索引与 Lead 映射

> 本目录是 Deep Thought 主题文档工厂（D71）的内容真源。
> 每个主题 = `{slug}/README.md`（启动文档）+ `index.md`（定版）+ `_history/`（工作现场）。
> 本文件维护 **主题 ↔ Lead Agent ↔ 参与团队** 的映射关系（D71 Batch 4 #17 Lead 挑选机制）。

## 组织架构（部门负责人 = 各主题 Lead 候选）

| 部门 (org_path) | Head of Dept | 职级 | 成员 |
|---|---|---|---|
| research/macro | soros | Principal | zhou_jintao, dalio, nick_timiraos |
| research/fundamental | buffett | Principal | lynch |
| research/sentimental | kahneman | Principal | shiller |
| research/sector | tech_generalist | Principal | ai_specialist, software_analyst, silicon_analyst, tech_scout |
| research/foresight | kevin_kelly | Principal | karpathy |
| research/crypto | crypto_trader | Principal | — |
| research/geopolitics | geopolitics_agent | Principal | — |
| risk_management | taleb | Principal | —（风控审查，不 Lead 主题） |
| executive | ackman | Managing Director | —（跨资产综合） |

## 主题 ↔ Lead 映射表

| 主题 | Lead | 参与团队 | 主题类型 | 依赖上游 |
|---|---|---|---|---|
| nvda | tech_generalist | sector + fundamental + market-daily | 个股/行业 | semiconductor, global-macro |
| semiconductor | tech_generalist | sector + macro + risk | 行业 | global-macro, geo-conflicts |
| optical-modules | tech_generalist | sector + macro | 行业 | semiconductor, global-macro |
| alphabet | tech_generalist | sector + fundamental | 个股/行业 | global-macro, market-daily |
| tesla | tech_generalist | sector + foresight | 个股/行业 | global-macro, market-daily |
| spacex | tech_generalist | sector + foresight | 个股/行业（硬科技） | — |
| disruptive-innovation | kevin_kelly | foresight + sector | 前瞻/扫描 | — |
| ten-bagger-hunting | kevin_kelly | foresight + fundamental + sector | 前瞻/策略扫描 | disruptive-innovation |
| fed | soros | macro + market-daily | 宏观政策 | — |
| global-macro | soros | macro | 宏观 | — |
| energy | soros | macro + geopolitics + market-daily | 宏观/商品 | global-macro, geo-conflicts |
| pdd | buffett | fundamental + macro | 个股 | china-internet, global-macro |
| china-internet | buffett | fundamental + macro | 行业 | global-macro, market-sentiment |
| pig-cycle | buffett | fundamental + macro | 周期 | global-macro |
| btc | crypto_trader | crypto + macro + sector | 加密资产 | global-macro, market-sentiment |
| cryptocurrency | crypto_trader | crypto + sector + macro | 加密行业 | global-macro, market-sentiment |
| market-daily | ackman | executive + sentimental + sector + macro | 综合/每日 | — |
| qqq | ackman | executive + sector + sentimental | 指数 | global-macro, market-daily, semiconductor |
| market-sentiment | kahneman | sentimental + crypto | 情绪面 | — |
| geo-conflicts | geopolitics_agent | geopolitics_agent + risk(taleb 审查) + macro + sentimental + crypto | 地缘/黑天鹅/避险 | — |
| economic-calendar | ackman | executive + macro + fundamental + sector + risk | 宏观/日历预读 | market-daily, fed, global-macro |
| ai-industry | ai_specialist | sector + fundamental + foresight | 行业 | semiconductor, nvda, alphabet, global-macro, market-sentiment, disruptive-innovation |
| biopharma | pharma_specialist | sector + fundamental + macro + risk + advisory | 行业 | global-macro, disruptive-innovation |
| ai-second-order | kevin_kelly | foresight + sector + fundamental + macro | 前瞻/衍生机会 | ai-industry, disruptive-innovation, ten-bagger-hunting, semiconductor, global-macro, market-sentiment |
| brk | buffett | fundamental + macro + sentimental + risk(taleb 审查) | 人物情报/机会发现（跟风标的） | global-macro, market-daily, market-sentiment |
| justin-sun | crypto_trader | crypto + sentimental + macro + geopolitics + risk(taleb 审查) | 人物情报/资金动向 | cryptocurrency, btc, global-macro, market-sentiment, geo-conflicts |
| hn-daily | tech_generalist | sector + foresight | 综合/每日扫描（人读书摘） | ai-industry, disruptive-innovation, market-daily |
| podcast-digest | tech_generalist | sector + foresight + macro + fundamental | 播客/访谈学习文档（人读二次学习） | ai-industry, market-daily |
| el-nino-2026-27 | ackman | executive + macro + fundamental + sector + risk + sentimental | 跨资产追踪（1+4+Q） | global-macro, market-daily, energy, geo-conflicts |

## 数据蒸馏机制（DISTILLATION）

> 完整协议见 **[DISTILLATION.md](DISTILLATION.md)**（kickstarter，Agent 自发维护，不强制）。

主题之间采用**倒金字塔式数据蒸馏**：上游（L1 宏观/全球）先发布已核验结论，
下游（L2 行业/资产 → L3 个股/指数）通过 `depends_on` 声明依赖，引用上游 `index.md`
的结论，避免重复查询原始数据（实例：qqq 因缺上游宏观/估值结论，一轮耗时 19 分钟 vs
正常 11 分钟）。

- 上表「依赖上游」列 = 各主题 `README.md` frontmatter 的 `depends_on`（建议字段，Agent 维护）
- `depends_on` 引用的 slug 必须存在于 `themes/` 目录 / REGISTRY.yaml
- 下游 roundtable/relay 时，Lead 优先用 ReadThemeDocsTool 读取依赖上游的 `index.md`
- REGISTRY.yaml 的 `related_themes` 与 `depends_on` 双向保持一致

## Lead 挑选规则（D71 Batch 4 #17）

1. **显式声明优先**：`{slug}/README.md` frontmatter 的 `lead_agent` 字段（人类维护，文档为真源）
2. **职级校验**：lead_agent 必须是 agents 表中存在的 agent，且 `job_position = Head of Dept`（或 Principal）——校验失败告警并 fallback
3. **无命中处理**：README 标题加 `⚠️`（如 `# ⚠️ 未分配`），flow 触发时跳过执行 + 日志告警，不静默 fallback
4. **跨部门协作**：lead 单一（主责部门），participants 可跨部门（见上表"参与团队"列）

## 无命中（unassigned）主题

| 主题 | 原因 | 处理 |
|---|---|---|
| （当前无） | — | — |

> 若某主题无法匹配 Lead，在此登记并同步在 README 标题加 ⚠️。

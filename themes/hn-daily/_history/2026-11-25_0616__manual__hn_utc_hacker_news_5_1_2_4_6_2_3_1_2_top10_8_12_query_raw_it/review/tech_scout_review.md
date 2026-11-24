## 审查结论（tech_scout / 早期技术信号视角）

已独立核验：`ReadThemeDocsTool` 读完 `drafts/current.md` 全文（15560 chars，分段读完）与 `reference.md`、`discussion_log.md`；`query_raw_items(source=hackernews, published_after=2026-11-24T00:00:00Z, limit=50)` 独立拉取当日 HN 池；另用 `keyword="Show HN"` 补查。未仅对照 reference.md。

### 🚫 blocker

- **技术雷达漏掉明确的早期技术信号（Show HN/新库/新模型权重），与栏目定位不符。** 当前“技术雷达”仅 3 条（unkernel、VP≠VNP、GreyNoise），但同日 HN 池里有多条 tech_scout 应覆盖的导入期信号，且部分已在 discussion_log 被提及却未进正文：
  - `[id:817761]` **Ternary Bonsai 2.5 27B**（▲65/💬12，`prismml.com`）——三值量化 27B 权重发布，低比特量化从论文走向可用权重的 S 曲线导入期信号。Big Picture 只一句“Bonsai 等增量工程”带过，无摘要、无链接、无溯源。
  - `[id:817552]` **Show HN: Mason**（▲33/💬3，`masondata.ai`）——DuckDB 列存驱动的 Postgres 读副本替代，开发者基础设施/OLAP-OLTP 边界信号。
  - `[id:817861]` **Launch HN: Versine (YC F26)**（▲34/💬15）——MCP 收发款，MCP 协议向垂直支付场景裂变的早期产品信号。
  - `[id:817313]` **Songe**（▲39/💬4，`github.com/sous-labs/songe`）——利用闲置算力训练本地模型，AI 下沉/本地训练生态信号。
  - `[id:817749]` **Compiling web applications into verified operations for AI agents**（▲29/💬8，`protocolis.co/paper/`）——Web→agent 可验证操作，kevin_kelly 在讨论中点名，但正文完全缺席。
  
  这些不是“可有可无的尾巴”，而是本栏目“新工具/新库/新论文/Show HN”的核心覆盖对象。建议至少将 Bonsai + 1-2 个 Show HN/agent-infra 条目补入技术雷达，每条给出原文链接、HN 热度、真实摘要、S 曲线/置信度标注。

- **draft 文件存在明显重复/拼接损坏片段，发布前必须清理。** 全文读到 `offset=12000` 时，该段开头为 `list 视角：** 这条信号的战略价值...`，随后重复了条目 9/10/11、共识、数据速览占位符，与前文已出现内容重叠。虽然尾部结构看似完整，但文档中存在乱码/重复块会破坏可读性与下游渲染/引用定位。需通读去重，确认每个条目只出现一次，段落边界完整。

### ⚠️ concern

- **AI infra / 开发者生态方向被低估，缺少“能力变便宜后的基础设施经济学”条目。** `[id:816379]` *Jevons Paradox in AI: Cheaper Tokens Won't Pay for Capex*（▲77/💬37）在讨论记录和共识背景里被反复引用，但正文没有独立条目。它直接关系 AI infra capex 回收、token 价格战与算力投资逻辑，是开发者/infra 读者的关键判断变量。建议补一条短卡片，明确“方向性信号、非财务结论”，并标注置信度。

- **“未能抓取评论”表述过于笼统，削弱溯源可信度。** 条目 3/4/5/6/7/9/10 多处写“未能抓取评论”。部分条目在 HN 有高评论量（如 #3 ▲456/💬263、#5 ▲148/💬105），完全不摘评论会让读者无法判断社区分歧。至少应区分“未抓取正文评论”与“HN 讨论未抽样”，或补 1 条代表性 HN 评论链接/摘要；无法核验时明确“基于原文+HN 元数据，未纳入评论证据”。

- **reference.md 可追溯性差，存在重复拼接。** `reference.md` 有三段重复/重叠记录（同一批 id 多次出现，格式不统一），且部分条目缺少关键参数或混入“本轮 query_raw_items 未返回该 id，数字沿用稿内标注”这类弱溯源说明。作为审查依据文件，这会增加后续 fact-check 成本。建议按“数据点: 工具(参数)[id:N] = 值”统一去重；对未在本轮查询返回的 id（如 draft 引用的 817875 在我首轮返回中可见，但 reference 备注自相矛盾）重新核对。

- **热度口径存在快照漂移风险，需在文内显式锁定口径。** discussion_log 已指出 `query_raw_items` 头部 ▲/💬 与 summary `Points/Comments` 可能不一致。draft 正文统一用了头部数字（我抽查与当前 query_raw_items 头部一致），这是可接受的，但应在“数据速览/方法说明”处写明“热度取 query_raw_items 返回时的 ▲/💬 快照，非实时最终值”。否则读者对照 HN 页面会看到漂移。

- **条目 6（Anthropic Working with AI）样本偏差提示够，但“增量产出”被多处复用为共识基座。** 共识 3 已标注样本自选，但 Big Picture 与多视角仍把它当作较强支撑。建议在 Big Picture 第三层加一句“该结论来自 Anthropic 自选客户访谈，外推需谨慎”，避免从“方向性证据”滑成“行业事实”。

### 🔧 nit

- **中文表达整体自然，格式克制，符合要求。** 无 emoji 堆砌，表格/分节清晰；“Big Picture / 共识 / 少数派”结构可读性好。
- **个别措辞可更审慎。** 如“多数企业反而减少招聘与离岸外包”建议改为“调研样本中，多数企业报告减少招聘或削减离岸外包”，避免把样本结论写成普遍事实。
- **“数据速览”占位符可加一句生成说明。** 当前仅“本节由代码从冻结快照注入 Top10，此处不手写”——可补充“若注入失败，应回退为手写 Top10 并标注快照时间”，防止发布空节。

### ✅ pass

- **独立核验意识到位。** draft 对 Bloomberg/Reuters/MSN 付费墙未抓取正文做了诚实标注（“具体跌幅与收盘价未核验”），没有编造收盘价。
- **核心高热度条目溯源基本完整。** 我抽查条目 1-11 的原文链接、HN id、热度数字与 `query_raw_items` 返回一致；关键事实（Polymarket 钱包/时间/金额、Tidal 43%/96%/8-8.5万、unkernel 2-32x、VP≠VNP Lean 形式化、GreyNoise 99 IP/22 org/CVE）均有对应来源条目或正文摘录。
- **信号过滤框架执行较好。** 对 Tegmark 标题失真、VP≠VNP“可核验≠已验收”、GreyNoise“LLM 驱动”为推断、Working with AI 样本偏差，都做了降权/置信度标注，符合 tech_scout 的噪声过滤原则。
- **少数派保留得当。** kevin_kelly 的长周期萌芽视角被保留且未与短期共识混淆，符合“高分≠高 foresight 价值”的校准。

**审查总结：** 主线叙事和溯源纪律总体扎实，但作为 tech_scout 审查，我不能放过“技术雷达缺失 Show HN/新工具/新库/早期 infra 信号”这一结构性遗漏，以及 draft 中的重复拼接损坏。修完这两个 blocker 后，文档质量可以达到发布线。
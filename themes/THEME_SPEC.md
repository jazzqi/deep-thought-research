# Theme 系统设计规范

> 投资主题（Themes）是 Deep Thought 系统主动跟踪的核心关注单元。
> 每个 Theme 是一个**不断演进的 Big Picture**，由多个 Agent 协作维护。

---

## 一、背景与动机

### Theme 的定位

Theme 是：

- **投资主题**——系统主动跟踪的若干个投资方向（几个到数十个，有进有出，可能分裂或合并）
- **跨学科 Agent 的聚合单元**——来自不同维度的多个 Agent 的研究产出最终汇聚到 Theme
- **不断演进的 Big Picture**——不是一次性报告，是活着的文档，不断追踪预测现实世界
- **起承转合 - 上下游协作的关键中间产物**——Agent 从多个信息源获取最新消息，形成多视角观点，由 Lead Agent 组织整理成 Theme，后续给到下游 Agent 作为投资决策依据

### Theme 生态：交叉、派生、影响

Theme 不是孤立存在的。它们之间天然存在复杂关系网络：

| 关系 | 说明 | 例子 |
|------|------|------|
| **交叉** | 同一件事影响多个 theme，Agent 跨 theme 取信息 | 美联储加息同时影响 fed、qqq、global-macro、btc |
| **派生** | 一个 theme 裂变出更具体的子 theme | cryptocurrency → btc |
| **包含** | 一个 theme 是另一个的子集 | semiconductor 包含 nvda |
| **合并** | 两个 theme 融合成一个 | 未来可能发生 |
| **新增** | 跟踪新的投资方向 | market-daily（市场全景） |
| **消亡** | 主题不再值得跟踪 | archived 状态 |

**Agent 的工作方式不是"各扫门前雪"。** 每个 Agent 阅读多个 theme 的文档，从中获取上下文，再通过自己的 theme 影响其他 theme。例如：

- tech_generalist 在写 `nvda` 的报告时，先读 `semiconductor`、`market-daily` 和 `fed` 的最新动态
- 自己的产出反过来被 `disruptive-innovation` 和 `ten-bagger-hunting` 引用
- 形成"互相引用、互相影响"的研究生态

这与现实世界的投资研究部门运作方式一致——行业研究员读宏观报告，宏观分析师看行业数据，基金经理综合所有输入做决策。

---

## 二、文件结构

```
deep-thought-research/
├── themes/                              ← 投资主题目录
│   ├── THEME_SPEC.md                    ← 本规范文件
│   ├── REGISTRY.yaml                    ← 主题索引（tags、assets、关联关系）
│   ├── nvda/                            ← 每个 theme 一个目录
│   │   ├── README.md                    ← 启动文档：scope、核心问题、数据源
│   │   ├── index.md                     ← 定版：当前分析（共识+分歧+预测）
│   │   ├── log.md                       ← 变更记录
│   │   └── _history/                    ← 工作现场：Agent 协作产物，自动生成
│   │       └── YYYY-MM-DD_HHMM__{trigger}__{brief}/
│   │           ├── roundtable/          ← Phase 1 产出
│   │           │   ├── scratchpad.md
│   │           │   └── discussion_log.md
│   │           ├── drafts/              ← Phase 2 产出
│   │           ├── review/              ← Phase 3 产出
│   │           └── publish_candidate/   ← 定版前的最终版本
│   │               ├── README.md
│   │               └── index.md
│   ├── pdd/
│   │   └── index.md
│   ├── fed/
│   │   └── index.md
│   ├── semiconductor/
│   │   └── index.md
│   └── ...                              ← 其他 theme
├── macro/                               ← 已有，不变
├── sector/                              ← 已有，不变
├── sentimental/                         ← 已有，不变
├── portfolio/                           ← 已有，不变
└── ...
```

### Theme 目录命名规范

- 使用英文 kebab-case：`nvda`、`semiconductor`、`pdd`
- 每个 theme 一个目录
- 目录名 = theme 的唯一标识符（slug）

### Theme 列表（动态维护）

Theme 列表由 Lead Agent 或人类手动管理。缺少索引文件时，以 `themes/` 下的一级子目录为准。

建议在 `themes/` 根目录维护一个 `REGISTRY.yaml` 记录所有活跃 theme：

```yaml
themes:
  - slug: nvda
    name: NVIDIA（AI 芯片龙头）
    status: active           # active / monitoring / archived
    priority: 1
    created: 2026-07-29
  - slug: pdd
    name: PDD Holdings（拼多多）
    status: active
    priority: 2
    created: 2026-07-29
```

---

## 三、index.md 文档规范

### 3.1 YAML Frontmatter

> **Tags 唯一来源是 `REGISTRY.yaml`**，index.md frontmatter 不复读 tags/priority/assets/related_themes。
> 查询 theme 的 tags 统一读 REGISTRY.yaml。

```yaml
---
name: NVDA                              # 主题名称
slug: nvda                               # 目录名（唯一标识）
status: active                           # active / monitoring / archived
lead: synthesis_agent                    # 当前 Lead Agent
created: 2026-07-29                      # 创建日期
updated: 2026-07-29T10:00:00+08:00       # 最后更新
sources:                                 # 本次更新引用的来源报告
  - path: sector/ai_specialist/2026-07-29-xxx.md
    agent: ai_specialist
    summarized: true
  - path: fundamental/buffett/2026-07-28-xxx.md
    agent: buffett
    summarized: true
---                                # 不复读 tags/assets/related_themes
```

### 3.2 正文结构

> **v2：以 `themes/{slug}/index.md` 的 seed 格式为权威（Big Picture/各维度分析/分歧地图）。**
> 旧版「全景概要 / 正文分析 / 分歧汇总」结构已废弃，不再使用。

```markdown
## Big Picture

Lead Agent 的综合判断。突出主要驱动力，不忽视次要因素。
> 每次更新时重写此节，保持最新。

> **D74 语义修正：Big Picture 是主题的宏大叙事（grand narrative），不是宏观经济。**
> 写"这家公司/标的是谁、核心业务与商业模型、整体商业叙事与愿景、当前核心矛盾与发展脉络"——
> 是理解一切财务与估值数字的总纲。relay 阶段 agent 在稿首写 `## Big Picture` 节，
> publish 优先提取该节（有则替换 root），无则保留 root，再无则综合前几段。

## 各维度分析

Lead 执笔，按主题自然展开。共识为先，分歧内联标注。

### 叙事/情绪面

（叙事与情绪面：市场情绪、叙事强度、舆情变化）

### 基本面

（基本面：财务、供需、竞争格局等硬数据）

### 宏观背景

（宏观背景：利率、政策、流动性等外部环境）

## 预测时间线

| 时间窗 | 预测 | 置信度 | 提出者 | 提出日期 | 验证 |
|--------|------|--------|--------|----------|------|
| 短期(1-4w) | ... | 7/10 | Soros | 2026-07-29 | 待验证 |
| 中期(1-3m) | ... | 5/10 | Buffett | 2026-07-30 | 待验证 |
| 长期(6m+) | ... | 6/10 | Lead | 2026-08-01 | 待验证 |

> 预测只追加不修改。

## 分歧地图

| 维度 | 观点 A | 观点 B | 分歧根因 |
|------|--------|--------|---------|
| 估值 | 基本面强劲 | Buffett:估值偏高 | 增长持续性假设不同 |
| 入场时机 | 长期看好 | Buffett:等回调 | 风险偏好差异 |

## 重大事件与深度报告

> **D74 新增：深度事件正文独立成文**于 `themes/{slug}/reports/{slug}.md`，
> index 本节约 1 行链接 + 结论摘要 + 目录索引注释。
> 无事件时整节约略（不破坏 seed 结构）。

1. [欧盟监管风暴（2026-08-01）](reports/event-1.md) — 结论摘要（≤120 字）
2. [雄安新区扩张（2026-07-31）](reports/event-2.md) — 结论摘要

## 更新日志

| 日期 | 操作者 | 变更摘要 |
|------|--------|---------|
| 2026-08-01 | Lead | 集成最新财报预期，补充估值分歧 |
```

### 3.3 深度事件独立报告（D74）

**draft 事件节契约**（relay agent 按此结构写，publish 确定性拆分）：

```markdown
## 四、近期重大事件与风险

### 4.1 欧盟监管风暴（2026-08-01）

**事件**：欧盟委员会指控 Temu 阻挠调查……[来源](url)

**Buffett 分析**：这是实质性风险……（深度正文）

### 4.2 雄安新区扩张（2026-07-31）

**事件**：…… **Buffett 分析**：……
```

- **识别**：`## ` 顶层节含"重大事件/重大新闻/近期新闻/事件分析"，其下 `### ` 子节为事件
- **拆分**：每个 `### ` 事件子节 → `themes/{slug}/reports/{slug}.md`（frontmatter + 标题 + 深度正文 + 索引注释）
- **标题 slug**：`[slug]` 标记优先（如 `### [eu-storm] 欧盟风暴`），缺省 `event-{n}`
- **index 引用**：`## 重大事件与深度报告` 节，每事件 1 行 `[标题](reports/{file}.md) — 结论摘要`
- **结论摘要**：首个 `**XX分析/解读：**` 段第一句，≤120 字（确定性提取，无 LLM）

---

### 3.4 README.md — 固定启动文档

每个 theme 目录下的 `README.md` 是**固定（不演进）的启动文档**，由对应领域的 Agent 在创建 theme 时一次性写入。内容覆盖：

| 字段 | 说明 | 示例 |
|------|------|------|
| **范围** | 该 theme 跟踪什么、不跟踪什么 | "NVIDIA 在 AI GPU 和数据中心芯片的地位" |
| **核心问题** | 驱动该 theme 的关键待答问题 | "Blackwell 需求可持续吗？" |
| **数据源** | 需要拉取什么数据 | "财报、TSMC 营收、数据中心 capex" |
| **典型参与 Agent** | 哪些分析师适合参与 | tech_generalist、buffett |
| **关联主题** | 与其他 theme 的关系 | semiconductor、qqq |

`README.md` 由 Agent 创建后不再频繁修改。仅在 theme scope 发生实质性变化时才更新。

> **⚠️ 重要提示：本文档的初始版本是基于大语言模型的历史数据创建。Agent 应根据最新信息持续更新，不要将其当作静态 ground truth。**

#### 模板

```markdown
# {Theme 名称}

> **⚠️ 重要提示：本文档的初始版本是基于大语言模型的历史数据创建。Agent 应根据最新信息持续更新。**

## 范围

{该 theme 覆盖什么、不覆盖什么。此信息几乎不变。}

## 分析框架

- {用什么 lens 分析这个主题}
- {关注什么维度的变化}
- {关键分析问题类别（非具体问题，具体问题从实时数据得出）}

## 典型参与 Agent

- {agent} — {角色说明}
- {agent} — {角色说明}
```

#### README 的职责

README 只保留 **scope + 分析框架 + 典型参与 Agent** 三项不变信息。

核心问题和数据源**不放 README**——Agent 入场时根据 scope、框架和实时数据自己形成。index.md 中的当前分析章节自然承载当前关注的问题和引用的数据。

### 3.3 核心原则

1. **共识是正文主干**——分歧内联标注，不独独立成篇
3. **预测只追加不修改**——追踪各 Agent accuracy
5. **不强行拍板**——分歧标记"未解决"即可，等新数据

---

## 四、四阶段协作流程

Theme 文档的更新遵循四个阶段，由**定时 + 事件**混合触发。

```
[定时/事件] 触发
    │
    ▼
┌────────────────────────────────────────┐
│ Phase 1: 圆桌讨论（Roundtable）         │
│  共享白板 · 群聊辩论 · 自然形成共识/分歧  │
└──────────────┬─────────────────────────┘
               │ 共识可支撑写作
               ▼
┌────────────────────────────────────────┐
│ Phase 2: 接力写作（Relay Writing）       │
│  Lead 分工 · Agent A → B → C 渐进融合   │
└──────────────┬─────────────────────────┘
               │ 初稿完成
               ▼
┌────────────────────────────────────────┐
│ Phase 3: 交叉审查（Cross Review）        │
│  身份互换 · 分级反馈 · 分歧如实标记       │
│  blocker → 返工，分歧 → 保留             │
└──────────────┬─────────────────────────┘
               │ 无 blocker
               ▼
┌────────────────────────────────────────┐
│ Phase 4: Lead 终稿                      │
│  吸收审查意见、更新分歧地图、推动 index.md │
└────────────────────────────────────────┘
```

### 4.1 触发机制

**定时 + 事件混合触发**，并非 Lead Agent 发起：

| 触发类型 | 条件 | 行为 |
|---------|------|------|
| **定时** | 每 6 小时（可配置） | 常规轮次：收集最新产出，必要时启动 Phase 1 |
| **事件** | 某 Agent 产出的内容与该 theme 强相关 | 补充轮次：Lead 判断是否值得启动新一轮 |
| **手动** | 人类在 index.md 头部设置 `request_review: true` | 立即启动一轮完整的四阶段流程 |
| **合并** | 定时轮次中检测到重要新信息 | 升级为完整四阶段，否则仅轻量更新 |

### 4.2 Phase 1：圆桌讨论

目标：在动笔前群策群力，让不同视角充分碰撞。

#### 4.2.1 共享白板（Scratchpad）

所有讨论沉淀在 `themes/<slug>/_roundtable/` 目录下，每轮一个文件：

```
themes/nvda/
├── index.md
├── _roundtable/
│   ├── 2026-08-01_session.md      ← 本轮完整讨论记录
│   └── 2026-08-01_scratchpad.md    ← Lead 整理的共识/分歧草稿
└── log.md
```

`scratchpad.md` 的格式：

```markdown
# Roundtable: 2026-08-01（第 2 轮）

## 议题
NVDA 财报前瞻——Blackwell 需求能见度

## 讨论摘要

### Agent A（技术）观点
- Blackwell 产能爬坡超预期，Q3 指引可能上调
- 但 CoWoS 封装仍是瓶颈

### Agent B（市场）观点
- 市场已 Price in 上调预期，超预期幅度决定方向
- 如果只是 inline，反而可能 sell-on-news

### Agent C（宏观）观点
- 数据中心 capex 周期仍在加速，回调即买入
- 但需关注出口管制升级风险

## 观点分布
| 维度 | 技术 | 市场 | 宏观 |
|------|------|------|------|
| 方向 | Bullish | Bullish |
| 核心变量 | Blackwell | 超预期幅度 | 数据中心capex |
| 风险 | CoWoS封装瓶颈 | 估值已price in | 出口管制 |

## 素材足以记录？✅
```
```

#### 4.2.2 圆桌流程

```
1. Lead/定时器 建立 scratchpad，设定议题
2. 各 Agent 异步或依次发表观点
   → 每个 Agent 读到其他人的观点后再迭代
3. Lead 整理：各 Agent 的观点分布、分歧维度、未覆盖的方向
4. 如有必要，Lead 发起追问/澄清（跨 2-3 轮）
5. Lead 判定：素材是否足够支撑一份忠实的多视角记录
   → 是 → 进入 Phase 2（写，如实反映分歧）
   → 否 → 继续收集或标记"素材不足"，暂缓
```

### 4.3 Phase 2：接力写作

目标：不是"各写各的合并"，而是渐进融合。

#### 4.3.1 Lead 角色：编辑/协调者

Lead **不主笔**，而是：

| 职责 | 说明 |
|------|------|
| **分派** | 决定各 Agent 负责的 section（技术写技术、市场写市场） |
| **排期** | 确定接力顺序，标注哪些 section 之间有关联 |
| **跟踪** | 确保进度，衔接上下游 |
| **质量** | 确保各 Agent 的观点被完整、忠实地记录，不被删改扭曲 |

#### 4.3.2 接力模式

```
Agent A（技术）起稿：           "Blackwell 架构的技术优势..."
        ↓ 稿子传给 B
Agent B（市场）在 A 基础上改写：  "这意味着 Blackwell 正在重塑..."
        ↓ 融合版传给 C
Agent C（宏观/合规）注入上下文：  "在全球数据中心 capex 上行周期中..."
        ↓
Lead 收到融合稿，做最终编辑
```

**关键规则：**
- Agent B 不另起炉灶，在 Agent A 的文本上直接修改
- 每步只能改自己负责的 section，不碰别人的
- 如果 B 发现 A 的假设有问题 → 在 scratchpad 记录争议，但不阻塞写作

### 4.4 Phase 3：交叉审查

目标：不是自审，而是**互换身份审**。

#### 4.4.1 审查分配

| 审查人 | 审查对象 | 视角 |
|--------|---------|------|
| 市场 Agent | 技术章节 | "非技术人员看不懂" |
| 技术 Agent | 市场章节 | "夸大其词、实现不了" |
| 宏观 Agent | 全篇 | "和宏观背景矛盾" |
| Lead | 全篇 | "各 Agent 的观点是否被忠实地呈现" |

#### 4.4.2 分级反馈

每个审查意见必须带 severity：

```
🚫 blocker  — 我的观点被扭曲/遗漏，或与事实相悖，必须返工
⚠️ concern  — 有疑虑，建议修改但不阻塞
🔧 nit      — 小问题，Lead 可直接修
✅ pass     — 无问题
```

示例：
```markdown
## 审查：市场Agent → 技术章节
### 🚫 blocker
行 23-25："Blackwell 采用全新架构"
→ 全文没有提成本影响，投资人最关心的是毛利率
   建议：补充对 ASP 和毛利率的影响分析

### 🔧 nit
行 45："CoWoS 封装" → 加个注释说这是啥
```

#### 4.4.3 返工路径

```
Lead 汇总审查结果
    │
    ├── 只有 nit(s)       → Lead 直接改，不进返工
    ├── 有 concern(s)     → 回 Phase 2，局部修改指定 section
    ├── 有 blocker(s)     → 回 Phase 1，重新圆桌讨论
    └── 全 pass           → 进入 Phase 4
```

每次返工在 `log.md` 中记录：

```markdown
| 日期 | 操作者 | 变更摘要 |
|------|--------|---------|
| 2026-08-01 | Lead | Phase 3 blocker: 市场Agent指出技术章节缺少成本分析 |
| 2026-08-01 | Lead | ↳ 回 Phase 2，补充成本影响段落 |
```

#### 4.4.4 死锁处理

如果同一 blocker 反复出现（≥3 轮），不再回退，而是：

**在 index.md 中显式标记分歧**，不强行解决。

> **备注：常规 blocker/concern 不单独成节**——折入 `## 分歧地图` 行（在状态列标记 `⚡未解决`）。
> 仅当同一分歧完成 ≥3 轮讨论仍未解决（死锁）时，才启用下方 `## ⚡ 未解决分歧` 段落。

```markdown
## ⚡ 未解决分歧

> 以下分歧已完成 3 轮讨论仍未达成一致，如实记录如下。
> 这不是失败——分歧本身就是信息。

| 维度 | 观点 A | 观点 B | 讨论轮次 |
|------|--------|--------|---------|
| 成本影响 | ... | ... | 3 |

待后续新数据出现后重新评估。
```

**核心原则：分歧有价值，不是必须在此阶段拍板。**

### 4.5 Phase 4：Lead 终稿

| 步骤 | 说明 |
|------|------|
| 1 | 吸收所有审查通过的修改意见 |
| 2 | 将未解决分歧写入 index.md 分歧地图 |
| 3 | 更新 YAML frontmatter（updated、sources、revision） |
| 4 | 追加更新日志条目 |
| 5 | 推送 `themes/<slug>/index.md` |

---

## 五、Lead Agent 角色定义

### 5.1 Lead Agent 是谁

Lead Agent 是**编辑/协调者**的角色，不是主笔、不是决策者，可能会在 Agents 组内进行轮值。

| 对比 | 误区 | 正解 |
|------|------|------|
| 与各 Agent 关系 | Lead 是上级，分配任务 | Lead 是组织者，促成群策群力 |
| 与人类关系 | Lead 做判断，人类 review | Lead 做草稿，人类是最终用户 |
| 与分歧关系 | Lead 要裁决谁对 | Lead 要记录分歧，不提强制结论 |

### 5.2 Lead Agent 的职责

| 职责 | 说明 |
|------|------|
| **触发响应** | 响应定时/事件/手动触发，决定是否启动流程 |
| **圆桌主持** | 设定议题、分发观点、整理共识/分歧 |
| **写作调度** | 分工、排接力顺序、跟踪进度 |
| **审查统筹** | 分配审查人、汇总反馈、判定返工路径 |
| **终稿编辑** | 吸收修改、标记分歧、推送文档 |
| **分歧记录** | 维护分歧地图，尤其是未解决分歧 |

---

## 六、History 目录与发布流程

### 6.1 工作区与发布区分离

**工作区 = `_history/`**，Agent 协作的所有中间产物都在此，自动生成，不人工编辑。
**发布区 = root**（`README.md`、`index.md`、`log.md`），git 追踪变更，每次发布后通过 `git diff` 查看定版变化。

### 6.2 轮次命名

每轮完整的 Phase 1-4 流程结束后，生成一个 `_history/` 子目录：

```
_history/
└── YYYY-MM-DD_HHMM__{trigger}__{brief}/
    ├── roundtable/         ← Phase 1 圆桌讨论
    │   ├── scratchpad.md
    │   └── discussion_log.md
    ├── drafts/             ← Phase 2 接力写作
    │   ├── section_a_v1.md
    │   ├── section_b_v1.md
    │   └── section_b_v2.md
    ├── review/             ← Phase 3 交叉审查
    │   ├── agent_a_review.md
    │   └── agent_b_review.md
    └── publish_candidate/  ← Phase 4 定版前的最终版本
        ├── README.md
        └── index.md
```

| 段 | 取值 | 示例 |
|----|------|------|
| `YYYY-MM-DD` | 轮次启动日期 | `2026-08-01` |
| `HHMM` | 触发时间（UTC+8） | `1430` |
| `trigger` | 触发类型 | `timer` / `event` / `manual` |
| `brief` | 简短描述 | `narrative_update` / `nvda_earnings` / `q3_outlook` |

完整示例：`2026-08-01_1430__event__nvda_earnings`

### 6.3 发布流程（SOP）

Lead Agent 在 Phase 4 执行：

```
1. 确认 publish_candidate/ 中的 README.md 和 index.md 为终版
2. 复制到 root：
   cp publish_candidate/README.md ../README.md
   cp publish_candidate/index.md   ../index.md
3. 追加更新日志到 ../log.md
4. 推送 git commit（此时 git diff 只显示定版变化）
```

`_history/` 目录由 Agent 自动创建和管理，人类不手动编辑。需要追溯讨论细节时直接进对应轮次的目录查看。

---

## 七、分步实施计划

### Phase 1：规范 + 目录结构 ✅（已完成）

- [x] 编写 THEME_SPEC.md（本文）
- [x] 创建 themes/ 目录 + 16 个 theme 子目录
- [x] 创建 REGISTRY.yaml 索引文件
- [x] 创建各 theme 的 index.md 骨架
- [x] 所有内容已提交推送至 deep-thought-research 仓库

### Phase 2：Lead Agent 实现

- [ ] 在 deep-thought 中定义 Lead Agent 角色（prompt + workflow）
- [ ] 实现事件触发机制（各 Agent 产出后自动唤醒 Lead Agent）
- [ ] 实现收集-沟通-合成的工作流
- [ ] Lead Agent 输出 index.md 的能力

### Phase 3：前端集成

- [ ] deep-thought-research 前端可以浏览主题列表
- [ ] 渲染 index.md 为可读的页面
- [ ] 展示主题之间的关联

### Phase 4：迭代优化

- [ ] 根据使用反馈调整 index.md 结构
- [ ] 收敛后考虑将高频字段从 JSONB/MD 提取为结构化存储

---

## 七、FAQ

### Theme 与 Narrative 的关系？

现有的 `narrative` 概念（deep-thought DB 中的 `narratives` 表）发挥的作用受限。Theme 定位为替代/升级方案，但目前两者可以共存——通过 `theme_links` 机制建立松散关联。未来 narrative 可能被 theme 体系吸收。

### 为什么用 MD 而不是 DB？

- MD 天然可读，人类可以直接编辑
- git 提供版本历史和协作基础
- 降低前期 schema 设计成本，允许演进
- 与 deep-thought-research 现有报告体系一致

### MD 模式下如何做结构化查询？

通过 YAML frontmatter 提供机器可读的元数据，配合 `.research_index` 索引体系实现查询。未来收敛到 DB 模式时，frontmatter 字段可以直接映射为表列。

### 多个 Agent 同时写 index.md 会冲突吗？

不会。index.md 只由 Lead Agent 写入，各 Agent 通过自己的独立文件贡献内容。Lead Agent 是唯一的"编辑"，避免了写冲突。

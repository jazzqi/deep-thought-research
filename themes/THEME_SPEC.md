# Theme 系统设计规范

> 投资主题（Themes）是 Deep Thought 系统主动跟踪的核心关注单元。
> 每个 Theme 是一个**不断演进的 Big Picture**，由多个 Agent 协作维护。

---

## 一、背景与动机

### 现状问题

当前 `deep-thought-research` 按 **Agent 维度**组织：

```
sector/tech_generalist/2026-07-19-xxx.md   ← 按 agent 分
macro/soros/xxx.md
sentimental/kahneman/xxx.md
portfolio/cio/xxx.md
```

每个 Agent 独立产出，但缺少**按主题聚合**的视角。用户关心的是"NVDA 现在怎么样"，而不是"tech_generalist 今天写了什么"。

### Theme 的定位

Theme 是：

- **投资主题**——系统主动跟踪的若干个投资方向（数个到十几个）
- **跨 Agent 的聚合单元**——各 Agent 的产出最终汇聚到 Theme
- **不断演进的 Big Picture**——不是一次性报告，是活着的文档
- **人机协作的产物**——Lead Agent 维护，人类 review/override

---

## 二、文件结构

```
deep-thought-research/
├── themes/                              ← 投资主题目录
│   ├── THEME_SPEC.md                    ← 本规范文件
│   ├── nvda/                            ← 每个 theme 一个目录
│   │   ├── index.md                     ← Lead Agent 维护的主文档
│   │   └── log.md                       ← 变更日志（可选）
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
tags:
  - semiconductors
  - AI
  - growth
assets:
  - NVDA                                  # 关联 ticker
related_themes:
  - semiconductor                         # 关联 theme slug
---
```

### 3.2 正文结构

```markdown
## Big Picture

> 由 Lead Agent 维护的连贯叙事。
> 回答：这个主题当前处于什么阶段？最核心的驱动力是什么？
> 每次更新时重写此节，保持最新。

## 各维度分析

### 叙事/情绪面
> 来源：tech_generalist / ai_specialist 等

Lead Agent 提炼的摘要 + 个人评注。

### 基本面
> 来源：buffett

...

### 宏观背景
> 来源：dalio / soros / zhou_jintao

...

### [其他维度]
> 根据 theme 特点自由添加

...

## 预测时间线

| 时间窗 | 预测 | 置信度 | 提出者 | 提出日期 | 验证 |
|--------|------|--------|--------|----------|------|
| 短期(1-4w) | ... | 7/10 | Soros | 2026-07-29 | 待验证 |
| 中期(1-3m) | ... | 5/10 | Buffett | 2026-07-28 | 待验证 |
| 长期(6m+) | ... | 6/10 | Lead | 2026-07-29 | 待验证 |

> 预测**不删除**——只追加或标记状态变更。
> 用于追踪 Agent 的预测 accuracy，形成 accountability。

## 分歧地图

| 维度 | 观点 A | 观点 B | 分歧根因 |
|------|--------|--------|---------|
| 估值 | 合理（Soros） | 偏高（Buffett） | 对增长持续性的假设不同 |
| 入场时机 | 现在（Soros） | 等回调（Buffett） | 风险偏好差异 |

> 分歧是核心信息——不同分析框架得出不同结论是常态。

## Agent 观点摘要

> Lead Agent 在此列出各 Agent 的核心贡献，并标注分歧点。
> 每个 Agent 的观点保持独立段落，不强制统一。

## 更新日志

| 日期 | 操作者 | 变更摘要 |
|------|--------|---------|
| 2026-07-29 | Lead Agent | 集成 tech_scan 和宏观更新，调整 Big Picture |
| 2026-07-28 | Soros | 补充反身性分析 |
| 2026-07-28 | Buffett | 质疑估值假设 |
```

### 3.3 核心原则

1. **Big Picture 是灵魂**——每次更新重点维护，保持连贯叙事
2. **预测不删只追加**——旧预测保留，标记验证状态
3. **分歧显式化**——不强行统一，分歧表是核心产出
4. **来源可追溯**——每个观点标注来源 agent + 原文路径

---

## 四、Lead Agent 工作流

### 4.1 触发机制

事件驱动，在各 Agent 产出后触发：

```
[事件] tech_generalist 完成 narrative scan
[事件] buffett 完成基本面分析
[事件] soros 完成宏观分析
       │
       ▼
Lead Agent 被唤醒
       │
       ├── 1. 收集：读取相关 Agent 的最新产出
       ├── 2. 沟通：与相关 Agent 追问/澄清
       ├── 3. 合成：更新 index.md
       └── 4. 通知：通知人类 + 下游 Agent
```

### 4.2 Lead Agent 的职责

| 职责 | 说明 |
|------|------|
| **收集** | 读取各 Agent 的最新报告，提取与 theme 相关的内容 |
| **沟通** | 与各 Agent 进行对话，澄清分歧、追问推理细节 |
| **合成** | 更新 Big Picture、整合多维度分析、维护分歧地图 |
| **协调** | 确保各 Agent 的分析覆盖全面，不遗漏关键维度 |
| **归档** | 维护更新日志，记录预测的验证状态 |

### 4.3 沟通协议

Lead Agent 与各 Agent 的通信（示例）：

```
Lead Agent → Soros:
  我看到你基于反身性理论认为 NVDA 处于正反馈循环中。
  请问你的判断中，这个反馈循环的脆弱点在哪里？
  什么条件会导致循环断裂？

Soros → Lead Agent:
  脆弱点在于：1) 若 Blackwell 发货不及预期，会打破"需求→收入→capex→需求"循环
  2) 估值本身已包含较高预期，miss 的惩罚会很大
  监控指标：下期财报的数据中心收入环比增速
```

### 4.4 输出物

每次 Lead Agent 运行后：

1. **更新** `themes/<slug>/index.md`（核心产出）
2. **可选** 在 `themes/<slug>/log.md` 追加运行记录

---

## 五、Agent 协作协议

### 5.1 分工规则

| 角色 | 写什么 | 覆盖规则 |
|------|--------|---------|
| **各 Agent** | 自己的报告（macro/soros/ 等） | 独立文件，互不干扰 |
| **Lead Agent** | themes/<slug>/index.md | 全面负责，但对来源标注清晰 |
| **人类（你）** | 任何文件 | 最高权限，可直接编辑/override |
| **CEO 等下游 Agent** | 读取 themes/ 后产出决策报告 | 只读，不写 theme 文件 |

### 5.2 与现有报告系统的关系

```
各 Agent 日常产出
  macro/soros/2026-07-29-xxx.md     ← Agent 独立产出（已有）
  sector/tech_generalist/xxx.md      ← Agent 独立产出（已有）
  fundamental/buffett/xxx.md         ← Agent 独立产出（已有）
           │
           ▼ (事件驱动)
Lead Agent 收集、沟通、合成
           │
           ▼
themes/nvda/index.md                 ← 聚合视图（新增）
           │
           ▼
portfolio/cio/xxx.md                 ← CEO 等下游 Agent 消费后产出决策（已有）
```

---

## 六、分步实施计划

### Phase 1：规范 + 目录结构（本文档）

- [x] 编写 THEME_SPEC.md（本文）
- [ ] 创建 themes/ 目录
- [ ] 创建 REGISTRY.yaml 索引文件
- [ ] 创建第一个 theme 目录（nvda）和 index.md 骨架

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

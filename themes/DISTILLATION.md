# 主题数据蒸馏协议（DISTILLATION）

> **⚠️ 本协议是 kickstarter（初始建议），不是强制规范。**
> Agent 应根据实际运行情况自发维护、调整本协议、`depends_on` 与 REGISTRY.yaml 中的
> `related_themes`，使其逐渐收敛为符合系统真实依赖结构的"活文档"。
> 不要把它当作静态 ground truth。

---

## 一、背景与动机

### 问题：下游重复查询原始数据

主题之间存在天然的信息层级。下游主题（如 qqq 指数）分析时，经常缺少上游主题
（宏观/估值）**已核验的结论**，导致：

- Agent 反复查询 + 重试原始数据源（实例：qqq 一轮跑了 19 分钟 vs 正常 11 分钟）
- 同一份宏观数据被多个下游各自拉取、各自加工，重复浪费
- 结论口径不一致——各主题对同一数据各自解读，可能产出互相矛盾的判断

### 目标：倒金字塔式蒸馏

借鉴"倒金字塔写作"思想：**上游先发布结论，下游引用上游已核验的结论，而不是重新
查一遍原始数据**。形成自宏观向个股逐层收敛的蒸馏结构：

```
        L1 宏观/全球（global-macro / fed / market-daily / market-sentiment / geo-conflicts）
            │  先发布，提供已核验的宏观/全景结论
            ▼
        L2 行业/资产（semiconductor / energy / cryptocurrency / china-internet / ...）
            │  引用 L1 结论，叠加行业/资产自身的供需与结构数据
            ▼
        L3 个股/指数（nvda / qqq / pdd / btc / ...）
            引用 L1 + L2 结论，专注个股/指数自身的竞争地位与估值
```

---

## 二、主题层级概念

> 层级是**建议性的描述框架**，用于帮助 Agent 判断"谁先发布、谁引用谁"。
> 实际层级由 `depends_on` 声明决定，本节分类是初始建议。
> 同一主题在不同语境下可能跨层（如 btc 既是 L1 宏观的"流动性传感器"，也是
> L3 的单一资产）。层级不是硬约束。

### L1 宏观/全球（上游提供者）

跟踪全局变量，**先发布**，被下游广泛引用。`depends_on` 通常为空或最少。

| 主题 | 提供什么 |
|------|---------|
| global-macro | 全球/中美宏观：流动性、通胀、就业、增长、利率路径 |
| fed | 美联储货币政策路径、利率、资产负债表 |
| market-daily | 每日市场全景快照：指数、跨资产联动、风险偏好 |
| market-sentiment | 情绪面：Fear&Greed、叙事热度、泡沫/极端估值信号 |
| geo-conflicts | 地缘冲突、黑天鹅事件、避险资产定价传导 |

### L2 行业/资产（中游）

引用 L1 的宏观背景，叠加行业/资产自身的供需与结构数据。

| 主题 | 上游依赖（初始建议） | 提供什么 |
|------|---------------------|---------|
| semiconductor | global-macro、geo-conflicts | 半导体周期、foundry、设备 capex |
| optical-modules | semiconductor、global-macro | 光模块需求、技术路线、供应链 |
| energy | global-macro、geo-conflicts | 能源供需、OPEC+、地缘溢价 |
| cryptocurrency | global-macro、market-sentiment | 加密市场周期、链上数据、资金流 |
| china-internet | global-macro、market-sentiment | 中国互联网行业、监管周期、消费 |
| pig-cycle | global-macro | 中国猪周期、养殖盈利、CPI 传导 |
| disruptive-innovation | （无，自主扫描） | 颠覆式创新早期信号扫描 |

### L3 个股/指数（下游消费者）

引用 L1/L2 已核验结论，专注个股/指数自身的竞争地位与估值。

| 主题 | 上游依赖（初始建议） |
|------|---------------------|
| nvda | semiconductor、global-macro |
| alphabet | global-macro、market-daily |
| tesla | global-macro、market-daily |
| pdd | china-internet、global-macro |
| btc | global-macro、market-sentiment |
| qqq | global-macro、market-daily、semiconductor |
| spacex | （无，独立跟踪未上市公司） |
| ten-bagger-hunting | disruptive-innovation |

---

## 三、蒸馏规则建议（初始版，非强制）

> 以下是 kickstarter 规则。Agent 应根据实际情况调整：
> - 依赖是否成立、是否值得引用，由 Agent 判断；
> - 没有满足条件的上游结论时，**如实报"上游数据缺失"**，不要伪造引用。

### 3.1 `depends_on` 字段

下游主题的 `README.md` frontmatter 增加 `depends_on`（建议字段，由 Agent 维护）：

```yaml
---
slug: qqq
lead_agent: ackman
depends_on:
  - global-macro
  - market-daily
  - semiconductor
---
```

- `depends_on` 中的 slug 必须真实存在（以 `themes/` 目录 / REGISTRY.yaml 为准）
- **这是"数据依赖"声明，不是"引用关系"全图**——只列下游真正需要的上游结论
- 上游主题 `depends_on` 可以为空（L1 提供者）
- THEME_SPEC §3.4 定义的 README 固定字段（范围/分析框架/典型参与 Agent）不变，
  `depends_on` 是本协议新增的**建议字段**

### 3.2 下游引用上游结论（不重查原始数据）

- 下游 roundtable/relay 启动前，Lead 应优先用 **ReadThemeDocsTool** 读取依赖的
  上游 `index.md`，把上游**已核验的结论**作为输入之一
- 引用方式：在分析中明确标注结论来源与版本，如 `[global-macro index · 2026-08-04]`
- 只有当上游结论缺失 / 过时 / 与事实明显矛盾时，才自行查询原始数据，并在记录中
  说明原因——这能帮 Agent 后续判断该依赖是否仍然成立

### 3.3 上游发布后，下游更新引用

- 上游主题发布新结论（`index.md` 更新）后，**下游若依赖该上游**，应在自己的下一轮
  更新中检查并刷新相关引用（版本/日期）
- 上游 `index.md` 的 `updated` 字段与 `log.md` 的更新记录，是下游判断
  "是否需要刷新引用"的新鲜度信号
- 下游不必每次同步更新，但引用应带日期/版本，避免引用过期结论

### 3.4 发布顺序建议（倒金字塔）

- **上游先发布，下游后发布**。L1 → L2 → L3 的顺序能最大化蒸馏收益
- 同一层级内可并行
- 若上游未及时发布，下游可基于上次已知结论 + 增量数据更新，并显式标注
  "基于旧版本"（如 `基于 global-macro index 2026-08-01`）

---

## 四、维护与演进

### 4.1 谁维护

- `depends_on`：各主题 Lead Agent 根据实际依赖自发维护
- REGISTRY.yaml 的 `related_themes`：与 `depends_on` 保持一致（双向补充——
  A 依赖 B，则 B 的 related 含 A），由 Lead Agent 或人类维护
- 本协议文档：任何 Agent 遇到蒸馏运行中的新规律，可直接补充完善本节

### 4.2 校验

- 所有 `depends_on` / `related_themes` 引用的 slug 必须存在于 REGISTRY.yaml
  （或 `themes/` 目录），不存在则报错提示
- 建议在流水线中做 YAML 解析 + slug 存在性校验（README frontmatter 仍应能
  正常 YAML 解析）

### 4.3 关系维护

- 上游主题升级结论后，建议更新 `index.md` 的 `updated` 字段，方便下游判断新鲜度
- 若某依赖长期无价值（上游结论对下游没有增量信息），下游可移除该依赖，
  并在本协议记录原因
- 新主题创建时，建议同步声明 `depends_on`，并让上游在 `related_themes` 中反向登记

---

## 五、与 THEME_SPEC 的关系

- 本协议是对 THEME_SPEC §一（Theme 生态：交叉/派生/包含）与 §四（四阶段协作
  流程）的**补充**：THEME_SPEC 定义主题如何独立产出，本协议定义主题之间如何蒸馏数据
- THEME_SPEC §3.4 的 README.md 固定职责（scope + 分析框架 + 典型参与 Agent）
  保持不变；`depends_on` 是本协议新增的建议字段（Agent 维护）
- THEME_SPEC §二 的 REGISTRY.yaml 定义保持；本协议要求其 `related_themes` 与
  `depends_on` 双向一致

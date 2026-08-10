# FOMC 成员图谱（FOMC MEMBERS）

> **本文件是美联储 FOMC 成员的官方追踪底稿**（来源：federalreserve.gov/monetarypolicy/fomc.htm）。
> 数据抓取时间：2026-08-10。Agent 每轮用 query_raw_items 更新「最新言论/立场」列，
> 后续分析（index.md 成员立场矩阵 / 点阵图推算 / 投票预测）以本图谱为锚点。
>
> **使用规则**：
> - **成员名单为官方权威**——委员会成员变动以 fomc.htm 为准，禁止凭空增删
> - **「最新言论/立场」列由 agent 每轮更新**（工具查询，带来源与日期，无数据写「数据缺失」）
> - **票委/非票委**：Board of Governors = 常任票委；各联储主席按轮换表轮值票委（见文末）
> - 本图谱与 `template.md`（报告结构）配合：图谱回答「谁在委员会」，模板回答「怎么分析」

---

## 当前委员会成员

| 中文名 | 姓名 | 职位/机构 | 最新言论/立场（日期+来源） | 鹰/鸽 |
|--------|------|----------|--------------------------|--------|
| 凯文·沃什 | Kevin Warsh | Chairman / Board of Governors | 数据缺失 | — |
| 约翰·威廉姆斯 | John C. Williams | Vice Chair / New York | 数据缺失 | — |
| 迈克尔·巴尔 | Michael S. Barr | 成员 / Board of Governors | 数据缺失 | — |
| 米歇尔·鲍曼 | Michelle W. Bowman | 成员 / Board of Governors | 数据缺失 | — |
| 莉萨·库克 | Lisa D. Cook | 成员 / Board of Governors | 数据缺失 | — |
| 贝丝·哈马克 | Beth M. Hammack | 成员 / Cleveland | 数据缺失 | — |
| 菲利普·杰斐逊 | Philip N. Jefferson | 成员 / Board of Governors | 数据缺失 | — |
| 尼尔·卡什卡利 | Neel Kashkari | 成员 / Minneapolis | 数据缺失 | — |
| 洛里·洛根 | Lorie K. Logan | 成员 / Dallas | 数据缺失 | — |
| 安娜·保尔森 | Anna Paulson | 成员 / Philadelphia | 数据缺失 | — |
| 杰罗姆·鲍威尔 | Jerome H. Powell | 成员 / Board of Governors | 数据缺失 | — |
| 克里斯托弗·沃勒 | Christopher J. Waller | 成员 / Board of Governors | 数据缺失 | — |

## 候补成员（Alternates）

| 中文名 | 姓名 | 职位/机构 |
|--------|------|----------|
| 托马斯·巴尔金 | Thomas I. Barkin | Richmond |
| 玛丽·戴利 | Mary C. Daly | San Francisco |
| 奥斯坦·古尔斯比 | Austan D. Goolsbee | Chicago |
| 苏什米塔·舒克拉 | Sushmita Shukla | New York / First Vice President |
| 谢丽尔·维纳布尔 | Cheryl Venable | Atlanta / Interim President |

---

## FOMC 票委轮换（2027-2029）

| 年份 | 票委联储 | 候补 |
|------|---------|------|
| 2027 | New York, Chicago, Richmond, Atlanta, San Francisco | New York†, Cleveland, Boston, St. Louis, Kansas City |
| 2028 | New York, Cleveland, Boston, St. Louis, Kansas City | New York†, Chicago, Philadelphia, Dallas, Minneapolis |
| 2029 | New York, Chicago, Philadelphia, Dallas, Minneapolis | New York†, Cleveland, Richmond, Atlanta, San Francisco |

> † 纽约联储以第一副主席作为主席的候补。
> 注：Board of Governors（7 位）为常任票委；各联储主席按上表轮换。

## 数据源

- 成员名单：federalreserve.gov/monetarypolicy/fomc.htm（官方）
- 轮换表：同上
- 工具查询：query_raw_items（关键词=成员名）更新言论

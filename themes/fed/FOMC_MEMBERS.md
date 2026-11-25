# FOMC 成员图谱（FOMC MEMBERS）

> **本文件由数据库生成（D136），请勿手工编辑。**
> 机器可读数据：`GET /api/fomc/committee-brief`（聚合，推荐）、`GET /api/fomc/statements`（批量言论）、`GET /api/fomc/members`；Agent 工具 `query_fomc_members`（支持逗号分隔多人）。
> 生成时间：2026-11-25 21:00 UTC；名单来源：federalreserve.gov/monetarypolicy/fomc.htm + federalreservehistory.org/people/current-fed-leaders。
> 「最新言论/立场」来自 `fomc_member_statements`（每条可追溯 raw_items）；「鹰/鸽」来自 D137 stance 快照（LLM 分类）；「综合」来自 D138 记分卡（0.6×投票 + 0.4×言论，附样本量与状态）。

---

## 近 30 天立场变化（转边预警）

| 日期 | 成员 | 变化 | Δ分 | 级别 | 依据 |
|------|------|------|-----|------|------|
| 2026-11-20 | 莉萨·库克 | 中性→鹰 | +0.48 | medium | neutral→hawkish，分数 0.13→0.61（Δ+0.48）；近 30 天高置信支持言论 1 条 |
| 2026-11-16 | 米歇尔·鲍曼 | 中性→鹰 | +0.45 | medium | [冷启动基线] neutral→hawkish，分数 0.05→0.50（Δ+0.45）；近 30 天高置信支持言论 2 条 |
| 2026-11-16 | 菲利普·杰斐逊 | 中性→鹰 | +0.28 | medium | [冷启动基线] neutral→hawkish，分数 0.25→0.53（Δ+0.28）；近 30 天高置信支持言论 3 条 |
| 2026-11-16 | 克里斯托弗·沃勒 | 鸽→鹰 | +1.36 | high | dovish→hawkish，分数 -0.60→0.76（Δ+1.36）；近 30 天高置信支持言论 10 条 |

## 委员会综合立场（D138 记分卡）

> 口径：`综合 = 0.6×投票 + 0.4×言论`；`近期 = 365 天内最近 12 点 EMA`；`长期 = 730 天 / τ365`；样本 n 为按「成员+日期」去重后的事件数。仅统计当前票委。

| 口径 | 综合 | 投票轴 | 言论轴 | 票委数 |
|------|------|--------|--------|--------|
| 近期（365d EMA） | 0.233 | 0.055 | 0.545 | 12 |
| 长期（730d） | 0.179 | 0.016 | 0.423 | 12 |

### 言行不一（投票 vs 言论）

| 成员 | 投票轴 | 言论轴 | 差值 | 判定 |
|------|--------|--------|------|------|
| 贝丝·哈马克 | +0.24 | +0.75 | -0.50 | 言论比投票更鹰（表态强于行动） |
| 洛里·洛根 | +0.09 | +0.80 | -0.70 | 言论比投票更鹰（表态强于行动） |
| 尼尔·卡什卡利 | +0.09 | +0.69 | -0.59 | 言论比投票更鹰（表态强于行动） |
| 安娜·保尔森 | +0.06 | +0.69 | -0.63 | 言论比投票更鹰（表态强于行动） |
| 凯文·沃什 | +0.07 | +0.53 | -0.46 | 言论比投票更鹰（表态强于行动） |
| 迈克尔·巴尔 | +0.00 | +0.63 | -0.63 | 言论比投票更鹰（表态强于行动） |
| 约翰·威廉姆斯 | +0.00 | +0.59 | -0.59 | 言论比投票更鹰（表态强于行动） |

## 当前委员会成员

> 当年 12 位 FOMC 票委（7 理事 + 纽约联储主席 + 4 位轮值地区联储主席）。

| 中文名 | 姓名 | 职位/机构 | 最新言论/立场（日期+来源） | 鹰/鸽 | 综合（投票/言论/样本） |
|--------|------|----------|--------------------------|--------|------------------------|
| 凯文·沃什 | Kevin Warsh | 主席 / Board of Governors（常任票委） | 2026-11-25 telegram:Financial_Express：白宫经济顾问称当前通胀并未加速 美联储应重视供给侧因素 | 鹰（+0.54/0.51） | （+0.26，投 +0.07，言 +0.53，n=7/样本少） ⚠️言行不一 |
| 菲利普·杰斐逊 | Philip N. Jefferson | 副主席 / Board of Governors（常任票委） | 2026-11-19 telegram:Financial_Express：11 月 20 日隔夜要闻一览 | 鹰（+0.50/0.52） ⚠️shift_to_hawk | （+0.12，投 +0.00，言 +0.31，n=17/样本少） |
| 米歇尔·鲍曼 | Michelle W. Bowman | 负责监管事务的副主席 / Board of Governors（常任票委） | 2026-11-25 telegram:Financial_Express：美联储理事鲍曼在银行业监管会议上的讲话中未就经济或货币政策前景发表意见。 | 鹰（+0.62/0.50） ⚠️shift_to_hawk | （+0.09，投 +0.00，言 +0.22，n=15/样本少） |
| 克里斯托弗·沃勒 | Christopher J. Waller | 理事 / Board of Governors（常任票委） | 2026-11-23 telegram:Financial_Express：沃什主张美联储应“少出声” 其他官员置若罔闻 | 鹰（+0.68/1.00） ⚠️flip_dove_to_hawk | （+0.11，投 -0.03，言 +0.31，n=20） |
| 杰罗姆·鲍威尔 | Jerome H. Powell | 理事 / Board of Governors（常任票委） | 2026-11-18 telegram:Financial_Express：英国通胀攀升至一年来最高水平 | — | （+0.00，投 +0.00，言 —，n=8/样本少） |
| 莉萨·库克 | Lisa D. Cook | 理事 / Board of Governors（常任票委） | 2026-11-25 telegram:Financial_Express：美国白宫国家经济委员会主任哈塞特 | 鹰（+0.75/0.71） ⚠️shift_to_hawk | （+0.28，投 +0.13，言 +0.49，n=15/样本少） |
| 迈克尔·巴尔 | Michael S. Barr | 理事 / Board of Governors（常任票委） | 2026-11-19 longbridge：Fed's Barr worried regulatory changes may increase financial sector risks | 鹰（+0.80/0.55） | （+0.25，投 +0.00，言 +0.63，n=15/样本少） ⚠️言行不一 |
| 约翰·威廉姆斯 | John C. Williams | FOMC 副主席 / 纽约联储主席（常任票委） | 2026-11-24 longbridge：Federal Reserve Officials Williams Hints: Further Rate Hikes May Be Needed Over Time to Ta… | 鹰（+0.56/1.00） | （+0.24，投 +0.00，言 +0.59，n=13） ⚠️言行不一 |
| 安娜·保尔森 | Anna Paulson | 费城联储主席（2026 票委；下次 2029） | 2026-11-21 longbridge：Philadelphia Fed President Paulson: Does Not Rule Out Consecutive Rate Hikes, Emphasizes "… | 鹰（+0.68/1.00） | （+0.31，投 +0.06，言 +0.69，n=12） ⚠️言行不一 |
| 贝丝·哈马克 | Beth M. Hammack | 克利夫兰联储主席（2026 票委；下次 2028） | 2026-11-19 telegram:Financial_Express：① 港股盘后 阿里巴巴、拼多多、网易发布业绩报告； | 鹰（+0.76/1.00） | （+0.44，投 +0.24，言 +0.75，n=16） ⚠️言行不一 |
| 尼尔·卡什卡利 | Neel Kashkari | 明尼阿波利斯联储主席（2026 票委；下次 2029） | 2026-11-18 telegram:Financial_Express：美联储卡什卡利 | 鹰（+0.71/0.26） | （+0.33，投 +0.09，言 +0.69，n=10/样本少） ⚠️言行不一 |
| 洛里·洛根 | Lorie K. Logan | 达拉斯联储主席（2026 票委；下次 2029） | 2026-11-13 telegram:Financial_Express：美国达拉斯联储主席洛丽·洛根表示，美联储应将为维持市场正常运作而购买的资产，与为货币政策操作而持有的资产区分开来，以便在金融市场承压时期更清楚地传达其意图。 | 鹰（+0.82/0.89） | （+0.37，投 +0.09，言 +0.80，n=12） ⚠️言行不一 |

## 地区联储主席（全部 12 位，含非 2026 票委）

> 所有地区联储主席都参加 FOMC 讨论并提交 SEP 预测；**非票委的言论是
> 判断未来投票倾向 / 政策转向的先行信号**，需持续跟踪。

| 中文名 | 姓名 | 职位/机构 | 最新言论/立场（日期+来源） | 鹰/鸽 | 综合（投票/言论/样本） |
|--------|------|----------|--------------------------|--------|------------------------|
| 苏珊·柯林斯 | Susan M. Collins | 波士顿联储主席（非 2026 票委；2028 轮值票委） | 2026-11-14 longbridge：Fed's Collins: Steady, Gradual Interest Rate Hikes Are Appropriate | 鹰（+0.76/0.64） | （+0.13，投 -0.30，言 +0.77，n=4/样本少） |
| 约翰·威廉姆斯 | John C. Williams | FOMC 副主席 / 纽约联储主席（常任票委） | 2026-11-24 longbridge：Federal Reserve Officials Williams Hints: Further Rate Hikes May Be Needed Over Time to Ta… | 鹰（+0.56/1.00） | （+0.24，投 +0.00，言 +0.59，n=13） ⚠️言行不一 |
| 安娜·保尔森 | Anna Paulson | 费城联储主席（2026 票委；下次 2029） | 2026-11-21 longbridge：Philadelphia Fed President Paulson: Does Not Rule Out Consecutive Rate Hikes, Emphasizes "… | 鹰（+0.68/1.00） | （+0.31，投 +0.06，言 +0.69，n=12） ⚠️言行不一 |
| 贝丝·哈马克 | Beth M. Hammack | 克利夫兰联储主席（2026 票委；下次 2028） | 2026-11-19 telegram:Financial_Express：① 港股盘后 阿里巴巴、拼多多、网易发布业绩报告； | 鹰（+0.76/1.00） | （+0.44，投 +0.24，言 +0.75，n=16） ⚠️言行不一 |
| 托马斯·巴尔金 | Thomas I. Barkin | 里士满联储主席（非 2026 票委；2027 轮值票委） | 2026-11-19 telegram:Financial_Express：① 港股盘后 阿里巴巴、拼多多、网易发布业绩报告； | 鹰（+0.61/0.49） | （+0.54，投 —，言 +0.54，n=3/样本少） |
| 谢丽尔·维纳布尔 | Cheryl Venable | 亚特兰大联储主席（非 2026 票委；2027 轮值票委） | 数据缺失 | — | （+0.00，投 —，言 +0.00，n=1/样本少） |
| 奥斯坦·古尔斯比 | Austan D. Goolsbee | 芝加哥联储主席（非 2026 票委；2027 轮值票委） | 2026-11-20 longbridge：[External Economy] Fed's Goolsbee: Inflation has been worryingly high for several consecut… | 鹰（+0.60/1.00） | （+0.23，投 +0.00，言 +0.58，n=9） |
| 阿尔贝托·穆萨莱姆 | Alberto G. Musalem | 圣路易斯联储主席（非 2026 票委；2028 轮值票委） | 2026-11-18 longbridge：Four consecutive rate hikes? This Federal Reserve official signals the most hawkish stance… | 鹰（+0.90/0.62） | （+0.18，投 -0.30，言 +0.90，n=4/样本少） |
| 尼尔·卡什卡利 | Neel Kashkari | 明尼阿波利斯联储主席（2026 票委；下次 2029） | 2026-11-18 telegram:Financial_Express：美联储卡什卡利 | 鹰（+0.71/0.26） | （+0.33，投 +0.09，言 +0.69，n=10/样本少） ⚠️言行不一 |
| 杰弗里·施密德 | Jeffrey R. Schmid | 堪萨斯城联储主席（非 2026 票委；2028 轮值票委） | 2026-11-16 longbridge：International ／ Kansas City Fed President Schmid: Inflation Remains Overheated, Fed Needs … | 鹰（+0.77/0.73） | （+0.32，投 +0.00，言 +0.80，n=7/样本少） |
| 洛里·洛根 | Lorie K. Logan | 达拉斯联储主席（2026 票委；下次 2029） | 2026-11-13 telegram:Financial_Express：美国达拉斯联储主席洛丽·洛根表示，美联储应将为维持市场正常运作而购买的资产，与为货币政策操作而持有的资产区分开来，以便在金融市场承压时期更清楚地传达其意图。 | 鹰（+0.82/0.89） | （+0.37，投 +0.09，言 +0.80，n=12） ⚠️言行不一 |
| 玛丽·戴利 | Mary C. Daly | 旧金山联储主席（非 2026 票委；2027 轮值票委） | 2026-11-19 longbridge：[External Economy] Fed Governor Waller Suggests a 50-Basis-Point Rate Hike in December; Sa… | 鹰（+0.61/1.00） | （+0.56，投 —，言 +0.56，n=5） |

## 候补成员（Alternates）

| 中文名 | 姓名 | 职位/机构 |
|--------|------|----------|
| 谢丽尔·维纳布尔 | Cheryl Venable | Interim President / Atlanta |
| 奥斯坦·古尔斯比 | Austan D. Goolsbee | President / Chicago |
| 苏什米塔·舒克拉 | Sushmita Shukla | First Vice President / New York |
| 托马斯·巴尔金 | Thomas I. Barkin | President / Richmond |
| 玛丽·戴利 | Mary C. Daly | President / San Francisco |

---

## FOMC 票委轮换（2027-2029）

| 年份 | 票委联储 | 候补 |
|------|---------|------|
| 2027 | Atlanta, Chicago, New York, Richmond, San Francisco | Boston, Cleveland, Kansas City, New York, St. Louis |
| 2028 | Boston, Cleveland, Kansas City, New York, St. Louis | Chicago, Dallas, Minneapolis, New York, Philadelphia |
| 2029 | Chicago, Dallas, Minneapolis, New York, Philadelphia | Atlanta, Cleveland, New York, Richmond, San Francisco |

> 纽约联储以第一副主席作为主席的候补；理事为常任票委。

## 数据源

- 成员/投票权/轮换：federalreserve.gov/monetarypolicy/fomc.htm
- 完整领导名单/Board 职衔：federalreservehistory.org/people/current-fed-leaders
- 会议决议/票数：FOMC 声明原文 + FRED DFEDTARU/DFEDTARL
- 成员言论：raw_items 预采集（`scripts/extract_fomc_member_news.py`）

# FOMC 成员图谱（FOMC MEMBERS）

> **本文件由数据库生成（D136），请勿手工编辑。**
> 机器可读数据：`GET /api/fomc/committee-brief`（聚合，推荐）、`GET /api/fomc/statements`（批量言论）、`GET /api/fomc/members`；Agent 工具 `query_fomc_members`（支持逗号分隔多人）。
> 生成时间：2026-11-17 07:22 UTC；名单来源：federalreserve.gov/monetarypolicy/fomc.htm + federalreservehistory.org/people/current-fed-leaders。
> 「最新言论/立场」来自 `fomc_member_statements`（每条可追溯 raw_items）；「鹰/鸽」来自 D137 stance 快照（LLM 分类）；「综合」来自 D138 记分卡（0.6×投票 + 0.4×言论，附样本量与状态）。

---

## 近 30 天立场变化（转边预警）

| 日期 | 成员 | 变化 | Δ分 | 级别 | 依据 |
|------|------|------|-----|------|------|
| 2026-11-16 | 米歇尔·鲍曼 | 中性→鹰 | +0.45 | medium | [冷启动基线] neutral→hawkish，分数 0.05→0.50（Δ+0.45）；近 30 天高置信支持言论 2 条 |
| 2026-11-16 | 菲利普·杰斐逊 | 中性→鹰 | +0.28 | medium | [冷启动基线] neutral→hawkish，分数 0.25→0.53（Δ+0.28）；近 30 天高置信支持言论 3 条 |
| 2026-11-16 | 克里斯托弗·沃勒 | 鸽→鹰 | +1.36 | high | dovish→hawkish，分数 -0.60→0.76（Δ+1.36）；近 30 天高置信支持言论 10 条 |

## 委员会综合立场（D138 记分卡）

> 口径：`综合 = 0.6×投票 + 0.4×言论`；`近期 = 365 天内最近 12 点 EMA`；`长期 = 730 天 / τ365`；样本 n 为按「成员+日期」去重后的事件数。仅统计当前票委。

| 口径 | 综合 | 投票轴 | 言论轴 | 票委数 |
|------|------|--------|--------|--------|
| 近期（365d EMA） | 0.17 | 0.002 | 0.421 | 12 |
| 长期（730d） | 0.141 | 0.016 | 0.328 | 12 |

### 言行不一（投票 vs 言论）

| 成员 | 投票轴 | 言论轴 | 差值 | 判定 |
|------|--------|--------|------|------|
| 洛里·洛根 | +0.06 | +0.84 | -0.78 | 言论比投票更鹰（表态强于行动） |
| 贝丝·哈马克 | +0.15 | +0.70 | -0.55 | 言论比投票更鹰（表态强于行动） |
| 尼尔·卡什卡利 | +0.06 | +0.76 | -0.70 | 言论比投票更鹰（表态强于行动） |
| 克里斯托弗·沃勒 | -0.09 | +0.40 | -0.48 | 言论比投票更鹰（表态强于行动） |

## 当前委员会成员

> 当年 12 位 FOMC 票委（7 理事 + 纽约联储主席 + 4 位轮值地区联储主席）。

| 中文名 | 姓名 | 职位/机构 | 最新言论/立场（日期+来源） | 鹰/鸽 | 综合（投票/言论/样本） |
|--------|------|----------|--------------------------|--------|------------------------|
| 凯文·沃什 | Kevin Warsh | 主席 / Board of Governors（常任票委） | 2026-11-17 longbridge：Is the AI Boom an Engine or a Bubble? Fed Chair Warsh Outlines Three Scenarios: Productivi… | 鹰（+0.41/0.23） | （+0.05，投 +0.04，言 +0.07，n=10） |
| 菲利普·杰斐逊 | Philip N. Jefferson | 副主席 / Board of Governors（常任票委） | 2026-11-14 longbridge：Fed Vice Chair Jefferson: Inflation Will Determine Interest Rate Decisions | 鹰（+0.62/0.22） ⚠️shift_to_hawk | （+0.05，投 -0.05，言 +0.20，n=20/样本少） |
| 米歇尔·鲍曼 | Michelle W. Bowman | 负责监管事务的副主席 / Board of Governors（常任票委） | 2026-11-11 longbridge：Fed's Bowman Assessment: Inflation is Widening, Another Rate Hike Possible This Year; US S… | 鹰（+0.62/0.60） ⚠️shift_to_hawk | （+0.07，投 -0.05，言 +0.25，n=20） |
| 克里斯托弗·沃勒 | Christopher J. Waller | 理事 / Board of Governors（常任票委） | 2026-11-11 longbridge：Fed Governor Waller: Supports a One-Time 50-Basis-Point Rate Hike if Inflation Accelerates… | 鹰（+0.63/0.96） ⚠️flip_dove_to_hawk | （+0.11，投 -0.09，言 +0.40，n=20） ⚠️言行不一 |
| 杰罗姆·鲍威尔 | Jerome H. Powell | 理事 / Board of Governors（常任票委） | 数据缺失 | — | （-0.03，投 -0.05，言 +0.00，n=14/样本少） |
| 莉萨·库克 | Lisa D. Cook | 理事 / Board of Governors（常任票委） | 数据缺失 | —（低置信 +0.13） ⚠️shift_to_neutral | （+0.07，投 +0.04，言 +0.12，n=20/样本少） |
| 迈克尔·巴尔 | Michael S. Barr | 理事 / Board of Governors（常任票委） | 2026-11-16 telegram:Financial_Express：美联储理事巴尔：AI 智能体可能加剧未来的银行挤兑 | 鹰（+0.71/0.24） | （+0.04，投 -0.05，言 +0.19，n=20） |
| 约翰·威廉姆斯 | John C. Williams | FOMC 副主席 / 纽约联储主席（常任票委） | 2026-11-13 longbridge：Fed's Williams says central bank has 'work to do' to get inflation back on target | 鹰（+0.62/0.28） | （+0.24，投 -0.05，言 +0.68，n=10/样本少） |
| 安娜·保尔森 | Anna Paulson | 费城联储主席（2026 票委；下次 2029） | 2026-11-11 longbridge：Fed's Paulson: Gradual Rate Hikes Still Needed to Bring Inflation Back to 2% Target | 鹰（+0.79/0.61） | （+0.37，投 +0.04，言 +0.87，n=9/样本少） |
| 贝丝·哈马克 | Beth M. Hammack | 克利夫兰联储主席（2026 票委；下次 2028） | 2026-11-17 longbridge：Federal Reserve's Hammack Reiterates Support for Small, Gradual Interest Rate Hikes | 鹰（+0.79/1.00） | （+0.37，投 +0.15，言 +0.70，n=18） ⚠️言行不一 |
| 尼尔·卡什卡利 | Neel Kashkari | 明尼阿波利斯联储主席（2026 票委；下次 2029） | 数据缺失 | 鹰（+0.88/0.20） | （+0.34，投 +0.06，言 +0.76，n=10/样本少） ⚠️言行不一 |
| 洛里·洛根 | Lorie K. Logan | 达拉斯联储主席（2026 票委；下次 2029） | 2026-11-13 longbridge：Fed's Logan: U.S. Treasury Market Functioning Well, Fed Needs to Strengthen Support Tools | 鹰（+0.84/1.00） | （+0.37，投 +0.06，言 +0.84，n=13） ⚠️言行不一 |

## 地区联储主席（全部 12 位，含非 2026 票委）

> 所有地区联储主席都参加 FOMC 讨论并提交 SEP 预测；**非票委的言论是
> 判断未来投票倾向 / 政策转向的先行信号**，需持续跟踪。

| 中文名 | 姓名 | 职位/机构 | 最新言论/立场（日期+来源） | 鹰/鸽 | 综合（投票/言论/样本） |
|--------|------|----------|--------------------------|--------|------------------------|
| 苏珊·柯林斯 | Susan M. Collins | 波士顿联储主席（非 2026 票委；2028 轮值票委） | 2026-11-14 longbridge：Fed's Collins: Steady, Gradual Interest Rate Hikes Are Appropriate | 鹰（+0.74/0.61） | （+0.11，投 -0.30，言 +0.72，n=4/样本少） |
| 约翰·威廉姆斯 | John C. Williams | FOMC 副主席 / 纽约联储主席（常任票委） | 2026-11-13 longbridge：Fed's Williams says central bank has 'work to do' to get inflation back on target | 鹰（+0.62/0.28） | （+0.24，投 -0.05，言 +0.68，n=10/样本少） |
| 安娜·保尔森 | Anna Paulson | 费城联储主席（2026 票委；下次 2029） | 2026-11-11 longbridge：Fed's Paulson: Gradual Rate Hikes Still Needed to Bring Inflation Back to 2% Target | 鹰（+0.79/0.61） | （+0.37，投 +0.04，言 +0.87，n=9/样本少） |
| 贝丝·哈马克 | Beth M. Hammack | 克利夫兰联储主席（2026 票委；下次 2028） | 2026-11-17 longbridge：Federal Reserve's Hammack Reiterates Support for Small, Gradual Interest Rate Hikes | 鹰（+0.79/1.00） | （+0.37，投 +0.15，言 +0.70，n=18） ⚠️言行不一 |
| 托马斯·巴尔金 | Thomas I. Barkin | 里士满联储主席（非 2026 票委；2027 轮值票委） | 2026-11-10 longbridge：Two Federal Reserve Officials Strike Hawkish Tone: Barkin Says Direction of Rate Hikes Is … | 鹰（+0.61/0.81） | （+0.28，投 —，言 +0.28，n=5/样本少） |
| 谢丽尔·维纳布尔 | Cheryl Venable | 亚特兰大联储主席（非 2026 票委；2027 轮值票委） | 数据缺失 | — | （+0.00，投 —，言 +0.00，n=1/样本少） |
| 奥斯坦·古尔斯比 | Austan D. Goolsbee | 芝加哥联储主席（非 2026 票委；2027 轮值票委） | 2026-11-13 longbridge：Fed's Goolsbee: US Inflation Issues Increasingly Severe, Further Action Still Needed | 鹰（+0.61/0.99） | （+0.20，投 +0.00，言 +0.51，n=7） |
| 阿尔贝托·穆萨莱姆 | Alberto G. Musalem | 圣路易斯联储主席（非 2026 票委；2028 轮值票委） | 2026-11-06 longbridge：Fed's Musalem: Businesses say inflation remains top concern | 鹰（+0.88/0.60） | （+0.12，投 -0.30，言 +0.75，n=5/样本少） |
| 尼尔·卡什卡利 | Neel Kashkari | 明尼阿波利斯联储主席（2026 票委；下次 2029） | 数据缺失 | 鹰（+0.88/0.20） | （+0.34，投 +0.06，言 +0.76，n=10/样本少） ⚠️言行不一 |
| 杰弗里·施密德 | Jeffrey R. Schmid | 堪萨斯城联储主席（非 2026 票委；2028 轮值票委） | 2026-11-16 longbridge：International ／ Kansas City Fed President Schmid: Inflation Remains Overheated, Fed Needs … | 鹰（+0.74/0.89） | （+0.30，投 +0.00，言 +0.74，n=8） |
| 洛里·洛根 | Lorie K. Logan | 达拉斯联储主席（2026 票委；下次 2029） | 2026-11-13 longbridge：Fed's Logan: U.S. Treasury Market Functioning Well, Fed Needs to Strengthen Support Tools | 鹰（+0.84/1.00） | （+0.37，投 +0.06，言 +0.84，n=13） ⚠️言行不一 |
| 玛丽·戴利 | Mary C. Daly | 旧金山联储主席（非 2026 票委；2027 轮值票委） | 2026-11-14 longbridge：Fed's Daly: Inflation Continues to Worsen, Further Rate Hikes Likely Necessary | 鹰（+0.76/1.00） | （+0.69，投 —，言 +0.69，n=5） |

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

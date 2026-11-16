# FOMC 成员图谱（FOMC MEMBERS）

> **本文件是美联储 FOMC 成员的官方追踪底稿**（来源：federalreserve.gov/monetarypolicy/fomc.htm）。
> 数据抓取时间：2026-11-16（官网 Last Update：October 28, 2026）。
> 「最新言论/立场」列由系统预采集或 agent 更新（带日期+来源，无可靠数据写「数据缺失」），
> 后续分析（index.md 成员立场矩阵 / 点阵图推算 / 投票预测）以本图谱为锚点。
>
> **使用规则**：
> - **成员名单为官方权威**——委员会成员变动以 fomc.htm 为准，禁止凭空增删
> - **票委/非票委**：Board of Governors（含主席）为常任票委；各联储主席按轮换表轮值票委（见文末）
> - **「鹰/鸽」不由新闻标题自动推断**——无官方/人工依据时保持「—」
> - 本图谱与 `template.md`（报告结构）配合：图谱回答「谁在委员会」，模板回答「怎么分析」

---

## 当前委员会成员

> 官方 `Committee Members` 即**当年 12 位 FOMC 票委**（7 理事 + 纽约联储主席 + 4 位轮值地区联储主席）；候补成员为非票委。

| 中文名 | 姓名 | 职位/机构 | 最新言论/立场（日期+来源） | 鹰/鸽 |
|--------|------|----------|--------------------------|--------|
| 凯文·沃什 | Kevin Warsh | 主席 / Board of Governors（常任票委） | 2026-11-06 longbridge：Warsh Pushes for Reform of Federal Reserve Meeting Mechanism: Fewer Rate Decisions, More S… | — |
| 约翰·威廉姆斯 | John C. Williams | 副主席 / 纽约（常任票委） | 2026-11-13 longbridge：Fed's Williams says central bank has 'work to do' to get inflation back on target | — |
| 迈克尔·巴尔 | Michael S. Barr | 理事 / Board of Governors（常任票委） | 2026-11-12 longbridge：Fed's Barr: US should prepare for "serious" AI job disruption, widening inequality | — |
| 米歇尔·鲍曼 | Michelle W. Bowman | 理事 / Board of Governors（常任票委） | 2026-11-11 longbridge：Fed's Bowman Assessment: Inflation is Widening, Another Rate Hike Possible This Year; US S… | — |
| 莉萨·库克 | Lisa D. Cook | 理事 / Board of Governors（常任票委） | 数据缺失 | — |
| 贝丝·哈马克 | Beth M. Hammack | 克利夫兰联储主席（2026 轮值票委） | 2026-11-12 longbridge：Fed's Hammack: Further Rate Hikes Needed to Curb Inflation | — |
| 菲利普·杰斐逊 | Philip N. Jefferson | 理事 / Board of Governors（常任票委） | 2026-11-14 longbridge：Fed Vice Chair Jefferson: Inflation Will Determine Interest Rate Decisions | — |
| 尼尔·卡什卡利 | Neel Kashkari | 明尼阿波利斯联储主席（2026 轮值票委） | 2026-10-02 telegram:Financial_Express：美联储官员卡什卡利：人工智能并非推动美国经济增长的唯一动力 | — |
| 洛里·洛根 | Lorie K. Logan | 达拉斯联储主席（2026 轮值票委） | 2026-11-13 longbridge：Fed's Logan: U.S. Treasury Market Functioning Well, Fed Needs to Strengthen Support Tools | — |
| 安娜·保尔森 | Anna Paulson | 费城联储主席（2026 轮值票委） | 2026-11-11 longbridge：Fed's Paulson: Gradual Rate Hikes Still Needed to Bring Inflation Back to 2% Target | — |
| 杰罗姆·鲍威尔 | Jerome H. Powell | 理事 / Board of Governors（常任票委） | 数据缺失 | — |
| 克里斯托弗·沃勒 | Christopher J. Waller | 理事 / Board of Governors（常任票委） | 2026-11-11 longbridge：Fed Governor Waller: Supports a One-Time 50-Basis-Point Rate Hike if Inflation Accelerates… | — |

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
| 2027 | New York, Chicago, Richmond, Atlanta, San Francisco | New York, Cleveland, Boston, St. Louis, Kansas City |
| 2028 | New York, Cleveland, Boston, St. Louis, Kansas City | New York, Chicago, Philadelphia, Dallas, Minneapolis |
| 2029 | New York, Chicago, Philadelphia, Dallas, Minneapolis | New York, Cleveland, Richmond, Atlanta, San Francisco |

> † 纽约联储以第一副主席作为主席的候补。
> 注：Board of Governors（7 位）为常任票委；各联储主席按上表轮换。

## 数据源

- 成员名单 / 轮换表：federalreserve.gov/monetarypolicy/fomc.htm（官方）
- 成员言论：raw_items 预采集（`scripts/extract_fomc_member_news.py`）
- 言论明细（日期+来源+片段）：`FOMC_MEMBER_NEWS.md`（每日 04:45 刷新）

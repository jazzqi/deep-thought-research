<tool_call><function=WriteThemeDocsTool><parameter=path>themes/economic-calendar/_history/2026-11-16_0617__manual__readthemedocstool_1_themes_economic_calendar_template_md_v2/reference.md</parameter><parameter=content>
## 审查人 soros 独立核验数据来源（2026-11-15 追加）

- 11-25 核心PCE/PCE/实际PCE/个人收入前值（forecast=None、actual=None，PCE 条目在源中为 medium 重要性）: query_calendar_events(country=US, days=15, importance=high,medium, lookback_days=7) = 核心PCE同比前值3.1/环比0.3；PCE同比3.6/环比0.5；实际PCE环比0.0；个人收入环比0.2
- 11-23~11-29 窗口美联储讲话与美债拍卖条目: query_calendar_events(country=US, days=15, importance=high,medium, lookback_days=7) = 窗口内 0 条 Fed 讲话/拍卖条目；而 11-09~11-20 窗口内每日均有讲话条目（洛根/柯林斯/鲍曼/戴利/杰斐逊/威廉姆斯/穆萨莱姆/哈玛克/古尔斯比/巴尔金/保尔森等），11-20 后条目断流——疑似源数据断档
- 初请序列核验: query_calendar_events(country=US, days=15, importance=high,medium, lookback_days=7) = 11-7当周 actual 20.0（11-12发布，前值18.9、共识19.4）；11-2当周前值18.9；11-14当周条目发布日 11-19（未来），previous 20.0、共识 19.7、actual=None（尚未发布）；11-21当周条目发布日 11-25，previous/actual 均空
- 10月能源CPI同比字段语义: query_calendar_events(country=US, importance=high,medium, lookback_days=7) = "美国10月能源CPI年率-未季调(%)" previous=20.4、actual=None（20.4 属前值字段，10月实值未返回）
- 10月PPI vs 共识: query_calendar_events(country=US, days=15, importance=high,lookback_days=7) = 同比 actual 6.5 < forecast 6.6（低于共识）；环比 actual 0.3 < forecast 0.4
- 10月CPI vs 共识: query_calendar_events(country=US, days=15, importance=high, lookback_days=7) = 环比 actual 0.4 > forecast 0.3（超共识）；核心CPI环比 actual 0.3 > forecast 0.2
- 感恩节休市条目日期: query_calendar_events(country=US, days=15, importance=high,medium, lookback_days=7) = 条目在 11-24T16:00Z 与 11-25T16:00Z 各一条，2026年感恩节实为 11-26 周四（稿件披露正确）
- 11-20 LPR 条目: query_calendar_events(country=CN, days=15, lookback_days=7) = 1年期 previous 3.0 / 5年期 previous 3.5，actual=None、forecast=None（报价日 11-20 尚未到来）
- 中国央行上调金融机构外汇存款准备金率2个百分点（11-15起生效）: query_calendar_events(country=, days=15, importance=high,medium, lookback_days=7) = 重要性 medium，11-13 与 11-14 两条条目，稿件未覆盖
- Anthropic/NVDA/13F 时点: query_calendar_events(country=US, days=15, importance=high,medium, lookback_days=7) = Anthropic IPO定价 11-17、纳斯达克上市 11-19、英伟达Q3财报 11-17、13F 集中披露 11-16——均在 11-16 当周，早于预读窗口 11-23~11-29
- FOMC 会议日历: query_fomc(lookback_days=60, lookahead_days=90) = 空（无会议数据，12月决议日期无法核验）
- 11-10 10年期拍卖双序列: query_calendar_events(country=US, days=15, importance=high,medium, lookback_days=7) = "Note Auction - High yield (10Y)" actual 5.02（前值5.3）与 "10 Year (Official)" actual 2.46（前值2.77）——两序列前值口径亦不同，疑似序列定义差异而非单纯数据矛盾
- query_raw_items(Fed OR 加息 OR PCE... /近14天无关键词全量) = NO_DATA（库中暂无该主题原始新闻，本轮无 raw item 引用与打分）
</parameter></function></tool_call>
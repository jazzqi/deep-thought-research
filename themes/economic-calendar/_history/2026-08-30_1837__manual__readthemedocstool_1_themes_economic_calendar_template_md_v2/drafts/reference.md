
## 交叉审查补充溯源（ackman，2026-08-30）

### 独立核验数据源
- G20 财长和央行行长会议: query_calendar_events(country=US, days=14, lookback=0, importance=high,medium) = 8/30 G20财长央行行长会议，贝森特或警告各国配合对伊经济制裁
- 韩国副总理取消赴美 G20 行程: query_raw_items(keyword="G20 OR 二十国集团 OR 财长央行")[id:192648] = 韩国副总理兼财经部长官具润哲临时取消赴美出席G20财长央行行长会议
- 苹果 CEO 换届: query_calendar_events(country=US, days=14, lookback=0, importance=high,medium) = 8/30 蒂姆·库克正式卸任苹果CEO，John Ternus接任
- 中国 7 月规上工业利润同比: query_calendar_events(country=CN, days=14, lookback=7, importance=high,medium) = 7月同比 11.2%（前值 15.1%）
- 美国新屋销售: query_calendar_events(country=US, days=14, lookback=7, importance=high) = 0.607（前值 0.628，预测 0.62），文档引用"−10.5% m/m"
- 美国消费者信心: query_calendar_events(country=US, days=14, lookback=7, importance=high) = 89.4（前值 90.8，预测 90.2），文档未覆盖
- 美国商品贸易逆差: query_calendar_events(country=US, days=14, lookback=7, importance=high) = −118.8B（前值 −101.41B），文档未覆盖
- Richmond Fed 制造业: query_calendar_events(country=US, days=14, lookback=7, importance=high) = 4.0（前值 5.0），文档未覆盖
- 中国建行延长房贷至40年: query_raw_items(keyword="房贷 OR housing loan")[id:192842] = 央行/金管局新规，个人住房贷款最长延至40年，文档未覆盖
- 加拿大对美200亿反制关税: 文档 §7 [新增] 提及 9/7 生效，无独立新闻源核验

### 非农共识一致性检查
- reference.md 主文 section: consensus ~+5.5万（路透，非日历工具返回）
- reference.md 接力补充溯源 section: +5.8万（路透，query_raw_items [id:192622]）
- 原稿正文: +5.8万（路透 [id:192622]）
- 矛盾：同一文件内 +5.5万 vs +5.8万不一致，需统一

### 东京 CPI 溯源
- 原稿引用 [id:东京CPI] 为虚构 ID，query_raw_items 无此条目
- 建议：从 query_calendar_events 或上周 recap 获取实际来源

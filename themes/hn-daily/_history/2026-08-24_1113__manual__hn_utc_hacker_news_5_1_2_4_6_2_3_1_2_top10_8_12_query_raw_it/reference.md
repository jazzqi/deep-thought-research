# 数据来源溯源

- Anthropic A/B 测试缩减 effort 档位: query_raw_items(source='hackernews', min_points=20)[id:135512] = Claude Code 2.1.237 起 high effort 读作 10/100，服务端 A/B 实验
- 本地 LLM 感觉更笨: query_raw_items(source='hackernews', min_points=20)[id:135524] = 量化/采样器/硬件指令集差异导致同一权重解码不同
- hdiutil 弃用: query_raw_items(source='hackernews', min_points=20)[id:135530] = macOS 27 弃用 hdiutil，改 diskutil image
- Moxie Scrap: query_raw_items(source='hackernews', min_points=20)[id:135521] = 2006 旧文被翻出，▲356 💬189
- Thinking in Python: query_raw_items(source='hackernews', min_points=20)[id:135522] = Bruce Eckel 新书，47 章，CC BY-NC-ND 4.0
- NetBSD and my life: query_raw_items(source='hackernews', min_points=20)[id:135531] = 2005 邮件，29 台 NetBSD 支撑 4800 用户
- 比利时王子: query_raw_items(source='hackernews', min_points=20)[id:135514] = DNA 检测证实王室私生子
- Figmimic: query_raw_items(source='hackernews', min_points=20)[id:135523] = bookmarklet 复制网页为 Figma 可编辑图层
- 正文抓取: fetch_url(forum.level1techs.com) = 本地 LLM 排障细节
- 正文抓取: fetch_url(lapcatsoftware.com) = hdiutil/diskutil 对比实测
- 正文抓取: fetch_url(twitter.com/argofowl) = A/B 测试细节
- 正文抓取: fetch_url(thinkinginpython.com) = 书籍目录
- 正文抓取: fetch_url(mail-index.netbsd.org) = NetBSD 用户来信
- 正文抓取: fetch_url(marcua.net) = Figmimic 功能与限制
- 未能抓取: fetch_url(xcancel.com/moxie) = ConnectError，Scrap 正文缺失

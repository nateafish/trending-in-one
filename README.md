# trending-in-one

> 本仓库基于上游项目 [huqi-pr/trending-in-one](https://github.com/huqi-pr/trending-in-one)
> 及其持续更新分支整理，补全了历史归档数据；内容由 GitHub Actions 自动抓取、归档并维护。

[![ci](https://github.com/nateafish/trending-in-one/actions/workflows/ci.yml/badge.svg)](https://github.com/nateafish/trending-in-one/actions/workflows/ci.yml)
[![license](https://img.shields.io/github/license/izukuuuu/trending-in-one)](https://github.com/nateafish/trending-in-one/blob/main/LICENSE)

今日头条热搜、知乎热搜榜、知乎热门话题、微博热搜榜；记录从 2020-11-29
日开始的热搜。每小时抓取一次数据，按天[归档](./archives)。知乎视频热榜已下线（2025-05
起停更），不再抓取，仅保留历史数据。

<!-- BEGIN ZHIHUCOOKIE -->

**知乎热榜 Cookie**：✅ 有效 ｜ 最近刷新：2026-08-07 13:14 ｜ 最近检测：2026-10-11 06:35:09

<!-- END ZHIHUCOOKIE -->

## 相关项目

- [知乎热门视频](https://github.com/justjavac/zhihu-trending-hot-video)
- [知乎热搜榜](https://github.com/justjavac/zhihu-trending-top-search)
- [知乎热门话题](https://github.com/justjavac/zhihu-trending-hot-questions)
- [微博热搜榜](https://github.com/justjavac/weibo-trending-hot-search)

## 知乎 Cookie 维护

知乎热榜接口自 2025-05 起要求登录态，抓取依赖有效的 `z_c0` 会话 cookie。cookie 保存在 GitHub Actions Secret
`ZHIHU_COOKIE` 中（不写入代码库）。本仓库每小时抓取时都会自动检测 cookie 有效性，并在此 README 顶部显示状态：

- `✅ 有效` —— 热榜数据正常抓取；
- `❌ 已失效` —— 需要重新扫码获取新 cookie。

**刷新步骤**（每次 cookie 失效时执行一次）：

```bash
# 1. 扫码登录并验证新 cookie
deno run -A scripts/refresh-zhihu-cookie.ts

# 2. 把新 cookie 更新到仓库 Secret
gh secret set ZHIHU_COOKIE -R nateafish/trending-in-one \
  --body "$(cat /tmp/zhihu_new_cookie.txt)"

# 3. 手动触发一次抓取，验证 README 顶部状态变为 ✅
gh workflow run "zhihu-questions update" -R nateafish/trending-in-one
```

首次使用需安装 playwright 浏览器：`npx playwright install chromium`。

## 今日头条热搜

<!-- BEGIN TOUTIAO -->
<!-- 最后更新时间 Sun Oct 11 2026 03:30:04 GMT+0800 (China Standard Time) -->

1. [乌方抛出全面无条件停火方案有何意图](https://so.toutiao.com/search?keyword=乌方抛出全面无条件停火方案有何意图)
1. [人社部：要把未参保人员找到动员参保](https://so.toutiao.com/search?keyword=人社部：要把未参保人员找到动员参保)
1. [中外游客“双向奔赴”活力涌动](https://so.toutiao.com/search?keyword=中外游客“双向奔赴”活力涌动)
1. [油价将于10月15日24时调整](https://so.toutiao.com/search?keyword=油价将于10月15日24时调整)
1. [郑钦文首进中网决赛](https://so.toutiao.com/search?keyword=郑钦文首进中网决赛)
1. [男性衰老时身体或会有4大变化](https://so.toutiao.com/search?keyword=男性衰老时身体或会有4大变化)
1. [男子河里捞出春秋编钟卖30万获刑5年](https://so.toutiao.com/search?keyword=男子河里捞出春秋编钟卖30万获刑5年)
1. [人社部：全面推进“退休预服务”](https://so.toutiao.com/search?keyword=人社部：全面推进“退休预服务”)
1. [郑钦文：中网就像第五个大满贯](https://so.toutiao.com/search?keyword=郑钦文：中网就像第五个大满贯)
1. [人社部：解决“有人没活干”的问题](https://so.toutiao.com/search?keyword=人社部：解决“有人没活干”的问题)
1. [社保卡有金卡？北京人社局：诈骗](https://so.toutiao.com/search?keyword=社保卡有金卡？北京人社局：诈骗)
1. [张雪机车葡萄牙站第1回合德比斯第6](https://so.toutiao.com/search?keyword=张雪机车葡萄牙站第1回合德比斯第6)
1. [医生：七成肝癌早期没症状](https://so.toutiao.com/search?keyword=医生：七成肝癌早期没症状)
1. [美国为何想要开直播处决一名死囚](https://so.toutiao.com/search?keyword=美国为何想要开直播处决一名死囚)
1. [巴拿马华人从51楼跑下来花10多分钟](https://so.toutiao.com/search?keyword=巴拿马华人从51楼跑下来花10多分钟)
1. [国防部：日本必须履行二战战败国义务](https://so.toutiao.com/search?keyword=国防部：日本必须履行二战战败国义务)
1. [长期这样吃饭全身炎症水平会上升](https://so.toutiao.com/search?keyword=长期这样吃饭全身炎症水平会上升)
1. [下周一A股要变盘吗](https://so.toutiao.com/search?keyword=下周一A股要变盘吗)
1. [为何外军愿花大量时间跟踪055大驱](https://so.toutiao.com/search?keyword=为何外军愿花大量时间跟踪055大驱)
1. [手脚发麻不是小毛病](https://so.toutiao.com/search?keyword=手脚发麻不是小毛病)
1. [人社部：新就业形态人员可按单参保](https://so.toutiao.com/search?keyword=人社部：新就业形态人员可按单参保)
1. [女子仅退款9斤蜜薯称有本事就来拿](https://so.toutiao.com/search?keyword=女子仅退款9斤蜜薯称有本事就来拿)
1. [王曼昱：决赛打佐藤瞳会很艰苦](https://so.toutiao.com/search?keyword=王曼昱：决赛打佐藤瞳会很艰苦)
1. [男子钓鱼“钓”到万元无人机带走](https://so.toutiao.com/search?keyword=男子钓鱼“钓”到万元无人机带走)
1. [谁在偷偷握紧油价定价权](https://so.toutiao.com/search?keyword=谁在偷偷握紧油价定价权)
1. [盛家把视后视帝包揽了](https://so.toutiao.com/search?keyword=盛家把视后视帝包揽了)
1. [王仁君是杨幂大学班长](https://so.toutiao.com/search?keyword=王仁君是杨幂大学班长)
1. [刘烨16岁儿子诺一近照曝光](https://so.toutiao.com/search?keyword=刘烨16岁儿子诺一近照曝光)
1. [苹果供应链公司：iPhone Duo加单30%](https://so.toutiao.com/search?keyword=苹果供应链公司：iPhone%20Duo加单30%)
1. [鲁比奥扬言瘫痪国际刑事法院运作能力](https://so.toutiao.com/search?keyword=鲁比奥扬言瘫痪国际刑事法院运作能力)
1. [人民日报评畸形饭圈：赛场不容戾气](https://so.toutiao.com/search?keyword=人民日报评畸形饭圈：赛场不容戾气)
1. [四部门拟禁止汽车配全隐藏式门把手](https://so.toutiao.com/search?keyword=四部门拟禁止汽车配全隐藏式门把手)
1. [村民自家宅基地发现古墓盗掘获刑15年](https://so.toutiao.com/search?keyword=村民自家宅基地发现古墓盗掘获刑15年)
1. [“面包刺客”卖不动了吗](https://so.toutiao.com/search?keyword=“面包刺客”卖不动了吗)
1. [杜特尔特被裁定适合受审意味什么](https://so.toutiao.com/search?keyword=杜特尔特被裁定适合受审意味什么)
1. [我国基本养老保险参保人数10.79亿人](https://so.toutiao.com/search?keyword=我国基本养老保险参保人数10.79亿人)
1. [“飞天奖”在坚守什么](https://so.toutiao.com/search?keyword=“飞天奖”在坚守什么)
1. [人社部：稳定国企等招录规模](https://so.toutiao.com/search?keyword=人社部：稳定国企等招录规模)
1. [乌将战火烧向俄导弹燃料厂与数据中心](https://so.toutiao.com/search?keyword=乌将战火烧向俄导弹燃料厂与数据中心)
1. [美俄达成柴油协议背后透露什么信息](https://so.toutiao.com/search?keyword=美俄达成柴油协议背后透露什么信息)
1. [媒体评《伟大的长征》：书写不朽信仰](https://so.toutiao.com/search?keyword=媒体评《伟大的长征》：书写不朽信仰)
1. [葡萄牙足协：对C罗停赛+调查](https://so.toutiao.com/search?keyword=葡萄牙足协：对C罗停赛+调查)
1. [我国将深入实施“新八级工”制度](https://so.toutiao.com/search?keyword=我国将深入实施“新八级工”制度)
1. [刘艳红已任广西党委组织部部长](https://so.toutiao.com/search?keyword=刘艳红已任广西党委组织部部长)
1. [武网签表出炉 郑钦文或再战萨巴伦卡](https://so.toutiao.com/search?keyword=武网签表出炉%20郑钦文或再战萨巴伦卡)
1. [人社部：社保关系转移全国通办](https://so.toutiao.com/search?keyword=人社部：社保关系转移全国通办)
1. [A股五大科技板块谁上涨逻辑更“硬”](https://so.toutiao.com/search?keyword=A股五大科技板块谁上涨逻辑更“硬”)
1. [李昊炎打进拉玛西亚生涯正式比赛首球](https://so.toutiao.com/search?keyword=李昊炎打进拉玛西亚生涯正式比赛首球)
1. [郑钦文成首位闯入中网决赛本土球员](https://so.toutiao.com/search?keyword=郑钦文成首位闯入中网决赛本土球员)
1. [新郎遭好友婚闹被砸鸡蛋泼酱油](https://so.toutiao.com/search?keyword=新郎遭好友婚闹被砸鸡蛋泼酱油)

<!-- END TOUTIAO -->

历史归档 [./archives/toutiao-search](./archives/toutiao-search)

## 知乎热搜榜

<!-- BEGIN ZHIHUSEARCH -->
<!-- 最后更新时间 Sun Oct 11 2026 05:37:00 GMT+0800 (China Standard Time) -->

1. [双汇被罚1.29亿](https://www.zhihu.com/search?q=%E5%8F%8C%E6%B1%87%E8%A2%AB%E7%BD%9A1.29%E4%BA%BF)
1. [警方通报王皓被聚集辱骂](https://www.zhihu.com/search?q=%E8%AD%A6%E6%96%B9%E9%80%9A%E6%8A%A5%E7%8E%8B%E7%9A%93%E8%A2%AB%E8%81%9A%E9%9B%86%E8%BE%B1%E9%AA%82)
1. [俄罗斯不明病因肺炎事件四种说法](https://www.zhihu.com/search?q=%E4%BF%84%E7%BD%97%E6%96%AF%E4%B8%8D%E6%98%8E%E7%97%85%E5%9B%A0%E8%82%BA%E7%82%8E%E4%BA%8B%E4%BB%B6%E5%9B%9B%E7%A7%8D%E8%AF%B4%E6%B3%95)
1. [林诗栋被撤销亚锦赛男单混双报名](https://www.zhihu.com/search?q=%E6%9E%97%E8%AF%97%E6%A0%8B%E8%A2%AB%E6%92%A4%E9%94%80%E4%BA%9A%E9%94%A6%E8%B5%9B%E7%94%B7%E5%8D%95%E6%B7%B7%E5%8F%8C%E6%8A%A5%E5%90%8D)
1. [711关闭印度全部门店](https://www.zhihu.com/search?q=711%E5%85%B3%E9%97%AD%E5%8D%B0%E5%BA%A6%E5%85%A8%E9%83%A8%E9%97%A8%E5%BA%97)
1. [俄解除不明原因肺炎防疫措施](https://www.zhihu.com/search?q=%E4%BF%84%E8%A7%A3%E9%99%A4%E4%B8%8D%E6%98%8E%E5%8E%9F%E5%9B%A0%E8%82%BA%E7%82%8E%E9%98%B2%E7%96%AB%E6%8E%AA%E6%96%BD)
1. [邵艾伦对话孙宇晨](https://www.zhihu.com/search?q=%E9%82%B5%E8%89%BE%E4%BC%A6%E5%AF%B9%E8%AF%9D%E5%AD%99%E5%AE%87%E6%99%A8)
1. [王仁君首获飞天奖视帝](https://www.zhihu.com/search?q=%E7%8E%8B%E4%BB%81%E5%90%9B%E9%A6%96%E8%8E%B7%E9%A3%9E%E5%A4%A9%E5%A5%96%E8%A7%86%E5%B8%9D)
1. [宋佳获飞天奖视后](https://www.zhihu.com/search?q=%E5%AE%8B%E4%BD%B3%E8%8E%B7%E9%A3%9E%E5%A4%A9%E5%A5%96%E8%A7%86%E5%90%8E)
1. [樊振东回归救不了国乒人才断档](https://www.zhihu.com/search?q=%E6%A8%8A%E6%8C%AF%E4%B8%9C%E5%9B%9E%E5%BD%92%E6%95%91%E4%B8%8D%E4%BA%86%E5%9B%BD%E4%B9%92%E4%BA%BA%E6%89%8D%E6%96%AD%E6%A1%A3)
1. [女子换支付方式付款被误会逃单](https://www.zhihu.com/search?q=%E5%A5%B3%E5%AD%90%E6%8D%A2%E6%94%AF%E4%BB%98%E6%96%B9%E5%BC%8F%E4%BB%98%E6%AC%BE%E8%A2%AB%E8%AF%AF%E4%BC%9A%E9%80%83%E5%8D%95)
1. [多家烘焙店下架超长蛋挞](https://www.zhihu.com/search?q=%E5%A4%9A%E5%AE%B6%E7%83%98%E7%84%99%E5%BA%97%E4%B8%8B%E6%9E%B6%E8%B6%85%E9%95%BF%E8%9B%8B%E6%8C%9E)
1. [郑钦文 2-0 梅尔滕斯](https://www.zhihu.com/search?q=%E9%83%91%E9%92%A6%E6%96%87%202-0%20%E6%A2%85%E5%B0%94%E6%BB%95%E6%96%AF)
1. [王曼昱4-1张本美和](https://www.zhihu.com/search?q=%E7%8E%8B%E6%9B%BC%E6%98%B14-1%E5%BC%A0%E6%9C%AC%E7%BE%8E%E5%92%8C)
1. [中国金花首进中网女单决赛](https://www.zhihu.com/search?q=%E4%B8%AD%E5%9B%BD%E9%87%91%E8%8A%B1%E9%A6%96%E8%BF%9B%E4%B8%AD%E7%BD%91%E5%A5%B3%E5%8D%95%E5%86%B3%E8%B5%9B)

<!-- END ZHIHUSEARCH -->

历史归档 [./archives/zhihu-search](./archives/zhihu-search)

## 知乎热门话题

<!-- BEGIN ZHIHUQUESTIONS -->
<!-- 最后更新时间 Sun Oct 11 2026 06:35:09 GMT+0800 (China Standard Time) -->

1. [日媒曝黑客黑掉软银旗下云平台后留下225封勒索信，结果运维找7小时没发现勒索信只是一味重启，如何看待？](https://www.zhihu.com/question/2092283931764552200)
1. [红果短剧为何让人着迷？](https://www.zhihu.com/question/2081873980173174300)
1. [如何看待5090将停产？](https://www.zhihu.com/question/2092286756028672000)
1. [女子称 38 元买榴莲，切开后发现里面都是假果肉，还塞着年糕和土豆，是真的吗？可以怎样维权？](https://www.zhihu.com/question/2092234755576001500)
1. [为什么不把香港元朗、屯门、北区划到深圳，既能帮助香港开发荒地，又能解决深圳的用地不足问题？](https://www.zhihu.com/question/2049776403307029800)
1. [买家花 15 元买蜜薯后「仅退款」，还称有本事就过来拿，商家驱车数百公里连夜取回，买家的行为算违法吗？](https://www.zhihu.com/question/2092050467320812800)
1. [男子在 ICU 抢救，母亲却取不出儿子存款救命，银行称家属须出具法定监护人身份证明，这规定合理吗？](https://www.zhihu.com/question/2092224091172201200)
1. [中网女单半决赛，郑钦文总比分2-0战胜梅尔滕斯，首次闯进中网决赛，如何评价本场比赛以及她的个人表现？](https://www.zhihu.com/question/2092297507661244000)
1. [国庆景区热度前十被小城包揽，这会成为一种旅游趋势吗？你会选择大城市出游还是小城呢？](https://www.zhihu.com/question/2090156101194839800)
1. [多家烘焙店陆续下架超长蛋挞，为啥网红小吃总难逃昙花一现的命运？有啥破局之法吗？](https://www.zhihu.com/question/2091945934384887300)
1. [美国国债已攀升至约 41 万亿美元规模，会带来哪些影响？财长称将推出财政整顿计划，可能有哪些手段？](https://www.zhihu.com/question/2092180406640685600)
1. [多家医院、卫生院暂停夜间门诊，为什么会这样？对患者夜间就诊影响有多大？](https://www.zhihu.com/question/2092161569975001600)
1. [两名内地女学生在澳门非法旅拍被捕，为什么属于非法务工？雇主和摄影师会面临什么处罚？](https://www.zhihu.com/question/2092196902880203300)
1. [为什么中国的影视行业至今都没有一个有普遍大众公信力的奖项？](https://www.zhihu.com/question/2070890086497874400)
1. [国乒调整亚锦赛名单，林诗栋不参加男单混双项目，梁靖崑不参加男单男团项目，如何评价新名单？](https://www.zhihu.com/question/2092277750874596000)
1. [如何评价邵艾伦对话孙宇晨4.5小时？](https://www.zhihu.com/question/2091813630790707200)
1. [根据《国家通用语言文字法》，在正式场合把“兆”当作“万亿”来使用是不是违法行为？](https://www.zhihu.com/question/1937838426146727400)
1. [顾客称在胖东来购物结账时发现多收 27.79 元，次日退还款项还额外补偿两百元，如何看待这一处理方式？](https://www.zhihu.com/question/2091845282501866500)
1. [在职场中，A承担了 80% 的工作量，B只做 20%，但B零失误。为什么最后奖金、升职全是干活少的B？](https://www.zhihu.com/question/2091907275392866300)
1. [潜伏为什么结局写这么残忍？](https://www.zhihu.com/question/2016650683198218500)
1. [有一个百思不得其解的问题，也是我迟迟不想换电车的原因，电车电池虚标这么严重为什么没有人打假？](https://www.zhihu.com/question/2090544879965419300)
1. [总感觉不喜欢现在的工作怎么办？辞职又怕找不到合适的？](https://www.zhihu.com/question/9115333903)
1. [家庭教育不到位的孩子，很难会优秀吗？](https://www.zhihu.com/question/9060552735)
1. [如果要选一位被贬谪的诗人跟着去体验一下贬谪生活，你会选谁?为什么?](https://www.zhihu.com/question/2087096149228501000)
1. [孩子爷爷奶奶不出钱也不出力，你会有意见吗？](https://www.zhihu.com/question/1990700492788088800)
1. [怎么系统建立计算机科学的知识体系，再逐步完善到实际开发？](https://www.zhihu.com/question/2089005964619944200)
1. [WTT 中国大满贯女单半决赛，王曼昱 4-1 战胜张本美和挺进决赛，如何评价本场比赛？](https://www.zhihu.com/question/2092297031662264800)
1. [1N （牛）的力量有多大？1500N 呢？](https://www.zhihu.com/question/2092046621265679400)
1. [刘欢是怎么做到一天音乐学院都没上过，就能在音乐方面有这么大的造诣的？](https://www.zhihu.com/question/2090980380291736800)
1. [贵州遵义一新郎婚礼当天就医输液后死亡，家属称输液区域监控未投入使用，公安已介入，哪些信息值得关注？](https://www.zhihu.com/question/2091881372683956700)
1. [为什么郭靖不告诉黄蓉自己有婚约？](https://www.zhihu.com/question/1985770857109422300)
1. [英特尔CEO陈立武称内存短缺明年或进一步恶化，CPU也缺货，内存、电力、散热都是基建瓶颈，如何解读？](https://www.zhihu.com/question/2083661446060234500)
1. [电影《神探之痕迹》有哪些细思极恐的细节？](https://www.zhihu.com/question/2089661309084344600)

<!-- END ZHIHUQUESTIONS -->

历史归档 [./archives/zhihu-questions](./archives/zhihu-questions)

## 知乎热门视频

> ⚠️ 知乎视频热榜已下线（2025-05 起停更），抓取已在 workflow 中停用；本节为历史数据。

<!-- BEGIN ZHIHUVIDEO -->
<!-- 最后更新时间 Tue May 06 2025 09:19:13 GMT+0800 (China Standard Time) -->

1. [赵心童夺得斯诺克世锦赛冠军，成为中国首位，也是亚洲首位斯诺克世锦赛冠军，如何评价他的比赛表现？](https://www.zhihu.com/question/1902560709012878096)
1. [2025 五一档票房 7.43 亿，不及去年同档期票房一半，这一现象原因是什么？](https://www.zhihu.com/question/1902835234510214480)
1. [南京明孝陵石兽遭涂鸦「到此一游」，景区称已进行修补保护，涉事游客可能出于什么心理？将受到哪些处罚？](https://www.zhihu.com/question/1902762657548821705)
1. [孩子幼儿园，早上起不来，是该强行拖起来，还是让她睡够了再去幼儿园？](https://www.zhihu.com/question/13172991603)
1. [阿诺德将在赛季结束后离开利物浦加盟皇家马德里，如何评价这一举措？](https://www.zhihu.com/question/1902785483890755051)
1. [如何看待阿维塔再回应网传「风阻系数造假」，称近期将根据国家专业机构实验室排期公开测试？](https://www.zhihu.com/question/1902316343816074282)
1. [SpaceX 星舰 S35 火箭在静态点火测试中发生爆炸，爆炸原因有哪些？](https://www.zhihu.com/question/1902415262592004400)
1. [我是行政，老板说不招保洁了，让我一个月打扫一次厕所和会议室，给我涨工资 500 元，我怎么回？](https://www.zhihu.com/question/1902315003505270826)
1. [五一假期结束了，如果真有「反方向的钟」，你最想把时间拨回到假期的哪一天？](https://www.zhihu.com/question/1902677957484443611)
1. [哪道菜一出现就知道是妈妈的「敷衍式做饭」？](https://www.zhihu.com/question/1899914369975957373)
1. [小米汽车将 SU7 新车定购页面中的「智驾」更名为「辅助驾驶」，这一调整是出于怎样的品牌定位考量？](https://www.zhihu.com/question/1902406018308211718)
1. [贵州游船侧翻致 10 死，当地称日常有执法检查，曾发天气预警，为何悲剧仍发生？暴露了哪些问题？](https://www.zhihu.com/question/1902679450086237352)
1. [DND 世界观下巨龙靠什么能活到成年?](https://www.zhihu.com/question/11292701270)
1. [孩子明明天天都在学习，可咋就不出成绩呢？](https://www.zhihu.com/question/1898247330764919030)
1. [你在热血传奇里面打到的最贵的东西是什么？](https://www.zhihu.com/question/33399354)
1. [学校为什么喜欢把食堂、宿舍等职能单位外包出去呢？](https://www.zhihu.com/question/1899419117401929649)
1. [历史上有哪些很冷的冷知识?](https://www.zhihu.com/question/1895916425392132635)
1. [日本的小学生上学、放学为什么不可以接送？](https://www.zhihu.com/question/5900994708)
1. [5 月是 2025 年牛市的起点吗？](https://www.zhihu.com/question/1898639747859079484)
1. [美国男子注射蛇毒 18 年血液产生抗体，蛇毒在血液中是怎么产生抗体的？他的抗体有哪些研究价值？](https://www.zhihu.com/question/1902414257561232264)
1. [巴菲特宣布年底退休，63 岁阿贝尔将接班，公司已囤积 3477 亿美元现金，哪些信息值得关注？](https://www.zhihu.com/question/1902313765539668566)
1. [湖北江陵一男子跑马拉松心脏骤停，30 秒急救捡回一命，反映出什么问题？普通人怎么判断身体条件是否合适？](https://www.zhihu.com/question/1902078766752170336)
1. [上班通勤在多久内可以接受啊？](https://www.zhihu.com/question/12996127786)
1. [怎样增加深度睡眠时间？](https://www.zhihu.com/question/23273243)
1. [孩子写作业不会，你教也听不懂，你会说孩子笨吗？](https://www.zhihu.com/question/1900219572537258288)
1. [吕布在三国正史里是不是第一猛将？](https://www.zhihu.com/question/605192875)
1. [金庸《笑傲江湖》中，同一本剑谱为什么采用两个命名？](https://www.zhihu.com/question/1896870169315353556)
1. [声音是怎么影响人的情绪的？](https://www.zhihu.com/question/1901017819027584504)
1. [《情深深雨濛濛》里方瑜为什么看上尔豪?](https://www.zhihu.com/question/663501446)
1. [为什么漫威要在《雷霆特攻队 *》里，让模仿大师两分钟暴毙？](https://www.zhihu.com/question/1901352690442831573)

<!-- END ZHIHUVIDEO -->

历史归档 [./archives/zhihu-video](./archives/zhihu-video)

## 微博热搜

<!-- BEGIN WEIBO -->
<!-- 最后更新时间 Sun Oct 11 2026 06:41:02 GMT+0800 (China Standard Time) -->

1. [总书记考察的长征故地](https://s.weibo.com//weibo?q=%23%E6%80%BB%E4%B9%A6%E8%AE%B0%E8%80%83%E5%AF%9F%E7%9A%84%E9%95%BF%E5%BE%81%E6%95%85%E5%9C%B0%23&Refer=new_time)
1. [泰国警方回应大概率已被转至缅甸](https://s.weibo.com//weibo?q=%23%E6%B3%B0%E5%9B%BD%E8%AD%A6%E6%96%B9%E5%9B%9E%E5%BA%94%E5%A4%A7%E6%A6%82%E7%8E%87%E5%B7%B2%E8%A2%AB%E8%BD%AC%E8%87%B3%E7%BC%85%E7%94%B8%23&t=31&band_rank=1&Refer=top)
1. [明知不该买房却想要自己的家](https://s.weibo.com//weibo?q=%E6%98%8E%E7%9F%A5%E4%B8%8D%E8%AF%A5%E4%B9%B0%E6%88%BF%E5%8D%B4%E6%83%B3%E8%A6%81%E8%87%AA%E5%B7%B1%E7%9A%84%E5%AE%B6&t=31&band_rank=2&Refer=top)
1. [以青春之我建强农之业](https://s.weibo.com//weibo?q=%23%E4%BB%A5%E9%9D%92%E6%98%A5%E4%B9%8B%E6%88%91%E5%BB%BA%E5%BC%BA%E5%86%9C%E4%B9%8B%E4%B8%9A%23&t=31&band_rank=3&Refer=top)
1. [梅艳芳骨灰被盗](https://s.weibo.com//weibo?q=%23%E6%A2%85%E8%89%B3%E8%8A%B3%E9%AA%A8%E7%81%B0%E8%A2%AB%E7%9B%97%23&t=31&band_rank=4&Refer=top)
1. [马斯克阴阳怪气向印度首富道歉](https://s.weibo.com//weibo?q=%E9%A9%AC%E6%96%AF%E5%85%8B%E9%98%B4%E9%98%B3%E6%80%AA%E6%B0%94%E5%90%91%E5%8D%B0%E5%BA%A6%E9%A6%96%E5%AF%8C%E9%81%93%E6%AD%89&t=31&band_rank=5&Refer=top)
1. [刘琳琳抖音账号被封](https://s.weibo.com//weibo?q=%23%E5%88%98%E7%90%B3%E7%90%B3%E6%8A%96%E9%9F%B3%E8%B4%A6%E5%8F%B7%E8%A2%AB%E5%B0%81%23&t=31&band_rank=6&Refer=top)
1. [四部门终结速成车乱象](https://s.weibo.com//weibo?q=%E5%9B%9B%E9%83%A8%E9%97%A8%E7%BB%88%E7%BB%93%E9%80%9F%E6%88%90%E8%BD%A6%E4%B9%B1%E8%B1%A1&t=31&band_rank=7&Refer=top)
1. [打一针让癌细胞生锈而死](https://s.weibo.com//weibo?q=%23%E6%89%93%E4%B8%80%E9%92%88%E8%AE%A9%E7%99%8C%E7%BB%86%E8%83%9E%E7%94%9F%E9%94%88%E8%80%8C%E6%AD%BB%23&t=31&band_rank=8&Refer=top)
1. [郑钦文创中网历史](https://s.weibo.com//weibo?q=%23%E9%83%91%E9%92%A6%E6%96%87%E5%88%9B%E4%B8%AD%E7%BD%91%E5%8E%86%E5%8F%B2%23&t=31&band_rank=9&Refer=top)
1. [香港近年多位名人骨灰被盗](https://s.weibo.com//weibo?q=%23%E9%A6%99%E6%B8%AF%E8%BF%91%E5%B9%B4%E5%A4%9A%E4%BD%8D%E5%90%8D%E4%BA%BA%E9%AA%A8%E7%81%B0%E8%A2%AB%E7%9B%97%23&t=31&band_rank=10&Refer=top)
1. [曝商家直接和刘琳琳终止合作](https://s.weibo.com//weibo?q=%23%E6%9B%9D%E5%95%86%E5%AE%B6%E7%9B%B4%E6%8E%A5%E5%92%8C%E5%88%98%E7%90%B3%E7%90%B3%E7%BB%88%E6%AD%A2%E5%90%88%E4%BD%9C%23&t=31&band_rank=11&Refer=top)
1. [花店老板说李勒优是真没钱](https://s.weibo.com//weibo?q=%23%E8%8A%B1%E5%BA%97%E8%80%81%E6%9D%BF%E8%AF%B4%E6%9D%8E%E5%8B%92%E4%BC%98%E6%98%AF%E7%9C%9F%E6%B2%A1%E9%92%B1%23&t=31&band_rank=12&Refer=top)
1. [男婴出生不到两天转入新生儿科后死亡](https://s.weibo.com//weibo?q=%23%E7%94%B7%E5%A9%B4%E5%87%BA%E7%94%9F%E4%B8%8D%E5%88%B0%E4%B8%A4%E5%A4%A9%E8%BD%AC%E5%85%A5%E6%96%B0%E7%94%9F%E5%84%BF%E7%A7%91%E5%90%8E%E6%AD%BB%E4%BA%A1%23&t=31&band_rank=13&Refer=top)
1. [AI把数学干废了](https://s.weibo.com//weibo?q=AI%E6%8A%8A%E6%95%B0%E5%AD%A6%E5%B9%B2%E5%BA%9F%E4%BA%86&t=31&band_rank=14&Refer=top)
1. [怪不得张国立在娱乐圈地位这么高](https://s.weibo.com//weibo?q=%23%E6%80%AA%E4%B8%8D%E5%BE%97%E5%BC%A0%E5%9B%BD%E7%AB%8B%E5%9C%A8%E5%A8%B1%E4%B9%90%E5%9C%88%E5%9C%B0%E4%BD%8D%E8%BF%99%E4%B9%88%E9%AB%98%23&t=31&band_rank=15&Refer=top)
1. [曼联1比1热刺](https://s.weibo.com//weibo?q=%E6%9B%BC%E8%81%941%E6%AF%941%E7%83%AD%E5%88%BA&t=31&band_rank=16&Refer=top)
1. [管泽元回应BLG](https://s.weibo.com//weibo?q=%23%E7%AE%A1%E6%B3%BD%E5%85%83%E5%9B%9E%E5%BA%94BLG%23&t=31&band_rank=17&Refer=top)
1. [崔晋说李勒优的钱都拿去买车开店](https://s.weibo.com//weibo?q=%23%E5%B4%94%E6%99%8B%E8%AF%B4%E6%9D%8E%E5%8B%92%E4%BC%98%E7%9A%84%E9%92%B1%E9%83%BD%E6%8B%BF%E5%8E%BB%E4%B9%B0%E8%BD%A6%E5%BC%80%E5%BA%97%23&t=31&band_rank=18&Refer=top)
1. [郑钦文解释为何提醒观众](https://s.weibo.com//weibo?q=%23%E9%83%91%E9%92%A6%E6%96%87%E8%A7%A3%E9%87%8A%E4%B8%BA%E4%BD%95%E6%8F%90%E9%86%92%E8%A7%82%E4%BC%97%23&t=31&band_rank=19&Refer=top)
1. [内娱的神之八秒](https://s.weibo.com//weibo?q=%E5%86%85%E5%A8%B1%E7%9A%84%E7%A5%9E%E4%B9%8B%E5%85%AB%E7%A7%92&t=31&band_rank=20&Refer=top)
1. [嫁人也要嫁舍得开灯的家庭](https://s.weibo.com//weibo?q=%E5%AB%81%E4%BA%BA%E4%B9%9F%E8%A6%81%E5%AB%81%E8%88%8D%E5%BE%97%E5%BC%80%E7%81%AF%E7%9A%84%E5%AE%B6%E5%BA%AD&t=31&band_rank=21&Refer=top)
1. [晒太阳补维D最好选这个时段](https://s.weibo.com//weibo?q=%23%E6%99%92%E5%A4%AA%E9%98%B3%E8%A1%A5%E7%BB%B4D%E6%9C%80%E5%A5%BD%E9%80%89%E8%BF%99%E4%B8%AA%E6%97%B6%E6%AE%B5%23&t=31&band_rank=22&Refer=top)
1. [iPhone标准版越来越值得等了吗](https://s.weibo.com//weibo?q=%23iPhone%E6%A0%87%E5%87%86%E7%89%88%E8%B6%8A%E6%9D%A5%E8%B6%8A%E5%80%BC%E5%BE%97%E7%AD%89%E4%BA%86%E5%90%97%23&t=31&band_rank=23&Refer=top)
1. [王楚钦孙颖莎林诗栋梁靖崑均伤病](https://s.weibo.com//weibo?q=%23%E7%8E%8B%E6%A5%9A%E9%92%A6%E5%AD%99%E9%A2%96%E8%8E%8E%E6%9E%97%E8%AF%97%E6%A0%8B%E6%A2%81%E9%9D%96%E5%B4%91%E5%9D%87%E4%BC%A4%E7%97%85%23&t=31&band_rank=24&Refer=top)
1. [云旗跳了神之八秒](https://s.weibo.com//weibo?q=%23%E4%BA%91%E6%97%97%E8%B7%B3%E4%BA%86%E7%A5%9E%E4%B9%8B%E5%85%AB%E7%A7%92%23&t=31&band_rank=25&Refer=top)
1. [国内景区审美降级](https://s.weibo.com//weibo?q=%E5%9B%BD%E5%86%85%E6%99%AF%E5%8C%BA%E5%AE%A1%E7%BE%8E%E9%99%8D%E7%BA%A7&t=31&band_rank=26&Refer=top)
1. [恋人](https://s.weibo.com//weibo?q=%E6%81%8B%E4%BA%BA&t=31&band_rank=27&Refer=top)
1. [郑钦文说中网像第5个大满贯](https://s.weibo.com//weibo?q=%23%E9%83%91%E9%92%A6%E6%96%87%E8%AF%B4%E4%B8%AD%E7%BD%91%E5%83%8F%E7%AC%AC5%E4%B8%AA%E5%A4%A7%E6%BB%A1%E8%B4%AF%23&t=31&band_rank=28&Refer=top)
1. [郑钦文击败13号种子梅尔滕斯](https://s.weibo.com//weibo?q=%23%E9%83%91%E9%92%A6%E6%96%87%E5%87%BB%E8%B4%A513%E5%8F%B7%E7%A7%8D%E5%AD%90%E6%A2%85%E5%B0%94%E6%BB%95%E6%96%AF%23&t=31&band_rank=29&Refer=top)
1. [店员也坐上电动车把我笑死](https://s.weibo.com//weibo?q=%E5%BA%97%E5%91%98%E4%B9%9F%E5%9D%90%E4%B8%8A%E7%94%B5%E5%8A%A8%E8%BD%A6%E6%8A%8A%E6%88%91%E7%AC%91%E6%AD%BB&t=31&band_rank=30&Refer=top)
1. [老一辈的书是教真东西啊](https://s.weibo.com//weibo?q=%E8%80%81%E4%B8%80%E8%BE%88%E7%9A%84%E4%B9%A6%E6%98%AF%E6%95%99%E7%9C%9F%E4%B8%9C%E8%A5%BF%E5%95%8A&t=31&band_rank=31&Refer=top)
1. [女生一定要学会藏锋](https://s.weibo.com//weibo?q=%E5%A5%B3%E7%94%9F%E4%B8%80%E5%AE%9A%E8%A6%81%E5%AD%A6%E4%BC%9A%E8%97%8F%E9%94%8B&t=31&band_rank=32&Refer=top)
1. [店员们误把保姆认成财阀夫人](https://s.weibo.com//weibo?q=%23%E5%BA%97%E5%91%98%E4%BB%AC%E8%AF%AF%E6%8A%8A%E4%BF%9D%E5%A7%86%E8%AE%A4%E6%88%90%E8%B4%A2%E9%98%80%E5%A4%AB%E4%BA%BA%23&t=31&band_rank=33&Refer=top)
1. [郑钦文谈决赛对手安德列娃](https://s.weibo.com//weibo?q=%23%E9%83%91%E9%92%A6%E6%96%87%E8%B0%88%E5%86%B3%E8%B5%9B%E5%AF%B9%E6%89%8B%E5%AE%89%E5%BE%B7%E5%88%97%E5%A8%83%23&t=31&band_rank=34&Refer=top)
1. [郑钦文说排名100多让我放下骄傲](https://s.weibo.com//weibo?q=%23%E9%83%91%E9%92%A6%E6%96%87%E8%AF%B4%E6%8E%92%E5%90%8D100%E5%A4%9A%E8%AE%A9%E6%88%91%E6%94%BE%E4%B8%8B%E9%AA%84%E5%82%B2%23&t=31&band_rank=35&Refer=top)
1. [华为整体成本涨了1400元](https://s.weibo.com//weibo?q=%E5%8D%8E%E4%B8%BA%E6%95%B4%E4%BD%93%E6%88%90%E6%9C%AC%E6%B6%A8%E4%BA%861400%E5%85%83&t=31&band_rank=36&Refer=top)
1. [餐厅里全程站着的妈妈](https://s.weibo.com//weibo?q=%E9%A4%90%E5%8E%85%E9%87%8C%E5%85%A8%E7%A8%8B%E7%AB%99%E7%9D%80%E7%9A%84%E5%A6%88%E5%A6%88&t=31&band_rank=37&Refer=top)
1. [2026中网](https://s.weibo.com//weibo?q=2026%E4%B8%AD%E7%BD%91&t=31&band_rank=38&Refer=top)
1. [四川妹子打麻将悟道了](https://s.weibo.com//weibo?q=%E5%9B%9B%E5%B7%9D%E5%A6%B9%E5%AD%90%E6%89%93%E9%BA%BB%E5%B0%86%E6%82%9F%E9%81%93%E4%BA%86&t=31&band_rank=39&Refer=top)
1. [小姨对李勒优说的话](https://s.weibo.com//weibo?q=%23%E5%B0%8F%E5%A7%A8%E5%AF%B9%E6%9D%8E%E5%8B%92%E4%BC%98%E8%AF%B4%E7%9A%84%E8%AF%9D%23&t=31&band_rank=40&Refer=top)
1. [郑钦文将迎战安德列娃](https://s.weibo.com//weibo?q=%23%E9%83%91%E9%92%A6%E6%96%87%E5%B0%86%E8%BF%8E%E6%88%98%E5%AE%89%E5%BE%B7%E5%88%97%E5%A8%83%23&t=31&band_rank=41&Refer=top)
1. [爸爸带儿子打卡清华神对话](https://s.weibo.com//weibo?q=%E7%88%B8%E7%88%B8%E5%B8%A6%E5%84%BF%E5%AD%90%E6%89%93%E5%8D%A1%E6%B8%85%E5%8D%8E%E7%A5%9E%E5%AF%B9%E8%AF%9D&t=31&band_rank=42&Refer=top)
1. [葡萄牙足协公布C罗处罚结果](https://s.weibo.com//weibo?q=%23%E8%91%A1%E8%90%84%E7%89%99%E8%B6%B3%E5%8D%8F%E5%85%AC%E5%B8%83C%E7%BD%97%E5%A4%84%E7%BD%9A%E7%BB%93%E6%9E%9C%23&t=31&band_rank=43&Refer=top)
1. [黄磊二女儿和黄磊一模一样](https://s.weibo.com//weibo?q=%E9%BB%84%E7%A3%8A%E4%BA%8C%E5%A5%B3%E5%84%BF%E5%92%8C%E9%BB%84%E7%A3%8A%E4%B8%80%E6%A8%A1%E4%B8%80%E6%A0%B7&t=31&band_rank=44&Refer=top)
1. [李现祝郑钦文中网决赛加油](https://s.weibo.com//weibo?q=%23%E6%9D%8E%E7%8E%B0%E7%A5%9D%E9%83%91%E9%92%A6%E6%96%87%E4%B8%AD%E7%BD%91%E5%86%B3%E8%B5%9B%E5%8A%A0%E6%B2%B9%23&t=31&band_rank=45&Refer=top)
1. [日本公司抢应届生涨薪四成](https://s.weibo.com//weibo?q=%E6%97%A5%E6%9C%AC%E5%85%AC%E5%8F%B8%E6%8A%A2%E5%BA%94%E5%B1%8A%E7%94%9F%E6%B6%A8%E8%96%AA%E5%9B%9B%E6%88%90&t=31&band_rank=46&Refer=top)
1. [葫芦爷爷宣布停止与游客互动](https://s.weibo.com//weibo?q=%23%E8%91%AB%E8%8A%A6%E7%88%B7%E7%88%B7%E5%AE%A3%E5%B8%83%E5%81%9C%E6%AD%A2%E4%B8%8E%E6%B8%B8%E5%AE%A2%E4%BA%92%E5%8A%A8%23&t=31&band_rank=47&Refer=top)
1. [员工拒绝晚上六点至八点加班被辞退](https://s.weibo.com//weibo?q=%23%E5%91%98%E5%B7%A5%E6%8B%92%E7%BB%9D%E6%99%9A%E4%B8%8A%E5%85%AD%E7%82%B9%E8%87%B3%E5%85%AB%E7%82%B9%E5%8A%A0%E7%8F%AD%E8%A2%AB%E8%BE%9E%E9%80%80%23&t=31&band_rank=48&Refer=top)
1. [无可替代](https://s.weibo.com//weibo?q=%E6%97%A0%E5%8F%AF%E6%9B%BF%E4%BB%A3&t=31&band_rank=49&Refer=top)
1. [郑钦文排名](https://s.weibo.com//weibo?q=%E9%83%91%E9%92%A6%E6%96%87%E6%8E%92%E5%90%8D&t=31&band_rank=50&Refer=top)
1. [四部门终结速成车乱象](https://s.weibo.com//weibo?q=%E5%9B%9B%E9%83%A8%E9%97%A8%E7%BB%88%E7%BB%93%E9%80%9F%E6%88%90%E8%BD%A6%E4%B9%B1%E8%B1%A1&t=31&band_rank=5&Refer=top)
1. [崔晋说李勒优的钱都拿去买车开店](https://s.weibo.com//weibo?q=%23%E5%B4%94%E6%99%8B%E8%AF%B4%E6%9D%8E%E5%8B%92%E4%BC%98%E7%9A%84%E9%92%B1%E9%83%BD%E6%8B%BF%E5%8E%BB%E4%B9%B0%E8%BD%A6%E5%BC%80%E5%BA%97%23&t=31&band_rank=7&Refer=top)
1. [恋人](https://s.weibo.com//weibo?q=%E6%81%8B%E4%BA%BA&t=31&band_rank=8&Refer=top)
1. [打一针让癌细胞生锈而死](https://s.weibo.com//weibo?q=%23%E6%89%93%E4%B8%80%E9%92%88%E8%AE%A9%E7%99%8C%E7%BB%86%E8%83%9E%E7%94%9F%E9%94%88%E8%80%8C%E6%AD%BB%23&t=31&band_rank=9&Refer=top)
1. [黄磊二女儿和黄磊一模一样](https://s.weibo.com//weibo?q=%E9%BB%84%E7%A3%8A%E4%BA%8C%E5%A5%B3%E5%84%BF%E5%92%8C%E9%BB%84%E7%A3%8A%E4%B8%80%E6%A8%A1%E4%B8%80%E6%A0%B7&t=31&band_rank=11&Refer=top)
1. [曝商家直接和刘琳琳终止合作](https://s.weibo.com//weibo?q=%23%E6%9B%9D%E5%95%86%E5%AE%B6%E7%9B%B4%E6%8E%A5%E5%92%8C%E5%88%98%E7%90%B3%E7%90%B3%E7%BB%88%E6%AD%A2%E5%90%88%E4%BD%9C%23&t=31&band_rank=12&Refer=top)
1. [花店老板说李勒优是真没钱](https://s.weibo.com//weibo?q=%23%E8%8A%B1%E5%BA%97%E8%80%81%E6%9D%BF%E8%AF%B4%E6%9D%8E%E5%8B%92%E4%BC%98%E6%98%AF%E7%9C%9F%E6%B2%A1%E9%92%B1%23&t=31&band_rank=13&Refer=top)
1. [小姨对李勒优说的话](https://s.weibo.com//weibo?q=%23%E5%B0%8F%E5%A7%A8%E5%AF%B9%E6%9D%8E%E5%8B%92%E4%BC%98%E8%AF%B4%E7%9A%84%E8%AF%9D%23&t=31&band_rank=14&Refer=top)
1. [葫芦爷爷宣布停止与游客互动](https://s.weibo.com//weibo?q=%23%E8%91%AB%E8%8A%A6%E7%88%B7%E7%88%B7%E5%AE%A3%E5%B8%83%E5%81%9C%E6%AD%A2%E4%B8%8E%E6%B8%B8%E5%AE%A2%E4%BA%92%E5%8A%A8%23&t=31&band_rank=15&Refer=top)
1. [郑钦文创中网历史](https://s.weibo.com//weibo?q=%23%E9%83%91%E9%92%A6%E6%96%87%E5%88%9B%E4%B8%AD%E7%BD%91%E5%8E%86%E5%8F%B2%23&t=31&band_rank=16&Refer=top)
1. [虞书欣成内娱首位太空应援艺人](https://s.weibo.com//weibo?q=%23%E8%99%9E%E4%B9%A6%E6%AC%A3%E6%88%90%E5%86%85%E5%A8%B1%E9%A6%96%E4%BD%8D%E5%A4%AA%E7%A9%BA%E5%BA%94%E6%8F%B4%E8%89%BA%E4%BA%BA%23&t=31&band_rank=17&Refer=top)
1. [郑钦文解释为何提醒观众](https://s.weibo.com//weibo?q=%23%E9%83%91%E9%92%A6%E6%96%87%E8%A7%A3%E9%87%8A%E4%B8%BA%E4%BD%95%E6%8F%90%E9%86%92%E8%A7%82%E4%BC%97%23&t=31&band_rank=18&Refer=top)
1. [内娱的神之八秒](https://s.weibo.com//weibo?q=%E5%86%85%E5%A8%B1%E7%9A%84%E7%A5%9E%E4%B9%8B%E5%85%AB%E7%A7%92&t=31&band_rank=19&Refer=top)
1. [葡萄牙足协公布C罗处罚结果](https://s.weibo.com//weibo?q=%23%E8%91%A1%E8%90%84%E7%89%99%E8%B6%B3%E5%8D%8F%E5%85%AC%E5%B8%83C%E7%BD%97%E5%A4%84%E7%BD%9A%E7%BB%93%E6%9E%9C%23&t=31&band_rank=20&Refer=top)
1. [Deft NS](https://s.weibo.com//weibo?q=Deft%20NS&t=31&band_rank=21&Refer=top)
1. [姐姐这分手速度引起舒适](https://s.weibo.com//weibo?q=%E5%A7%90%E5%A7%90%E8%BF%99%E5%88%86%E6%89%8B%E9%80%9F%E5%BA%A6%E5%BC%95%E8%B5%B7%E8%88%92%E9%80%82&t=31&band_rank=22&Refer=top)
1. [云旗跳了神之八秒](https://s.weibo.com//weibo?q=%23%E4%BA%91%E6%97%97%E8%B7%B3%E4%BA%86%E7%A5%9E%E4%B9%8B%E5%85%AB%E7%A7%92%23&t=31&band_rank=23&Refer=top)
1. [国内景区审美降级](https://s.weibo.com//weibo?q=%E5%9B%BD%E5%86%85%E6%99%AF%E5%8C%BA%E5%AE%A1%E7%BE%8E%E9%99%8D%E7%BA%A7&t=31&band_rank=24&Refer=top)
1. [王楚钦孙颖莎林诗栋梁靖崑均伤病](https://s.weibo.com//weibo?q=%23%E7%8E%8B%E6%A5%9A%E9%92%A6%E5%AD%99%E9%A2%96%E8%8E%8E%E6%9E%97%E8%AF%97%E6%A0%8B%E6%A2%81%E9%9D%96%E5%B4%91%E5%9D%87%E4%BC%A4%E7%97%85%23&t=31&band_rank=25&Refer=top)
1. [店员也坐上电动车把我笑死](https://s.weibo.com//weibo?q=%E5%BA%97%E5%91%98%E4%B9%9F%E5%9D%90%E4%B8%8A%E7%94%B5%E5%8A%A8%E8%BD%A6%E6%8A%8A%E6%88%91%E7%AC%91%E6%AD%BB&t=31&band_rank=26&Refer=top)
1. [男子805万买玉璧鉴定仅值6100元](https://s.weibo.com//weibo?q=%23%E7%94%B7%E5%AD%90805%E4%B8%87%E4%B9%B0%E7%8E%89%E7%92%A7%E9%89%B4%E5%AE%9A%E4%BB%85%E5%80%BC6100%E5%85%83%23&t=31&band_rank=27&Refer=top)
1. [王楚然王安宇的cp感](https://s.weibo.com//weibo?q=%23%E7%8E%8B%E6%A5%9A%E7%84%B6%E7%8E%8B%E5%AE%89%E5%AE%87%E7%9A%84cp%E6%84%9F%23&t=31&band_rank=28&Refer=top)
1. [鼓励灵活就业人员参加职工养老保险](https://s.weibo.com//weibo?q=%23%E9%BC%93%E5%8A%B1%E7%81%B5%E6%B4%BB%E5%B0%B1%E4%B8%9A%E4%BA%BA%E5%91%98%E5%8F%82%E5%8A%A0%E8%81%8C%E5%B7%A5%E5%85%BB%E8%80%81%E4%BF%9D%E9%99%A9%23&t=31&band_rank=29&Refer=top)
1. [女子癌症终末期的最后一个月](https://s.weibo.com//weibo?q=%23%E5%A5%B3%E5%AD%90%E7%99%8C%E7%97%87%E7%BB%88%E6%9C%AB%E6%9C%9F%E7%9A%84%E6%9C%80%E5%90%8E%E4%B8%80%E4%B8%AA%E6%9C%88%23&t=31&band_rank=30&Refer=top)
1. [嫁人也要嫁舍得开灯的家庭](https://s.weibo.com//weibo?q=%E5%AB%81%E4%BA%BA%E4%B9%9F%E8%A6%81%E5%AB%81%E8%88%8D%E5%BE%97%E5%BC%80%E7%81%AF%E7%9A%84%E5%AE%B6%E5%BA%AD&t=31&band_rank=31&Refer=top)
1. [马斯克阴阳怪气向印度首富道歉](https://s.weibo.com//weibo?q=%E9%A9%AC%E6%96%AF%E5%85%8B%E9%98%B4%E9%98%B3%E6%80%AA%E6%B0%94%E5%90%91%E5%8D%B0%E5%BA%A6%E9%A6%96%E5%AF%8C%E9%81%93%E6%AD%89&t=31&band_rank=32&Refer=top)
1. [怪不得张国立在娱乐圈地位这么高](https://s.weibo.com//weibo?q=%23%E6%80%AA%E4%B8%8D%E5%BE%97%E5%BC%A0%E5%9B%BD%E7%AB%8B%E5%9C%A8%E5%A8%B1%E4%B9%90%E5%9C%88%E5%9C%B0%E4%BD%8D%E8%BF%99%E4%B9%88%E9%AB%98%23&t=31&band_rank=33&Refer=top)
1. [演员赵奕欢上恋综了](https://s.weibo.com//weibo?q=%23%E6%BC%94%E5%91%98%E8%B5%B5%E5%A5%95%E6%AC%A2%E4%B8%8A%E6%81%8B%E7%BB%BC%E4%BA%86%23&t=31&band_rank=34&Refer=top)
1. [郑钦文谈决赛对手安德列娃](https://s.weibo.com//weibo?q=%23%E9%83%91%E9%92%A6%E6%96%87%E8%B0%88%E5%86%B3%E8%B5%9B%E5%AF%B9%E6%89%8B%E5%AE%89%E5%BE%B7%E5%88%97%E5%A8%83%23&t=31&band_rank=35&Refer=top)
1. [餐厅里全程站着的妈妈](https://s.weibo.com//weibo?q=%E9%A4%90%E5%8E%85%E9%87%8C%E5%85%A8%E7%A8%8B%E7%AB%99%E7%9D%80%E7%9A%84%E5%A6%88%E5%A6%88&t=31&band_rank=36&Refer=top)
1. [林依晨说想和邓为演夫妻](https://s.weibo.com//weibo?q=%23%E6%9E%97%E4%BE%9D%E6%99%A8%E8%AF%B4%E6%83%B3%E5%92%8C%E9%82%93%E4%B8%BA%E6%BC%94%E5%A4%AB%E5%A6%BB%23&t=31&band_rank=37&Refer=top)
1. [皖皖年总首个五杀](https://s.weibo.com//weibo?q=%23%E7%9A%96%E7%9A%96%E5%B9%B4%E6%80%BB%E9%A6%96%E4%B8%AA%E4%BA%94%E6%9D%80%23&t=31&band_rank=38&Refer=top)
1. [管泽元回应BLG](https://s.weibo.com//weibo?q=%23%E7%AE%A1%E6%B3%BD%E5%85%83%E5%9B%9E%E5%BA%94BLG%23&t=31&band_rank=39&Refer=top)
1. [王楚然下沉平台口碑](https://s.weibo.com//weibo?q=%23%E7%8E%8B%E6%A5%9A%E7%84%B6%E4%B8%8B%E6%B2%89%E5%B9%B3%E5%8F%B0%E5%8F%A3%E7%A2%91%23&t=31&band_rank=40&Refer=top)
1. [郑钦文说排名100多让我放下骄傲](https://s.weibo.com//weibo?q=%23%E9%83%91%E9%92%A6%E6%96%87%E8%AF%B4%E6%8E%92%E5%90%8D100%E5%A4%9A%E8%AE%A9%E6%88%91%E6%94%BE%E4%B8%8B%E9%AA%84%E5%82%B2%23&t=31&band_rank=41&Refer=top)
1. [四川妹子打麻将悟道了](https://s.weibo.com//weibo?q=%E5%9B%9B%E5%B7%9D%E5%A6%B9%E5%AD%90%E6%89%93%E9%BA%BB%E5%B0%86%E6%82%9F%E9%81%93%E4%BA%86&t=31&band_rank=42&Refer=top)
1. [日本公司抢应届生涨薪四成](https://s.weibo.com//weibo?q=%E6%97%A5%E6%9C%AC%E5%85%AC%E5%8F%B8%E6%8A%A2%E5%BA%94%E5%B1%8A%E7%94%9F%E6%B6%A8%E8%96%AA%E5%9B%9B%E6%88%90&t=31&band_rank=43&Refer=top)
1. [店员们误把保姆认成财阀夫人](https://s.weibo.com//weibo?q=%23%E5%BA%97%E5%91%98%E4%BB%AC%E8%AF%AF%E6%8A%8A%E4%BF%9D%E5%A7%86%E8%AE%A4%E6%88%90%E8%B4%A2%E9%98%80%E5%A4%AB%E4%BA%BA%23&t=31&band_rank=44&Refer=top)
1. [AI把数学干废了](https://s.weibo.com//weibo?q=AI%E6%8A%8A%E6%95%B0%E5%AD%A6%E5%B9%B2%E5%BA%9F%E4%BA%86&t=31&band_rank=45&Refer=top)
1. [华为整体成本涨了1400元](https://s.weibo.com//weibo?q=%E5%8D%8E%E4%B8%BA%E6%95%B4%E4%BD%93%E6%88%90%E6%9C%AC%E6%B6%A8%E4%BA%861400%E5%85%83&t=31&band_rank=46&Refer=top)
1. [贺嘉述生日发文](https://s.weibo.com//weibo?q=%E8%B4%BA%E5%98%89%E8%BF%B0%E7%94%9F%E6%97%A5%E5%8F%91%E6%96%87&t=31&band_rank=47&Refer=top)
1. [2026中网](https://s.weibo.com//weibo?q=2026%E4%B8%AD%E7%BD%91&t=31&band_rank=48&Refer=top)
1. [曝Deft复出](https://s.weibo.com//weibo?q=%23%E6%9B%9DDeft%E5%A4%8D%E5%87%BA%23&t=31&band_rank=49&Refer=top)
1. [郑钦文重现神兵小将庆祝动作](https://s.weibo.com//weibo?q=%23%E9%83%91%E9%92%A6%E6%96%87%E9%87%8D%E7%8E%B0%E7%A5%9E%E5%85%B5%E5%B0%8F%E5%B0%86%E5%BA%86%E7%A5%9D%E5%8A%A8%E4%BD%9C%23&t=31&band_rank=50&Refer=top)

<!-- END WEIBO -->

历史归档 [./archives/weibo-search](./archives/weibo-search)

## License

[trending-in-one/](https://github.com/cxyfreedom/trending-in-one) 的源码使用 MIT License 发布。具体内容请查看
[LICENSE](./LICENSE) 文件。

# trending-in-one

> 本仓库基于上游项目 [huqi-pr/trending-in-one](https://github.com/huqi-pr/trending-in-one)
> 及其持续更新分支整理，补全了历史归档数据；内容由 GitHub Actions 自动抓取、归档并维护。

[![ci](https://github.com/nateafish/trending-in-one/actions/workflows/ci.yml/badge.svg)](https://github.com/nateafish/trending-in-one/actions/workflows/ci.yml)
[![license](https://img.shields.io/github/license/izukuuuu/trending-in-one)](https://github.com/nateafish/trending-in-one/blob/main/LICENSE)

今日头条热搜、知乎热搜榜、知乎热门话题、微博热搜榜；记录从 2020-11-29
日开始的热搜。每小时抓取一次数据，按天[归档](./archives)。知乎视频热榜已下线（2025-05
起停更），不再抓取，仅保留历史数据。

<!-- BEGIN ZHIHUCOOKIE -->

**知乎热榜 Cookie**：✅ 有效 ｜ 最近刷新：2026-08-07 13:14 ｜ 最近检测：2026-09-13 06:20:29

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
<!-- 最后更新时间 Sun Sep 13 2026 07:18:59 GMT+0800 (China Standard Time) -->

1. [中国将于2027年接任金砖主席国](https://so.toutiao.com/search?keyword=中国将于2027年接任金砖主席国)
1. [男生去年考上北大放弃今年又考进北大](https://so.toutiao.com/search?keyword=男生去年考上北大放弃今年又考进北大)
1. [看懂中国贸易出海新模式](https://so.toutiao.com/search?keyword=看懂中国贸易出海新模式)
1. [一支拖鞋军正在改写中东格局](https://so.toutiao.com/search?keyword=一支拖鞋军正在改写中东格局)
1. [iPhone 18 Pro系列开售秒售罄](https://so.toutiao.com/search?keyword=iPhone%2018%20Pro系列开售秒售罄)
1. [超级厄尔尼诺来袭中国将面临什么](https://so.toutiao.com/search?keyword=超级厄尔尼诺来袭中国将面临什么)
1. [莫迪会见普京称愿支持俄乌和平努力](https://so.toutiao.com/search?keyword=莫迪会见普京称愿支持俄乌和平努力)
1. [雷军为首批小米澎程车主开车门](https://so.toutiao.com/search?keyword=雷军为首批小米澎程车主开车门)
1. [硕士因第一学历是专科被大厂拒之门外](https://so.toutiao.com/search?keyword=硕士因第一学历是专科被大厂拒之门外)
1. [莱巴金娜2-1萨巴伦卡首夺美网冠军](https://so.toutiao.com/search?keyword=莱巴金娜2-1萨巴伦卡首夺美网冠军)
1. [外卖员往饮料里加百草枯？假的](https://so.toutiao.com/search?keyword=外卖员往饮料里加百草枯？假的)
1. [警方通报公职人员醉驾致一对夫妻身亡](https://so.toutiao.com/search?keyword=警方通报公职人员醉驾致一对夫妻身亡)
1. [郭有才又回到了菏泽南站](https://so.toutiao.com/search?keyword=郭有才又回到了菏泽南站)
1. [3个方法把阳气“养”回来](https://so.toutiao.com/search?keyword=3个方法把阳气“养”回来)
1. [被罚了51.79亿的携程为何还在杀熟](https://so.toutiao.com/search?keyword=被罚了51.79亿的携程为何还在杀熟)
1. [多地小学改为养老院](https://so.toutiao.com/search?keyword=多地小学改为养老院)
1. [年轻人血管为什么会开始堵了](https://so.toutiao.com/search?keyword=年轻人血管为什么会开始堵了)
1. [84岁老人独自来店为自己挑选寿衣](https://so.toutiao.com/search?keyword=84岁老人独自来店为自己挑选寿衣)
1. [女性观众为什么爱看“追妻火葬场”](https://so.toutiao.com/search?keyword=女性观众为什么爱看“追妻火葬场”)
1. [北大硕士因本科非北大年薪被降5万](https://so.toutiao.com/search?keyword=北大硕士因本科非北大年薪被降5万)
1. [前TVB女星钟丽淇被曝急送ICU](https://so.toutiao.com/search?keyword=前TVB女星钟丽淇被曝急送ICU)
1. [日本旅游业承受签证费暴涨代价](https://so.toutiao.com/search?keyword=日本旅游业承受签证费暴涨代价)
1. [那英南京演唱会新编《山沟沟》](https://so.toutiao.com/search?keyword=那英南京演唱会新编《山沟沟》)
1. [特朗普7400万美元广告砸向关键选区](https://so.toutiao.com/search?keyword=特朗普7400万美元广告砸向关键选区)
1. [支付宝回应1.8元可伪造上亿转账截图](https://so.toutiao.com/search?keyword=支付宝回应1.8元可伪造上亿转账截图)
1. [俄方不排除普京和特朗普在中国会晤](https://so.toutiao.com/search?keyword=俄方不排除普京和特朗普在中国会晤)
1. [女子散步被蝙蝠撞脸紧急就医](https://so.toutiao.com/search?keyword=女子散步被蝙蝠撞脸紧急就医)
1. [下周上班时间有变](https://so.toutiao.com/search?keyword=下周上班时间有变)
1. [冉莹颖回应债还清后是否离婚](https://so.toutiao.com/search?keyword=冉莹颖回应债还清后是否离婚)
1. [试驾小米澎程意外驶出车道用户已锁单](https://so.toutiao.com/search?keyword=试驾小米澎程意外驶出车道用户已锁单)
1. [张雪被问带薪休假爽不：我是发钱那个](https://so.toutiao.com/search?keyword=张雪被问带薪休假爽不：我是发钱那个)
1. [吴沚默自曝在横店拍短剧遭遇潜规则](https://so.toutiao.com/search?keyword=吴沚默自曝在横店拍短剧遭遇潜规则)
1. [iPhone Duo炒到9万 黄牛贷款百万囤货](https://so.toutiao.com/search?keyword=iPhone%20Duo炒到9万%20黄牛贷款百万囤货)
1. [市委原书记化债不力被通报](https://so.toutiao.com/search?keyword=市委原书记化债不力被通报)
1. [中东局势骤变 全球经济承压](https://so.toutiao.com/search?keyword=中东局势骤变%20全球经济承压)
1. [下周会是黄金分水岭吗](https://so.toutiao.com/search?keyword=下周会是黄金分水岭吗)
1. [泡面怎么成了年轻人深夜“顶配大餐”](https://so.toutiao.com/search?keyword=泡面怎么成了年轻人深夜“顶配大餐”)
1. [伊拉克关闭与伊朗边境口岸有何考量](https://so.toutiao.com/search?keyword=伊拉克关闭与伊朗边境口岸有何考量)
1. [杨幂玩梗说自己45岁](https://so.toutiao.com/search?keyword=杨幂玩梗说自己45岁)
1. [房东催租反给租户转账2万](https://so.toutiao.com/search?keyword=房东催租反给租户转账2万)
1. [台人士：越来越多台青乐于走进大陆](https://so.toutiao.com/search?keyword=台人士：越来越多台青乐于走进大陆)
1. [人民日报：化债绝非数字游戏](https://so.toutiao.com/search?keyword=人民日报：化债绝非数字游戏)
1. [iPhone折叠屏为何命名为Duo](https://so.toutiao.com/search?keyword=iPhone折叠屏为何命名为Duo)
1. [印度称对台湾问题政策立场没有改变](https://so.toutiao.com/search?keyword=印度称对台湾问题政策立场没有改变)
1. [学者：“台独”分子私利至上甘当棋子](https://so.toutiao.com/search?keyword=学者：“台独”分子私利至上甘当棋子)
1. [胖东来两款网红月饼改线上购买](https://so.toutiao.com/search?keyword=胖东来两款网红月饼改线上购买)
1. [无锡市长蒋锋拟任设区市委书记](https://so.toutiao.com/search?keyword=无锡市长蒋锋拟任设区市委书记)
1. [李大霄：美联储加息的压力正在逼近](https://so.toutiao.com/search?keyword=李大霄：美联储加息的压力正在逼近)
1. [宁波大学暴雨典礼为何戳中人心](https://so.toutiao.com/search?keyword=宁波大学暴雨典礼为何戳中人心)
1. [中国男篮提前晋级亚运会八强](https://so.toutiao.com/search?keyword=中国男篮提前晋级亚运会八强)
1. [张本美和4-1战胜斯佐科斯晋级四强](https://so.toutiao.com/search?keyword=张本美和4-1战胜斯佐科斯晋级四强)
1. [雄安国际算力一体化调度中心上线运行](https://so.toutiao.com/search?keyword=雄安国际算力一体化调度中心上线运行)
1. [金砖峰会为中印关系带来哪些机遇](https://so.toutiao.com/search?keyword=金砖峰会为中印关系带来哪些机遇)
1. [马珊珊任沈阳市委副书记](https://so.toutiao.com/search?keyword=马珊珊任沈阳市委副书记)
1. [日本外交为何接连碰壁](https://so.toutiao.com/search?keyword=日本外交为何接连碰壁)
1. [15人合买彩票中3000万港元起纠纷](https://so.toutiao.com/search?keyword=15人合买彩票中3000万港元起纠纷)
1. [刘銮雄与弟弟罕同场看谭咏麟演唱会](https://so.toutiao.com/search?keyword=刘銮雄与弟弟罕同场看谭咏麟演唱会)
1. [AI安全研究者掀起“末日概率”讨论](https://so.toutiao.com/search?keyword=AI安全研究者掀起“末日概率”讨论)
1. [欧洲网友锐评让日本右翼破防](https://so.toutiao.com/search?keyword=欧洲网友锐评让日本右翼破防)
1. [AI真正的进化史](https://so.toutiao.com/search?keyword=AI真正的进化史)
1. [赵雷演唱会专列上歌迷自发大合唱](https://so.toutiao.com/search?keyword=赵雷演唱会专列上歌迷自发大合唱)
1. [记者直击金砖峰会媒体中心](https://so.toutiao.com/search?keyword=记者直击金砖峰会媒体中心)
1. [陈幸同晋级WTT澳门冠军赛女单4强](https://so.toutiao.com/search?keyword=陈幸同晋级WTT澳门冠军赛女单4强)
1. [戴羽彤亮相宿迁奥体助阵苏超](https://so.toutiao.com/search?keyword=戴羽彤亮相宿迁奥体助阵苏超)

<!-- END TOUTIAO -->

历史归档 [./archives/toutiao-search](./archives/toutiao-search)

## 知乎热搜榜

<!-- BEGIN ZHIHUSEARCH -->
<!-- 最后更新时间 Sun Sep 13 2026 06:14:46 GMT+0800 (China Standard Time) -->

1. [设计师称中国客厅已失去意义](https://www.zhihu.com/search?q=%E8%AE%BE%E8%AE%A1%E5%B8%88%E7%A7%B0%E4%B8%AD%E5%9B%BD%E5%AE%A2%E5%8E%85%E5%B7%B2%E5%A4%B1%E5%8E%BB%E6%84%8F%E4%B9%89)
1. [邓煜等菲奖得主称 AI 公司正摧毁数学](https://www.zhihu.com/search?q=%E9%82%93%E7%85%9C%E7%AD%89%E8%8F%B2%E5%A5%96%E5%BE%97%E4%B8%BB%E7%A7%B0%20AI%20%E5%85%AC%E5%8F%B8%E6%AD%A3%E6%91%A7%E6%AF%81%E6%95%B0%E5%AD%A6)
1. [多车队宣布永久退出中国 GT](https://www.zhihu.com/search?q=%E5%A4%9A%E8%BD%A6%E9%98%9F%E5%AE%A3%E5%B8%83%E6%B0%B8%E4%B9%85%E9%80%80%E5%87%BA%E4%B8%AD%E5%9B%BD%20GT)
1. [江西孩子看演唱会后全家低保取消](https://www.zhihu.com/search?q=%E6%B1%9F%E8%A5%BF%E5%AD%A9%E5%AD%90%E7%9C%8B%E6%BC%94%E5%94%B1%E4%BC%9A%E5%90%8E%E5%85%A8%E5%AE%B6%E4%BD%8E%E4%BF%9D%E5%8F%96%E6%B6%88)
1. [知乎 CLI 创作者能力上新](https://www.zhihu.com/search?q=%E7%9F%A5%E4%B9%8E%20CLI%20%E5%88%9B%E4%BD%9C%E8%80%85%E8%83%BD%E5%8A%9B%E4%B8%8A%E6%96%B0)
1. [刘翔被体育局买断获49.4万](https://www.zhihu.com/search?q=%E5%88%98%E7%BF%94%E8%A2%AB%E4%BD%93%E8%82%B2%E5%B1%80%E4%B9%B0%E6%96%AD%E8%8E%B749.4%E4%B8%87)
1. [三星嘲讽苹果iPhoneDuo](https://www.zhihu.com/search?q=%E4%B8%89%E6%98%9F%E5%98%B2%E8%AE%BD%E8%8B%B9%E6%9E%9CiPhoneDuo)
1. [医生建议内裤袜子放洗衣机洗](https://www.zhihu.com/search?q=%E5%8C%BB%E7%94%9F%E5%BB%BA%E8%AE%AE%E5%86%85%E8%A3%A4%E8%A2%9C%E5%AD%90%E6%94%BE%E6%B4%97%E8%A1%A3%E6%9C%BA%E6%B4%97)
1. [比亚迪利润奖事件](https://www.zhihu.com/search?q=%E6%AF%94%E4%BA%9A%E8%BF%AA%E5%88%A9%E6%B6%A6%E5%A5%96%E4%BA%8B%E4%BB%B6)
1. [女子称被公职人员推入厕所强奸](https://www.zhihu.com/search?q=%E5%A5%B3%E5%AD%90%E7%A7%B0%E8%A2%AB%E5%85%AC%E8%81%8C%E4%BA%BA%E5%91%98%E6%8E%A8%E5%85%A5%E5%8E%95%E6%89%80%E5%BC%BA%E5%A5%B8)
1. [「魔法画报」当事人称事件与荣耀手机无关](https://www.zhihu.com/search?q=%E3%80%8C%E9%AD%94%E6%B3%95%E7%94%BB%E6%8A%A5%E3%80%8D%E5%BD%93%E4%BA%8B%E4%BA%BA%E7%A7%B0%E4%BA%8B%E4%BB%B6%E4%B8%8E%E8%8D%A3%E8%80%80%E6%89%8B%E6%9C%BA%E6%97%A0%E5%85%B3)
1. [住建局副局长群内辱骂业主被停职](https://www.zhihu.com/search?q=%E4%BD%8F%E5%BB%BA%E5%B1%80%E5%89%AF%E5%B1%80%E9%95%BF%E7%BE%A4%E5%86%85%E8%BE%B1%E9%AA%82%E4%B8%9A%E4%B8%BB%E8%A2%AB%E5%81%9C%E8%81%8C)
1. [小孩 7 楼坠下砸坏宝马车](https://www.zhihu.com/search?q=%E5%B0%8F%E5%AD%A9%207%20%E6%A5%BC%E5%9D%A0%E4%B8%8B%E7%A0%B8%E5%9D%8F%E5%AE%9D%E9%A9%AC%E8%BD%A6)
1. [红果日活超爱优腾芒四家总和](https://www.zhihu.com/search?q=%E7%BA%A2%E6%9E%9C%E6%97%A5%E6%B4%BB%E8%B6%85%E7%88%B1%E4%BC%98%E8%85%BE%E8%8A%92%E5%9B%9B%E5%AE%B6%E6%80%BB%E5%92%8C)

<!-- END ZHIHUSEARCH -->

历史归档 [./archives/zhihu-search](./archives/zhihu-search)

## 知乎热门话题

<!-- BEGIN ZHIHUQUESTIONS -->
<!-- 最后更新时间 Sun Sep 13 2026 06:20:29 GMT+0800 (China Standard Time) -->

1. [网友爆料付航脱口秀1300张门票有一千张黄牛票，检票时强实名导致80%观众进不了，反映了哪些市场乱象？](https://www.zhihu.com/question/2082137769556628200)
1. [如何看待跳水奥运冠军张家齐称自己「慕强」，但男友实力似乎都低于她？](https://www.zhihu.com/question/2080416209279964000)
1. [LPL 2026 赛季败者组决赛 AL 3:2 淘汰 iG 晋级总决赛，如何评价这场比赛？](https://www.zhihu.com/question/2082125425837335000)
1. [亲戚借了网贷，还不起了，想找我帮忙，她不想告诉家人，数额巨大，我该怎么办？](https://www.zhihu.com/question/2072381217173921800)
1. [世卫预警全球癌症病例2050年可能激增67%，将上升至近3500万例，这意味着什么？有哪些预防措施？](https://www.zhihu.com/question/2059080438518436400)
1. [锂电池本月起征税，有电池企业率先涨价，业内判断10万元以内纯电车压力最大，行业会迎来新一轮洗牌吗？](https://www.zhihu.com/question/2081672062029019000)
1. [如何评价 DeepSeek 灰度测试语音对话，意味着什么？](https://www.zhihu.com/question/2082041103209820700)
1. [一设计师称中国客厅已失去意义，反映了当下怎样的家庭生活变化？你家还有客厅吗，是怎样的？](https://www.zhihu.com/question/2079581505047762000)
1. [陶哲轩、邓煜等菲奖得主联合抗议 AI 公司数学军备竞赛，AI 是否在毁掉数学？](https://www.zhihu.com/question/2082035913132193300)
1. [拆弹的时候为什么不一下把线全剪了?](https://www.zhihu.com/question/347179994)
1. [加拿大一向很听美国的话，这次怎么敢真的和美国打贸易战？](https://www.zhihu.com/question/2078761189157425700)
1. [女子向大雁塔景区雨水井塞管状不明物，警方已介入调查，可能塞的是什么？会承担怎样的责任？](https://www.zhihu.com/question/2080972261511487700)
1. [2026 WTT 澳门冠军赛女单四分之一决赛，陈熠 4-0韩莹，如何评价这场比赛？](https://www.zhihu.com/question/2082097949958485500)
1. [如何评价崩铁4.5活动方寸大冒险？](https://www.zhihu.com/question/2082085679195079400)
1. [都市剧总拍精英人设，为什么很难拍好普通人真实的生活？](https://www.zhihu.com/question/2079837487493543400)
1. [如何看待胡塞武装突然势如破竹控制曼德海峡和红海南部？这对当前局势有哪些影响？](https://www.zhihu.com/question/2081887737754415400)
1. [苹果高管称折叠屏比例泄密很遗憾，竞争对手拿到了屏幕比例，泄密为何难以防范？将对行业造成哪些影响？](https://www.zhihu.com/question/2081904462331908600)
1. [家长如何有效提升孩子的抗挫力？](https://www.zhihu.com/question/2080991958110040800)
1. [如何评价2026年9月米哈游《原神》7.1版本前瞻直播【往冥府的安魂歌】？](https://www.zhihu.com/question/2081765230707843000)
1. [LCK季后赛败者组决赛T1 1:3 HLE，如何评价这场比赛？](https://www.zhihu.com/question/2082161309999706600)
1. [iPhone 18 Pro 和 Max 开启预购，你抢到了吗？](https://www.zhihu.com/question/2082209639156769000)
1. [《死神千年血战篇》第四季祸进谭开播，如何评价第八集？](https://www.zhihu.com/question/2082239134933042200)
1. [2026澳门冠军赛男单1/4决赛，雨果4-2松岛辉空，晋级半决赛，如何评价两人本场比赛的发挥？](https://www.zhihu.com/question/2082229729579606000)
1. [《还珠》结局，为什么永琪逃亡云南，而尔康必须回京？](https://www.zhihu.com/question/33825141)
1. [家长花 20 万买房车陪读上高中儿子，称比租房划算，这笔账该怎么算？这种陪读方式值得吗？](https://www.zhihu.com/question/2082076266056738800)
1. [酒店为什么会有三小时钟点房？](https://www.zhihu.com/question/351651719)
1. [订阅了Kimi的199套餐，编程是用Kimi code好还是claude code好呢？](https://www.zhihu.com/question/2042306734392431900)
1. [为什么有些人在亲密关系里越痛苦，反而越离不开对方？](https://www.zhihu.com/question/2078584861032559000)
1. [白人饭的魅力主要是省时还是健康？](https://www.zhihu.com/question/2068725103534330400)
1. [一天一瓶啤酒，对身体有害吗？](https://www.zhihu.com/question/2080303059578705400)
1. [为什么打到现在，伊朗还有能力反击美国？](https://www.zhihu.com/question/2017262320611508200)
1. [“我端着一碗爷爷煮的面”有语法错误吗？](https://www.zhihu.com/question/2075605552319804000)
1. [如何评价《潜伏》里的罗掌柜？](https://www.zhihu.com/question/763191249)
1. [肠道里住着那么多细菌，免疫系统为什么不会一直攻击它们？](https://www.zhihu.com/question/2078484653351121700)
1. [赵松源进国家队，和董路的「培养」关系大吗？](https://www.zhihu.com/question/2081031712155199500)
1. [为什么很多家长特别爱转视频号当自己的「嘴替」来教育孩子？](https://www.zhihu.com/question/2080334464459039700)
1. [如何看待 DeepSeek V4 PRO 9月14日之后继续提供服务？](https://www.zhihu.com/question/2081824833357231400)

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
<!-- 最后更新时间 Sun Sep 13 2026 06:24:58 GMT+0800 (China Standard Time) -->

1. [习近平会见莫迪](https://s.weibo.com//weibo?q=%23%E4%B9%A0%E8%BF%91%E5%B9%B3%E4%BC%9A%E8%A7%81%E8%8E%AB%E8%BF%AA%23&Refer=new_time)
1. [AI短剧 成瘾](https://s.weibo.com//weibo?q=AI%E7%9F%AD%E5%89%A7%20%E6%88%90%E7%98%BE&t=31&band_rank=1&Refer=top)
1. [吃得越狠老得越慢](https://s.weibo.com//weibo?q=%E5%90%83%E5%BE%97%E8%B6%8A%E7%8B%A0%E8%80%81%E5%BE%97%E8%B6%8A%E6%85%A2&t=31&band_rank=2&Refer=top)
1. [金砖合作打造互联互通贸易通道](https://s.weibo.com//weibo?q=%23%E9%87%91%E7%A0%96%E5%90%88%E4%BD%9C%E6%89%93%E9%80%A0%E4%BA%92%E8%81%94%E4%BA%92%E9%80%9A%E8%B4%B8%E6%98%93%E9%80%9A%E9%81%93%23&t=31&band_rank=3&Refer=top)
1. [赵雷当爸爸了](https://s.weibo.com//weibo?q=%23%E8%B5%B5%E9%9B%B7%E5%BD%93%E7%88%B8%E7%88%B8%E4%BA%86%23&t=31&band_rank=4&Refer=top)
1. [孙心然美网青少年冠军](https://s.weibo.com//weibo?q=%23%E5%AD%99%E5%BF%83%E7%84%B6%E7%BE%8E%E7%BD%91%E9%9D%92%E5%B0%91%E5%B9%B4%E5%86%A0%E5%86%9B%23&t=31&band_rank=5&Refer=top)
1. [养得起父母却担心没人养我](https://s.weibo.com//weibo?q=%E5%85%BB%E5%BE%97%E8%B5%B7%E7%88%B6%E6%AF%8D%E5%8D%B4%E6%8B%85%E5%BF%83%E6%B2%A1%E4%BA%BA%E5%85%BB%E6%88%91&t=31&band_rank=6&Refer=top)
1. [弹壳说唱巅峰对决总冠军](https://s.weibo.com//weibo?q=%23%E5%BC%B9%E5%A3%B3%E8%AF%B4%E5%94%B1%E5%B7%85%E5%B3%B0%E5%AF%B9%E5%86%B3%E6%80%BB%E5%86%A0%E5%86%9B%23&t=31&band_rank=7&Refer=top)
1. [刘畊宏参加披哥掉粉近40万](https://s.weibo.com//weibo?q=%23%E5%88%98%E7%95%8A%E5%AE%8F%E5%8F%82%E5%8A%A0%E6%8A%AB%E5%93%A5%E6%8E%89%E7%B2%89%E8%BF%9140%E4%B8%87%23&t=31&band_rank=8&Refer=top)
1. [张国伟说不会自己花钱练体育](https://s.weibo.com//weibo?q=%23%E5%BC%A0%E5%9B%BD%E4%BC%9F%E8%AF%B4%E4%B8%8D%E4%BC%9A%E8%87%AA%E5%B7%B1%E8%8A%B1%E9%92%B1%E7%BB%83%E4%BD%93%E8%82%B2%23&t=31&band_rank=9&Refer=top)
1. [兰香如故男扮女装美得出彩](https://s.weibo.com//weibo?q=%E5%85%B0%E9%A6%99%E5%A6%82%E6%95%85%E7%94%B7%E6%89%AE%E5%A5%B3%E8%A3%85%E7%BE%8E%E5%BE%97%E5%87%BA%E5%BD%A9&t=31&band_rank=10&Refer=top)
1. [市场监管局回应烧烤店2个月被查15次](https://s.weibo.com//weibo?q=%23%E5%B8%82%E5%9C%BA%E7%9B%91%E7%AE%A1%E5%B1%80%E5%9B%9E%E5%BA%94%E7%83%A7%E7%83%A4%E5%BA%972%E4%B8%AA%E6%9C%88%E8%A2%AB%E6%9F%A515%E6%AC%A1%23&t=31&band_rank=11&Refer=top)
1. [厂二代下场当网红翻车](https://s.weibo.com//weibo?q=%23%E5%8E%82%E4%BA%8C%E4%BB%A3%E4%B8%8B%E5%9C%BA%E5%BD%93%E7%BD%91%E7%BA%A2%E7%BF%BB%E8%BD%A6%23&t=31&band_rank=12&Refer=top)
1. [付航回应脱口秀禁黄牛票入场](https://s.weibo.com//weibo?q=%23%E4%BB%98%E8%88%AA%E5%9B%9E%E5%BA%94%E8%84%B1%E5%8F%A3%E7%A7%80%E7%A6%81%E9%BB%84%E7%89%9B%E7%A5%A8%E5%85%A5%E5%9C%BA%23&t=31&band_rank=13&Refer=top)
1. [大姐购房父亲将402万房款分给两妹妹](https://s.weibo.com//weibo?q=%23%E5%A4%A7%E5%A7%90%E8%B4%AD%E6%88%BF%E7%88%B6%E4%BA%B2%E5%B0%86402%E4%B8%87%E6%88%BF%E6%AC%BE%E5%88%86%E7%BB%99%E4%B8%A4%E5%A6%B9%E5%A6%B9%23&t=31&band_rank=14&Refer=top)
1. [桑德兰vs阿森纳](https://s.weibo.com//weibo?q=%E6%A1%91%E5%BE%B7%E5%85%B0vs%E9%98%BF%E6%A3%AE%E7%BA%B3&t=31&band_rank=15&Refer=top)
1. [举报文物失踪被查多次店主发声](https://s.weibo.com//weibo?q=%23%E4%B8%BE%E6%8A%A5%E6%96%87%E7%89%A9%E5%A4%B1%E8%B8%AA%E8%A2%AB%E6%9F%A5%E5%A4%9A%E6%AC%A1%E5%BA%97%E4%B8%BB%E5%8F%91%E5%A3%B0%23&t=31&band_rank=16&Refer=top)
1. [TTG夺冠](https://s.weibo.com//weibo?q=TTG%E5%A4%BA%E5%86%A0&t=31&band_rank=17&Refer=top)
1. [FISTAuto中国GT](https://s.weibo.com//weibo?q=FISTAuto%E4%B8%AD%E5%9B%BDGT&t=31&band_rank=18&Refer=top)
1. [狼队 遗憾](https://s.weibo.com//weibo?q=%E7%8B%BC%E9%98%9F%20%E9%81%97%E6%86%BE&t=31&band_rank=19&Refer=top)
1. [孙心然回应美网青少年夺冠](https://s.weibo.com//weibo?q=%23%E5%AD%99%E5%BF%83%E7%84%B6%E5%9B%9E%E5%BA%94%E7%BE%8E%E7%BD%91%E9%9D%92%E5%B0%91%E5%B9%B4%E5%A4%BA%E5%86%A0%23&t=31&band_rank=20&Refer=top)
1. [为什么几乎不存在完美藏尸](https://s.weibo.com//weibo?q=%E4%B8%BA%E4%BB%80%E4%B9%88%E5%87%A0%E4%B9%8E%E4%B8%8D%E5%AD%98%E5%9C%A8%E5%AE%8C%E7%BE%8E%E8%97%8F%E5%B0%B8&t=31&band_rank=21&Refer=top)
1. [想换手机的欲望突然到了极致](https://s.weibo.com//weibo?q=%E6%83%B3%E6%8D%A2%E6%89%8B%E6%9C%BA%E7%9A%84%E6%AC%B2%E6%9C%9B%E7%AA%81%E7%84%B6%E5%88%B0%E4%BA%86%E6%9E%81%E8%87%B4&t=31&band_rank=22&Refer=top)
1. [皇马vs巴列卡诺](https://s.weibo.com//weibo?q=%E7%9A%87%E9%A9%ACvs%E5%B7%B4%E5%88%97%E5%8D%A1%E8%AF%BA&t=31&band_rank=23&Refer=top)
1. [一个妈妈在家做烤串的视频火了](https://s.weibo.com//weibo?q=%23%E4%B8%80%E4%B8%AA%E5%A6%88%E5%A6%88%E5%9C%A8%E5%AE%B6%E5%81%9A%E7%83%A4%E4%B8%B2%E7%9A%84%E8%A7%86%E9%A2%91%E7%81%AB%E4%BA%86%23&t=31&band_rank=24&Refer=top)
1. [你们经常换手机的人嘴真严](https://s.weibo.com//weibo?q=%23%E4%BD%A0%E4%BB%AC%E7%BB%8F%E5%B8%B8%E6%8D%A2%E6%89%8B%E6%9C%BA%E7%9A%84%E4%BA%BA%E5%98%B4%E7%9C%9F%E4%B8%A5%23&t=31&band_rank=25&Refer=top)
1. [紫幻回应巅峰对决阵容](https://s.weibo.com//weibo?q=%23%E7%B4%AB%E5%B9%BB%E5%9B%9E%E5%BA%94%E5%B7%85%E5%B3%B0%E5%AF%B9%E5%86%B3%E9%98%B5%E5%AE%B9%23&t=31&band_rank=26&Refer=top)
1. [非必要不熬夜](https://s.weibo.com//weibo?q=%E9%9D%9E%E5%BF%85%E8%A6%81%E4%B8%8D%E7%86%AC%E5%A4%9C&t=31&band_rank=27&Refer=top)
1. [苹果18 抢不到](https://s.weibo.com//weibo?q=%E8%8B%B9%E6%9E%9C18%20%E6%8A%A2%E4%B8%8D%E5%88%B0&t=31&band_rank=28&Refer=top)
1. [为什么早上是喝咖啡的最佳时间](https://s.weibo.com//weibo?q=%23%E4%B8%BA%E4%BB%80%E4%B9%88%E6%97%A9%E4%B8%8A%E6%98%AF%E5%96%9D%E5%92%96%E5%95%A1%E7%9A%84%E6%9C%80%E4%BD%B3%E6%97%B6%E9%97%B4%23&t=31&band_rank=29&Refer=top)
1. [iPhone18Pro系列首批货源全线告急](https://s.weibo.com//weibo?q=%23iPhone18Pro%E7%B3%BB%E5%88%97%E9%A6%96%E6%89%B9%E8%B4%A7%E6%BA%90%E5%85%A8%E7%BA%BF%E5%91%8A%E6%80%A5%23&t=31&band_rank=30&Refer=top)
1. [狗脚根本擦不干净](https://s.weibo.com//weibo?q=%23%E7%8B%97%E8%84%9A%E6%A0%B9%E6%9C%AC%E6%93%A6%E4%B8%8D%E5%B9%B2%E5%87%80%23&t=31&band_rank=31&Refer=top)
1. [莱巴金娜首盘6比4萨巴伦卡](https://s.weibo.com//weibo?q=%23%E8%8E%B1%E5%B7%B4%E9%87%91%E5%A8%9C%E9%A6%96%E7%9B%986%E6%AF%944%E8%90%A8%E5%B7%B4%E4%BC%A6%E5%8D%A1%23&t=31&band_rank=32&Refer=top)
1. [美网官方祝贺孙心然夺冠](https://s.weibo.com//weibo?q=%23%E7%BE%8E%E7%BD%91%E5%AE%98%E6%96%B9%E7%A5%9D%E8%B4%BA%E5%AD%99%E5%BF%83%E7%84%B6%E5%A4%BA%E5%86%A0%23&t=31&band_rank=33&Refer=top)
1. [桑德兰0比2阿森纳](https://s.weibo.com//weibo?q=%23%E6%A1%91%E5%BE%B7%E5%85%B00%E6%AF%942%E9%98%BF%E6%A3%AE%E7%BA%B3%23&t=31&band_rank=34&Refer=top)
1. [妈妈做烤串人怎么能聪明成这样](https://s.weibo.com//weibo?q=%E5%A6%88%E5%A6%88%E5%81%9A%E7%83%A4%E4%B8%B2%E4%BA%BA%E6%80%8E%E4%B9%88%E8%83%BD%E8%81%AA%E6%98%8E%E6%88%90%E8%BF%99%E6%A0%B7&t=31&band_rank=35&Refer=top)
1. [女子散步被蝙蝠撞脸连夜打狂犬疫苗](https://s.weibo.com//weibo?q=%23%E5%A5%B3%E5%AD%90%E6%95%A3%E6%AD%A5%E8%A2%AB%E8%9D%99%E8%9D%A0%E6%92%9E%E8%84%B8%E8%BF%9E%E5%A4%9C%E6%89%93%E7%8B%82%E7%8A%AC%E7%96%AB%E8%8B%97%23&t=31&band_rank=36&Refer=top)
1. [iPhone18Pro系列抢购火爆](https://s.weibo.com//weibo?q=iPhone18Pro%E7%B3%BB%E5%88%97%E6%8A%A2%E8%B4%AD%E7%81%AB%E7%88%86&t=31&band_rank=37&Refer=top)
1. [男子贷款60万开店2个月被差评干哭](https://s.weibo.com//weibo?q=%23%E7%94%B7%E5%AD%90%E8%B4%B7%E6%AC%BE60%E4%B8%87%E5%BC%80%E5%BA%972%E4%B8%AA%E6%9C%88%E8%A2%AB%E5%B7%AE%E8%AF%84%E5%B9%B2%E5%93%AD%23&t=31&band_rank=38&Refer=top)
1. [小胖6冠4FMVP](https://s.weibo.com//weibo?q=%23%E5%B0%8F%E8%83%966%E5%86%A04FMVP%23&t=31&band_rank=39&Refer=top)
1. [英超联赛](https://s.weibo.com//weibo?q=%E8%8B%B1%E8%B6%85%E8%81%94%E8%B5%9B&t=31&band_rank=40&Refer=top)
1. [兰香如故](https://s.weibo.com//weibo?q=%E5%85%B0%E9%A6%99%E5%A6%82%E6%95%85&t=31&band_rank=41&Refer=top)
1. [苏超](https://s.weibo.com//weibo?q=%E8%8B%8F%E8%B6%85&t=31&band_rank=42&Refer=top)
1. [校方回应男厕所里设置女厕所](https://s.weibo.com//weibo?q=%23%E6%A0%A1%E6%96%B9%E5%9B%9E%E5%BA%94%E7%94%B7%E5%8E%95%E6%89%80%E9%87%8C%E8%AE%BE%E7%BD%AE%E5%A5%B3%E5%8E%95%E6%89%80%23&t=31&band_rank=43&Refer=top)
1. [iPhone18Pro系列有多难抢](https://s.weibo.com//weibo?q=%23iPhone18Pro%E7%B3%BB%E5%88%97%E6%9C%89%E5%A4%9A%E9%9A%BE%E6%8A%A2%23&t=31&band_rank=44&Refer=top)
1. [张杰杭州演唱会散场后亮起国之脊梁](https://s.weibo.com//weibo?q=%23%E5%BC%A0%E6%9D%B0%E6%9D%AD%E5%B7%9E%E6%BC%94%E5%94%B1%E4%BC%9A%E6%95%A3%E5%9C%BA%E5%90%8E%E4%BA%AE%E8%B5%B7%E5%9B%BD%E4%B9%8B%E8%84%8A%E6%A2%81%23&t=31&band_rank=45&Refer=top)
1. [孙心然重心转向成人比赛](https://s.weibo.com//weibo?q=%E5%AD%99%E5%BF%83%E7%84%B6%E9%87%8D%E5%BF%83%E8%BD%AC%E5%90%91%E6%88%90%E4%BA%BA%E6%AF%94%E8%B5%9B&t=31&band_rank=46&Refer=top)
1. [小胖现场喊天狼星天为首](https://s.weibo.com//weibo?q=%23%E5%B0%8F%E8%83%96%E7%8E%B0%E5%9C%BA%E5%96%8A%E5%A4%A9%E7%8B%BC%E6%98%9F%E5%A4%A9%E4%B8%BA%E9%A6%96%23&t=31&band_rank=47&Refer=top)
1. [F1](https://s.weibo.com//weibo?q=F1&t=31&band_rank=48&Refer=top)
1. [Bin拒绝放狠话](https://s.weibo.com//weibo?q=%23Bin%E6%8B%92%E7%BB%9D%E6%94%BE%E7%8B%A0%E8%AF%9D%23&t=31&band_rank=49&Refer=top)
1. [AG 年总](https://s.weibo.com//weibo?q=AG%20%E5%B9%B4%E6%80%BB&t=31&band_rank=50&Refer=top)
1. [狼队 遗憾](https://s.weibo.com//weibo?q=%E7%8B%BC%E9%98%9F%20%E9%81%97%E6%86%BE&t=31&band_rank=1&Refer=top)
1. [兰香如故](https://s.weibo.com//weibo?q=%E5%85%B0%E9%A6%99%E5%A6%82%E6%95%85&t=31&band_rank=2&Refer=top)
1. [吃得越狠老得越慢](https://s.weibo.com//weibo?q=%E5%90%83%E5%BE%97%E8%B6%8A%E7%8B%A0%E8%80%81%E5%BE%97%E8%B6%8A%E6%85%A2&t=31&band_rank=4&Refer=top)
1. [AI短剧 成瘾](https://s.weibo.com//weibo?q=AI%E7%9F%AD%E5%89%A7%20%E6%88%90%E7%98%BE&t=31&band_rank=5&Refer=top)
1. [弹壳说唱巅峰对决总冠军](https://s.weibo.com//weibo?q=%23%E5%BC%B9%E5%A3%B3%E8%AF%B4%E5%94%B1%E5%B7%85%E5%B3%B0%E5%AF%B9%E5%86%B3%E6%80%BB%E5%86%A0%E5%86%9B%23&t=31&band_rank=6&Refer=top)
1. [赵雷当爸爸了](https://s.weibo.com//weibo?q=%23%E8%B5%B5%E9%9B%B7%E5%BD%93%E7%88%B8%E7%88%B8%E4%BA%86%23&t=31&band_rank=7&Refer=top)
1. [孙心然美网青少年冠军](https://s.weibo.com//weibo?q=%23%E5%AD%99%E5%BF%83%E7%84%B6%E7%BE%8E%E7%BD%91%E9%9D%92%E5%B0%91%E5%B9%B4%E5%86%A0%E5%86%9B%23&t=31&band_rank=9&Refer=top)
1. [AG 年总](https://s.weibo.com//weibo?q=AG%20%E5%B9%B4%E6%80%BB&t=31&band_rank=10&Refer=top)
1. [TTG夺冠](https://s.weibo.com//weibo?q=TTG%E5%A4%BA%E5%86%A0&t=31&band_rank=12&Refer=top)
1. [张国伟说不会自己花钱练体育](https://s.weibo.com//weibo?q=%23%E5%BC%A0%E5%9B%BD%E4%BC%9F%E8%AF%B4%E4%B8%8D%E4%BC%9A%E8%87%AA%E5%B7%B1%E8%8A%B1%E9%92%B1%E7%BB%83%E4%BD%93%E8%82%B2%23&t=31&band_rank=13&Refer=top)
1. [付航回应脱口秀禁黄牛票入场](https://s.weibo.com//weibo?q=%23%E4%BB%98%E8%88%AA%E5%9B%9E%E5%BA%94%E8%84%B1%E5%8F%A3%E7%A7%80%E7%A6%81%E9%BB%84%E7%89%9B%E7%A5%A8%E5%85%A5%E5%9C%BA%23&t=31&band_rank=14&Refer=top)
1. [小胖现场喊天狼星天为首](https://s.weibo.com//weibo?q=%23%E5%B0%8F%E8%83%96%E7%8E%B0%E5%9C%BA%E5%96%8A%E5%A4%A9%E7%8B%BC%E6%98%9F%E5%A4%A9%E4%B8%BA%E9%A6%96%23&t=31&band_rank=15&Refer=top)
1. [厂二代下场当网红翻车](https://s.weibo.com//weibo?q=%23%E5%8E%82%E4%BA%8C%E4%BB%A3%E4%B8%8B%E5%9C%BA%E5%BD%93%E7%BD%91%E7%BA%A2%E7%BF%BB%E8%BD%A6%23&t=31&band_rank=16&Refer=top)
1. [大姐购房父亲将402万房款分给两妹妹](https://s.weibo.com//weibo?q=%23%E5%A4%A7%E5%A7%90%E8%B4%AD%E6%88%BF%E7%88%B6%E4%BA%B2%E5%B0%86402%E4%B8%87%E6%88%BF%E6%AC%BE%E5%88%86%E7%BB%99%E4%B8%A4%E5%A6%B9%E5%A6%B9%23&t=31&band_rank=17&Refer=top)
1. [举报文物失踪被查多次店主发声](https://s.weibo.com//weibo?q=%23%E4%B8%BE%E6%8A%A5%E6%96%87%E7%89%A9%E5%A4%B1%E8%B8%AA%E8%A2%AB%E6%9F%A5%E5%A4%9A%E6%AC%A1%E5%BA%97%E4%B8%BB%E5%8F%91%E5%A3%B0%23&t=31&band_rank=18&Refer=top)
1. [兰香如故男扮女装美得出彩](https://s.weibo.com//weibo?q=%E5%85%B0%E9%A6%99%E5%A6%82%E6%95%85%E7%94%B7%E6%89%AE%E5%A5%B3%E8%A3%85%E7%BE%8E%E5%BE%97%E5%87%BA%E5%BD%A9&t=31&band_rank=19&Refer=top)
1. [FISTAuto中国GT](https://s.weibo.com//weibo?q=FISTAuto%E4%B8%AD%E5%9B%BDGT&t=31&band_rank=20&Refer=top)
1. [非必要不熬夜](https://s.weibo.com//weibo?q=%E9%9D%9E%E5%BF%85%E8%A6%81%E4%B8%8D%E7%86%AC%E5%A4%9C&t=31&band_rank=21&Refer=top)
1. [为什么几乎不存在完美藏尸](https://s.weibo.com//weibo?q=%E4%B8%BA%E4%BB%80%E4%B9%88%E5%87%A0%E4%B9%8E%E4%B8%8D%E5%AD%98%E5%9C%A8%E5%AE%8C%E7%BE%8E%E8%97%8F%E5%B0%B8&t=31&band_rank=22&Refer=top)
1. [一个妈妈在家做烤串的视频火了](https://s.weibo.com//weibo?q=%23%E4%B8%80%E4%B8%AA%E5%A6%88%E5%A6%88%E5%9C%A8%E5%AE%B6%E5%81%9A%E7%83%A4%E4%B8%B2%E7%9A%84%E8%A7%86%E9%A2%91%E7%81%AB%E4%BA%86%23&t=31&band_rank=23&Refer=top)
1. [皖皖状态](https://s.weibo.com//weibo?q=%E7%9A%96%E7%9A%96%E7%8A%B6%E6%80%81&t=31&band_rank=24&Refer=top)
1. [苹果18 抢不到](https://s.weibo.com//weibo?q=%E8%8B%B9%E6%9E%9C18%20%E6%8A%A2%E4%B8%8D%E5%88%B0&t=31&band_rank=25&Refer=top)
1. [赵雷1排1座留给母亲](https://s.weibo.com//weibo?q=%23%E8%B5%B5%E9%9B%B71%E6%8E%921%E5%BA%A7%E7%95%99%E7%BB%99%E6%AF%8D%E4%BA%B2%23&t=31&band_rank=26&Refer=top)
1. [小胖FMVP](https://s.weibo.com//weibo?q=%E5%B0%8F%E8%83%96FMVP&t=31&band_rank=27&Refer=top)
1. [为什么早上是喝咖啡的最佳时间](https://s.weibo.com//weibo?q=%23%E4%B8%BA%E4%BB%80%E4%B9%88%E6%97%A9%E4%B8%8A%E6%98%AF%E5%96%9D%E5%92%96%E5%95%A1%E7%9A%84%E6%9C%80%E4%BD%B3%E6%97%B6%E9%97%B4%23&t=31&band_rank=28&Refer=top)
1. [东北超](https://s.weibo.com//weibo?q=%E4%B8%9C%E5%8C%97%E8%B6%85&t=31&band_rank=29&Refer=top)
1. [F1](https://s.weibo.com//weibo?q=F1&t=31&band_rank=30&Refer=top)
1. [你们经常换手机的人嘴真严](https://s.weibo.com//weibo?q=%23%E4%BD%A0%E4%BB%AC%E7%BB%8F%E5%B8%B8%E6%8D%A2%E6%89%8B%E6%9C%BA%E7%9A%84%E4%BA%BA%E5%98%B4%E7%9C%9F%E4%B8%A5%23&t=31&band_rank=31&Refer=top)
1. [想换手机的欲望突然到了极致](https://s.weibo.com//weibo?q=%E6%83%B3%E6%8D%A2%E6%89%8B%E6%9C%BA%E7%9A%84%E6%AC%B2%E6%9C%9B%E7%AA%81%E7%84%B6%E5%88%B0%E4%BA%86%E6%9E%81%E8%87%B4&t=31&band_rank=32&Refer=top)
1. [小胖6冠4FMVP](https://s.weibo.com//weibo?q=%23%E5%B0%8F%E8%83%966%E5%86%A04FMVP%23&t=31&band_rank=33&Refer=top)
1. [养得起父母却担心没人养我](https://s.weibo.com//weibo?q=%E5%85%BB%E5%BE%97%E8%B5%B7%E7%88%B6%E6%AF%8D%E5%8D%B4%E6%8B%85%E5%BF%83%E6%B2%A1%E4%BA%BA%E5%85%BB%E6%88%91&t=31&band_rank=34&Refer=top)
1. [AL战胜iG](https://s.weibo.com//weibo?q=AL%E6%88%98%E8%83%9CiG&t=31&band_rank=35&Refer=top)
1. [心疼清清](https://s.weibo.com//weibo?q=%E5%BF%83%E7%96%BC%E6%B8%85%E6%B8%85&t=31&band_rank=36&Refer=top)
1. [iPhone18Pro系列有多难抢](https://s.weibo.com//weibo?q=%23iPhone18Pro%E7%B3%BB%E5%88%97%E6%9C%89%E5%A4%9A%E9%9A%BE%E6%8A%A2%23&t=31&band_rank=37&Refer=top)
1. [Bin拒绝放狠话](https://s.weibo.com//weibo?q=%23Bin%E6%8B%92%E7%BB%9D%E6%94%BE%E7%8B%A0%E8%AF%9D%23&t=31&band_rank=38&Refer=top)
1. [男子贷款60万开店2个月被差评干哭](https://s.weibo.com//weibo?q=%23%E7%94%B7%E5%AD%90%E8%B4%B7%E6%AC%BE60%E4%B8%87%E5%BC%80%E5%BA%972%E4%B8%AA%E6%9C%88%E8%A2%AB%E5%B7%AE%E8%AF%84%E5%B9%B2%E5%93%AD%23&t=31&band_rank=39&Refer=top)
1. [张杰杭州演唱会散场后亮起国之脊梁](https://s.weibo.com//weibo?q=%23%E5%BC%A0%E6%9D%B0%E6%9D%AD%E5%B7%9E%E6%BC%94%E5%94%B1%E4%BC%9A%E6%95%A3%E5%9C%BA%E5%90%8E%E4%BA%AE%E8%B5%B7%E5%9B%BD%E4%B9%8B%E8%84%8A%E6%A2%81%23&t=31&band_rank=40&Refer=top)
1. [狼队状态](https://s.weibo.com//weibo?q=%E7%8B%BC%E9%98%9F%E7%8A%B6%E6%80%81&t=31&band_rank=41&Refer=top)
1. [iPhone18扣款成功仍等待付款](https://s.weibo.com//weibo?q=iPhone18%E6%89%A3%E6%AC%BE%E6%88%90%E5%8A%9F%E4%BB%8D%E7%AD%89%E5%BE%85%E4%BB%98%E6%AC%BE&t=31&band_rank=42&Refer=top)
1. [妈妈做烤串人怎么能聪明成这样](https://s.weibo.com//weibo?q=%E5%A6%88%E5%A6%88%E5%81%9A%E7%83%A4%E4%B8%B2%E4%BA%BA%E6%80%8E%E4%B9%88%E8%83%BD%E8%81%AA%E6%98%8E%E6%88%90%E8%BF%99%E6%A0%B7&t=31&band_rank=43&Refer=top)
1. [iPhone18Pro最高溢价3000元](https://s.weibo.com//weibo?q=%23iPhone18Pro%E6%9C%80%E9%AB%98%E6%BA%A2%E4%BB%B73000%E5%85%83%23&t=31&band_rank=44&Refer=top)
1. [说唱巅峰对决2026](https://s.weibo.com//weibo?q=%E8%AF%B4%E5%94%B1%E5%B7%85%E5%B3%B0%E5%AF%B9%E5%86%B32026&t=31&band_rank=45&Refer=top)
1. [SK 背锅](https://s.weibo.com//weibo?q=SK%20%E8%83%8C%E9%94%85&t=31&band_rank=46&Refer=top)
1. [支付宝 假APP](https://s.weibo.com//weibo?q=%E6%94%AF%E4%BB%98%E5%AE%9D%20%E5%81%87APP&t=31&band_rank=47&Refer=top)
1. [欧阳娜娜演唱会嘉宾是周翊然](https://s.weibo.com//weibo?q=%23%E6%AC%A7%E9%98%B3%E5%A8%9C%E5%A8%9C%E6%BC%94%E5%94%B1%E4%BC%9A%E5%98%89%E5%AE%BE%E6%98%AF%E5%91%A8%E7%BF%8A%E7%84%B6%23&t=31&band_rank=48&Refer=top)
1. [切尔西2比2赫尔城](https://s.weibo.com//weibo?q=%23%E5%88%87%E5%B0%94%E8%A5%BF2%E6%AF%942%E8%B5%AB%E5%B0%94%E5%9F%8E%23&t=31&band_rank=49&Refer=top)
1. [英超联赛](https://s.weibo.com//weibo?q=%E8%8B%B1%E8%B6%85%E8%81%94%E8%B5%9B&t=31&band_rank=50&Refer=top)
1. [你们经常换手机的人嘴真严](https://s.weibo.com//weibo?q=%23%E4%BD%A0%E4%BB%AC%E7%BB%8F%E5%B8%B8%E6%8D%A2%E6%89%8B%E6%9C%BA%E7%9A%84%E4%BA%BA%E5%98%B4%E7%9C%9F%E4%B8%A5%23&t=31&band_rank=1&Refer=top)
1. [TTG夺冠](https://s.weibo.com//weibo?q=TTG%E5%A4%BA%E5%86%A0&t=31&band_rank=2&Refer=top)
1. [AG 年总](https://s.weibo.com//weibo?q=AG%20%E5%B9%B4%E6%80%BB&t=31&band_rank=7&Refer=top)
1. [狼队 遗憾](https://s.weibo.com//weibo?q=%E7%8B%BC%E9%98%9F%20%E9%81%97%E6%86%BE&t=31&band_rank=9&Refer=top)
1. [兰香如故](https://s.weibo.com//weibo?q=%E5%85%B0%E9%A6%99%E5%A6%82%E6%95%85&t=31&band_rank=10&Refer=top)
1. [小胖现场喊天狼星天为首](https://s.weibo.com//weibo?q=%23%E5%B0%8F%E8%83%96%E7%8E%B0%E5%9C%BA%E5%96%8A%E5%A4%A9%E7%8B%BC%E6%98%9F%E5%A4%A9%E4%B8%BA%E9%A6%96%23&t=31&band_rank=11&Refer=top)
1. [市场监管局回应烧烤店2个月被查15次](https://s.weibo.com//weibo?q=%23%E5%B8%82%E5%9C%BA%E7%9B%91%E7%AE%A1%E5%B1%80%E5%9B%9E%E5%BA%94%E7%83%A7%E7%83%A4%E5%BA%972%E4%B8%AA%E6%9C%88%E8%A2%AB%E6%9F%A515%E6%AC%A1%23&t=31&band_rank=12&Refer=top)
1. [说唱巅峰对决2026](https://s.weibo.com//weibo?q=%E8%AF%B4%E5%94%B1%E5%B7%85%E5%B3%B0%E5%AF%B9%E5%86%B32026&t=31&band_rank=13&Refer=top)
1. [兰香如故走势](https://s.weibo.com//weibo?q=%23%E5%85%B0%E9%A6%99%E5%A6%82%E6%95%85%E8%B5%B0%E5%8A%BF%23&t=31&band_rank=14&Refer=top)
1. [小胖FMVP](https://s.weibo.com//weibo?q=%E5%B0%8F%E8%83%96FMVP&t=31&band_rank=15&Refer=top)
1. [小胖6冠4FMVP](https://s.weibo.com//weibo?q=%23%E5%B0%8F%E8%83%966%E5%86%A04FMVP%23&t=31&band_rank=16&Refer=top)
1. [张国伟说不会自己花钱练体育](https://s.weibo.com//weibo?q=%23%E5%BC%A0%E5%9B%BD%E4%BC%9F%E8%AF%B4%E4%B8%8D%E4%BC%9A%E8%87%AA%E5%B7%B1%E8%8A%B1%E9%92%B1%E7%BB%83%E4%BD%93%E8%82%B2%23&t=31&band_rank=17&Refer=top)
1. [梅姨除了心狠还狡猾多疑](https://s.weibo.com//weibo?q=%23%E6%A2%85%E5%A7%A8%E9%99%A4%E4%BA%86%E5%BF%83%E7%8B%A0%E8%BF%98%E7%8B%A1%E7%8C%BE%E5%A4%9A%E7%96%91%23&t=31&band_rank=18&Refer=top)
1. [15名同事合买彩票中奖3000万](https://s.weibo.com//weibo?q=%2315%E5%90%8D%E5%90%8C%E4%BA%8B%E5%90%88%E4%B9%B0%E5%BD%A9%E7%A5%A8%E4%B8%AD%E5%A5%963000%E4%B8%87%23&t=31&band_rank=19&Refer=top)
1. [举报文物失踪被查多次店主发声](https://s.weibo.com//weibo?q=%23%E4%B8%BE%E6%8A%A5%E6%96%87%E7%89%A9%E5%A4%B1%E8%B8%AA%E8%A2%AB%E6%9F%A5%E5%A4%9A%E6%AC%A1%E5%BA%97%E4%B8%BB%E5%8F%91%E5%A3%B0%23&t=31&band_rank=20&Refer=top)
1. [付航回应脱口秀禁黄牛票入场](https://s.weibo.com//weibo?q=%23%E4%BB%98%E8%88%AA%E5%9B%9E%E5%BA%94%E8%84%B1%E5%8F%A3%E7%A7%80%E7%A6%81%E9%BB%84%E7%89%9B%E7%A5%A8%E5%85%A5%E5%9C%BA%23&t=31&band_rank=21&Refer=top)
1. [Bin拒绝放狠话](https://s.weibo.com//weibo?q=%23Bin%E6%8B%92%E7%BB%9D%E6%94%BE%E7%8B%A0%E8%AF%9D%23&t=31&band_rank=22&Refer=top)
1. [想换手机的欲望突然到了极致](https://s.weibo.com//weibo?q=%E6%83%B3%E6%8D%A2%E6%89%8B%E6%9C%BA%E7%9A%84%E6%AC%B2%E6%9C%9B%E7%AA%81%E7%84%B6%E5%88%B0%E4%BA%86%E6%9E%81%E8%87%B4&t=31&band_rank=23&Refer=top)
1. [为什么几乎不存在完美藏尸](https://s.weibo.com//weibo?q=%E4%B8%BA%E4%BB%80%E4%B9%88%E5%87%A0%E4%B9%8E%E4%B8%8D%E5%AD%98%E5%9C%A8%E5%AE%8C%E7%BE%8E%E8%97%8F%E5%B0%B8&t=31&band_rank=24&Refer=top)
1. [心疼清清](https://s.weibo.com//weibo?q=%E5%BF%83%E7%96%BC%E6%B8%85%E6%B8%85&t=31&band_rank=25&Refer=top)
1. [一个妈妈在家做烤串的视频火了](https://s.weibo.com//weibo?q=%23%E4%B8%80%E4%B8%AA%E5%A6%88%E5%A6%88%E5%9C%A8%E5%AE%B6%E5%81%9A%E7%83%A4%E4%B8%B2%E7%9A%84%E8%A7%86%E9%A2%91%E7%81%AB%E4%BA%86%23&t=31&band_rank=26&Refer=top)
1. [苹果18 抢不到](https://s.weibo.com//weibo?q=%E8%8B%B9%E6%9E%9C18%20%E6%8A%A2%E4%B8%8D%E5%88%B0&t=31&band_rank=27&Refer=top)
1. [切尔西2比2赫尔城](https://s.weibo.com//weibo?q=%23%E5%88%87%E5%B0%94%E8%A5%BF2%E6%AF%942%E8%B5%AB%E5%B0%94%E5%9F%8E%23&t=31&band_rank=29&Refer=top)
1. [雨果4比2松岛辉空](https://s.weibo.com//weibo?q=%23%E9%9B%A8%E6%9E%9C4%E6%AF%942%E6%9D%BE%E5%B2%9B%E8%BE%89%E7%A9%BA%23&t=31&band_rank=30&Refer=top)
1. [iPhone18Pro系列抢购火爆](https://s.weibo.com//weibo?q=iPhone18Pro%E7%B3%BB%E5%88%97%E6%8A%A2%E8%B4%AD%E7%81%AB%E7%88%86&t=31&band_rank=31&Refer=top)
1. [iPhone18扣款成功仍等待付款](https://s.weibo.com//weibo?q=iPhone18%E6%89%A3%E6%AC%BE%E6%88%90%E5%8A%9F%E4%BB%8D%E7%AD%89%E5%BE%85%E4%BB%98%E6%AC%BE&t=31&band_rank=32&Refer=top)
1. [大姐购房父亲将402万房款分给两妹妹](https://s.weibo.com//weibo?q=%23%E5%A4%A7%E5%A7%90%E8%B4%AD%E6%88%BF%E7%88%B6%E4%BA%B2%E5%B0%86402%E4%B8%87%E6%88%BF%E6%AC%BE%E5%88%86%E7%BB%99%E4%B8%A4%E5%A6%B9%E5%A6%B9%23&t=31&band_rank=33&Refer=top)
1. [AL战胜iG](https://s.weibo.com//weibo?q=AL%E6%88%98%E8%83%9CiG&t=31&band_rank=34&Refer=top)
1. [兰香如故男扮女装美得出彩](https://s.weibo.com//weibo?q=%E5%85%B0%E9%A6%99%E5%A6%82%E6%95%85%E7%94%B7%E6%89%AE%E5%A5%B3%E8%A3%85%E7%BE%8E%E5%BE%97%E5%87%BA%E5%BD%A9&t=31&band_rank=35&Refer=top)
1. [狼队状态](https://s.weibo.com//weibo?q=%E7%8B%BC%E9%98%9F%E7%8A%B6%E6%80%81&t=31&band_rank=36&Refer=top)
1. [男子贷款60万开店2个月被差评干哭](https://s.weibo.com//weibo?q=%23%E7%94%B7%E5%AD%90%E8%B4%B7%E6%AC%BE60%E4%B8%87%E5%BC%80%E5%BA%972%E4%B8%AA%E6%9C%88%E8%A2%AB%E5%B7%AE%E8%AF%84%E5%B9%B2%E5%93%AD%23&t=31&band_rank=37&Refer=top)
1. [苏超](https://s.weibo.com//weibo?q=%E8%8B%8F%E8%B6%85&t=31&band_rank=38&Refer=top)
1. [IG冒泡赛面对TES](https://s.weibo.com//weibo?q=%23IG%E5%86%92%E6%B3%A1%E8%B5%9B%E9%9D%A2%E5%AF%B9TES%23&t=31&band_rank=39&Refer=top)
1. [茶叶蛋vs白煮蛋](https://s.weibo.com//weibo?q=%E8%8C%B6%E5%8F%B6%E8%9B%8Bvs%E7%99%BD%E7%85%AE%E8%9B%8B&t=31&band_rank=40&Refer=top)
1. [iPhone18Pro系列有多难抢](https://s.weibo.com//weibo?q=%23iPhone18Pro%E7%B3%BB%E5%88%97%E6%9C%89%E5%A4%9A%E9%9A%BE%E6%8A%A2%23&t=31&band_rank=41&Refer=top)
1. [欧阳娜娜演唱会嘉宾是周翊然](https://s.weibo.com//weibo?q=%23%E6%AC%A7%E9%98%B3%E5%A8%9C%E5%A8%9C%E6%BC%94%E5%94%B1%E4%BC%9A%E5%98%89%E5%AE%BE%E6%98%AF%E5%91%A8%E7%BF%8A%E7%84%B6%23&t=31&band_rank=42&Refer=top)
1. [狼队决赛巅峰对决TTG](https://s.weibo.com//weibo?q=%23%E7%8B%BC%E9%98%9F%E5%86%B3%E8%B5%9B%E5%B7%85%E5%B3%B0%E5%AF%B9%E5%86%B3TTG%23&t=31&band_rank=43&Refer=top)
1. [一条小团团首播](https://s.weibo.com//weibo?q=%23%E4%B8%80%E6%9D%A1%E5%B0%8F%E5%9B%A2%E5%9B%A2%E9%A6%96%E6%92%AD%23&t=31&band_rank=44&Refer=top)
1. [iPhone18Pro最高溢价3000元](https://s.weibo.com//weibo?q=%23iPhone18Pro%E6%9C%80%E9%AB%98%E6%BA%A2%E4%BB%B73000%E5%85%83%23&t=31&band_rank=45&Refer=top)
1. [支付宝 假APP](https://s.weibo.com//weibo?q=%E6%94%AF%E4%BB%98%E5%AE%9D%20%E5%81%87APP&t=31&band_rank=46&Refer=top)
1. [警方通报公职人员醉驾超速致人死亡](https://s.weibo.com//weibo?q=%23%E8%AD%A6%E6%96%B9%E9%80%9A%E6%8A%A5%E5%85%AC%E8%81%8C%E4%BA%BA%E5%91%98%E9%86%89%E9%A9%BE%E8%B6%85%E9%80%9F%E8%87%B4%E4%BA%BA%E6%AD%BB%E4%BA%A1%23&t=31&band_rank=47&Refer=top)
1. [肥肉煮熟切片包豆沙一个月卖8万元](https://s.weibo.com//weibo?q=%23%E8%82%A5%E8%82%89%E7%85%AE%E7%86%9F%E5%88%87%E7%89%87%E5%8C%85%E8%B1%86%E6%B2%99%E4%B8%80%E4%B8%AA%E6%9C%88%E5%8D%968%E4%B8%87%E5%85%83%23&t=31&band_rank=48&Refer=top)
1. [英超联赛](https://s.weibo.com//weibo?q=%E8%8B%B1%E8%B6%85%E8%81%94%E8%B5%9B&t=31&band_rank=49&Refer=top)
1. [东北超](https://s.weibo.com//weibo?q=%E4%B8%9C%E5%8C%97%E8%B6%85&t=31&band_rank=50&Refer=top)

<!-- END WEIBO -->

历史归档 [./archives/weibo-search](./archives/weibo-search)

## License

[trending-in-one/](https://github.com/cxyfreedom/trending-in-one) 的源码使用 MIT License 发布。具体内容请查看
[LICENSE](./LICENSE) 文件。

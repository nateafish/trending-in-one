# trending-in-one

> 本仓库基于上游项目 [huqi-pr/trending-in-one](https://github.com/huqi-pr/trending-in-one)
> 及其持续更新分支整理，补全了历史归档数据；内容由 GitHub Actions 自动抓取、归档并维护。

[![ci](https://github.com/nateafish/trending-in-one/actions/workflows/ci.yml/badge.svg)](https://github.com/nateafish/trending-in-one/actions/workflows/ci.yml)
[![license](https://img.shields.io/github/license/izukuuuu/trending-in-one)](https://github.com/nateafish/trending-in-one/blob/main/LICENSE)

今日头条热搜、知乎热搜榜、知乎热门话题、微博热搜榜；记录从 2020-11-29
日开始的热搜。每小时抓取一次数据，按天[归档](./archives)。知乎视频热榜已下线（2025-05
起停更），不再抓取，仅保留历史数据。

<!-- BEGIN ZHIHUCOOKIE -->

**知乎热榜 Cookie**：✅ 有效 ｜ 最近刷新：2026-08-07 13:14 ｜ 最近检测：2026-11-01 01:45:32

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
<!-- 最后更新时间 Sat Oct 31 2026 23:30:25 GMT+0800 (China Standard Time) -->

1. [无锡队苏超夺冠](https://so.toutiao.com/search?keyword=无锡队苏超夺冠)
1. [75岁傅成玉被查](https://so.toutiao.com/search?keyword=75岁傅成玉被查)
1. [以钉钉子精神加强党的作风建设](https://so.toutiao.com/search?keyword=以钉钉子精神加强党的作风建设)
1. [孙颖莎4-3险胜早田希娜 晋级4强](https://so.toutiao.com/search?keyword=孙颖莎4-3险胜早田希娜%20晋级4强)
1. [官方披露勒多曼因峰4人滑坠2人遇难](https://so.toutiao.com/search?keyword=官方披露勒多曼因峰4人滑坠2人遇难)
1. [人民日报评朱之文被“黑粉”举报](https://so.toutiao.com/search?keyword=人民日报评朱之文被“黑粉”举报)
1. [“存钱不如存肌肉”的时代来了](https://so.toutiao.com/search?keyword=“存钱不如存肌肉”的时代来了)
1. [因吃猪蹄住院女子从170斤瘦到88斤](https://so.toutiao.com/search?keyword=因吃猪蹄住院女子从170斤瘦到88斤)
1. [将有两名中国人登陆月球](https://so.toutiao.com/search?keyword=将有两名中国人登陆月球)
1. [江苏13城球员集体上手破除摸杯魔咒](https://so.toutiao.com/search?keyword=江苏13城球员集体上手破除摸杯魔咒)
1. [蓝盈莹斩获“年度魅力演员”](https://so.toutiao.com/search?keyword=蓝盈莹斩获“年度魅力演员”)
1. [男子自行吃壮阳保健品拖成癌症晚期](https://so.toutiao.com/search?keyword=男子自行吃壮阳保健品拖成癌症晚期)
1. [广西男子造谣“石场死了3个”被处罚](https://so.toutiao.com/search?keyword=广西男子造谣“石场死了3个”被处罚)
1. [六小龄童从猴哥变猴爷爷](https://so.toutiao.com/search?keyword=六小龄童从猴哥变猴爷爷)
1. [女子花3元买彩票中1439万](https://so.toutiao.com/search?keyword=女子花3元买彩票中1439万)
1. [大批理发店关停10元快剪走红](https://so.toutiao.com/search?keyword=大批理发店关停10元快剪走红)
1. [李乃文帮刘敏涛捡掉落的耳环](https://so.toutiao.com/search?keyword=李乃文帮刘敏涛捡掉落的耳环)
1. [徐志胜唱《逆战》开口就是全新版本](https://so.toutiao.com/search?keyword=徐志胜唱《逆战》开口就是全新版本)
1. [日本访华代表团鞠躬谢罪](https://so.toutiao.com/search?keyword=日本访华代表团鞠躬谢罪)
1. [夫妻因一餐5个菜闹到要离婚](https://so.toutiao.com/search?keyword=夫妻因一餐5个菜闹到要离婚)
1. [金饰克价年内跌了近550元](https://so.toutiao.com/search?keyword=金饰克价年内跌了近550元)
1. [一套房650万要缴450万的税](https://so.toutiao.com/search?keyword=一套房650万要缴450万的税)
1. [伊朗最高领袖：要对敌方威胁作立即回应](https://so.toutiao.com/search?keyword=伊朗最高领袖：要对敌方威胁作立即回应)
1. [柯文哲点名沈伯洋不肯回答市政问题](https://so.toutiao.com/search?keyword=柯文哲点名沈伯洋不肯回答市政问题)
1. [高颜值保洁大叔助阵辽超](https://so.toutiao.com/search?keyword=高颜值保洁大叔助阵辽超)
1. [未来十年普通人最该守住什么](https://so.toutiao.com/search?keyword=未来十年普通人最该守住什么)
1. [3种食物吃着不甜却会让血糖飙升](https://so.toutiao.com/search?keyword=3种食物吃着不甜却会让血糖飙升)
1. [男子醉酒昏迷40分钟朋友以为睡着了](https://so.toutiao.com/search?keyword=男子醉酒昏迷40分钟朋友以为睡着了)
1. [李昀锐获年度塑造力演员](https://so.toutiao.com/search?keyword=李昀锐获年度塑造力演员)
1. [今年全国实现生娃基本不花钱](https://so.toutiao.com/search?keyword=今年全国实现生娃基本不花钱)
1. [东哈烧烤老板娘现身苏超决赛现场](https://so.toutiao.com/search?keyword=东哈烧烤老板娘现身苏超决赛现场)
1. [朝鲜600毫米大口径火箭炮首次亮相](https://so.toutiao.com/search?keyword=朝鲜600毫米大口径火箭炮首次亮相)
1. [伦德伯格：库里大哥把困难摆平了](https://so.toutiao.com/search?keyword=伦德伯格：库里大哥把困难摆平了)
1. [胡歌陈龙解锁播报新体验](https://so.toutiao.com/search?keyword=胡歌陈龙解锁播报新体验)
1. [小沈阳披荆斩棘冠军](https://so.toutiao.com/search?keyword=小沈阳披荆斩棘冠军)
1. [李一桐黑白撞色礼服造型](https://so.toutiao.com/search?keyword=李一桐黑白撞色礼服造型)
1. [东契奇：喜欢和新队友们一起打球](https://so.toutiao.com/search?keyword=东契奇：喜欢和新队友们一起打球)
1. [东鹏特饮下架含姆巴佩头像的饮料](https://so.toutiao.com/search?keyword=东鹏特饮下架含姆巴佩头像的饮料)
1. [刘宇豪攻入个人苏超的第12球](https://so.toutiao.com/search?keyword=刘宇豪攻入个人苏超的第12球)
1. [古力娜扎直播卸妆像没卸](https://so.toutiao.com/search?keyword=古力娜扎直播卸妆像没卸)
1. [江西省委书记：航空产业其势已成](https://so.toutiao.com/search?keyword=江西省委书记：航空产业其势已成)
1. [全球资产价格下跌的根本逻辑是什么](https://so.toutiao.com/search?keyword=全球资产价格下跌的根本逻辑是什么)
1. [毛晓彤亮相微博视界大会红毯](https://so.toutiao.com/search?keyword=毛晓彤亮相微博视界大会红毯)
1. [老人离世 多年未探望亲闺女要分房产](https://so.toutiao.com/search?keyword=老人离世%20多年未探望亲闺女要分房产)
1. [芯片的大买主们快没钱了吗](https://so.toutiao.com/search?keyword=芯片的大买主们快没钱了吗)
1. [科技股“认清现实”的一周](https://so.toutiao.com/search?keyword=科技股“认清现实”的一周)
1. [比亚迪在欧洲再造一个比亚迪](https://so.toutiao.com/search?keyword=比亚迪在欧洲再造一个比亚迪)
1. [院士：国产算力不能只看芯片](https://so.toutiao.com/search?keyword=院士：国产算力不能只看芯片)
1. [中国海警位台湾岛以东海域执法巡查](https://so.toutiao.com/search?keyword=中国海警位台湾岛以东海域执法巡查)
1. [有小缺陷的刘铮亮吸引了肖战](https://so.toutiao.com/search?keyword=有小缺陷的刘铮亮吸引了肖战)
1. [官方披露：将有两名中国人登陆月球](https://so.toutiao.com/search?keyword=官方披露：将有两名中国人登陆月球)
1. [保持定力持之以恒推进全面从严治党](https://so.toutiao.com/search?keyword=保持定力持之以恒推进全面从严治党)
1. [钓鱼男子被钱塘江涌潮吞没后游上岸](https://so.toutiao.com/search?keyword=钓鱼男子被钱塘江涌潮吞没后游上岸)
1. [梦舟载人飞船和揽月着陆器将首次飞行](https://so.toutiao.com/search?keyword=梦舟载人飞船和揽月着陆器将首次飞行)
1. [日代表团：掘开侵华日军坟墓让其谢罪](https://so.toutiao.com/search?keyword=日代表团：掘开侵华日军坟墓让其谢罪)
1. [“假笑男孩”16岁了](https://so.toutiao.com/search?keyword=“假笑男孩”16岁了)
1. [红军破险篇 驳“放水论”](https://so.toutiao.com/search?keyword=红军破险篇%20驳“放水论”)
1. [刘恺威与小20岁女友甜蜜互动曝光](https://so.toutiao.com/search?keyword=刘恺威与小20岁女友甜蜜互动曝光)
1. [NASA局长为何拿中国登月说事](https://so.toutiao.com/search?keyword=NASA局长为何拿中国登月说事)
1. [中国找矿获重大突破](https://so.toutiao.com/search?keyword=中国找矿获重大突破)
1. [勒布伦2比1孙颖莎](https://so.toutiao.com/search?keyword=勒布伦2比1孙颖莎)
1. [意大利50多个城市爆发示威游行](https://so.toutiao.com/search?keyword=意大利50多个城市爆发示威游行)
1. [官方通报村支书威胁环保博主](https://so.toutiao.com/search?keyword=官方通报村支书威胁环保博主)
1. [“共享儿女”试点：每月最低199元](https://so.toutiao.com/search?keyword=“共享儿女”试点：每月最低199元)
1. [昂跑未宣布与姆巴佩解约](https://so.toutiao.com/search?keyword=昂跑未宣布与姆巴佩解约)
1. [孟加拉国总理无视引导不向日国旗鞠躬](https://so.toutiao.com/search?keyword=孟加拉国总理无视引导不向日国旗鞠躬)
1. [《征服》各演员近况如何](https://so.toutiao.com/search?keyword=《征服》各演员近况如何)
1. [邵永灵谈中国载人登月方案](https://so.toutiao.com/search?keyword=邵永灵谈中国载人登月方案)
1. [军报：广大官兵坚决拥护党中央决定](https://so.toutiao.com/search?keyword=军报：广大官兵坚决拥护党中央决定)
1. [尹锡悦会被判死刑吗](https://so.toutiao.com/search?keyword=尹锡悦会被判死刑吗)
1. [白宇帆发文承认已有孩子](https://so.toutiao.com/search?keyword=白宇帆发文承认已有孩子)
1. [俄外长：乌方破坏会谈氛围](https://so.toutiao.com/search?keyword=俄外长：乌方破坏会谈氛围)
1. [G20外长会取消合影 俄德外长交锋](https://so.toutiao.com/search?keyword=G20外长会取消合影%20俄德外长交锋)
1. [华尔街大逃亡 黄金股票被无差别抛售](https://so.toutiao.com/search?keyword=华尔街大逃亡%20黄金股票被无差别抛售)
1. [闫妮携女儿现身大孤山](https://so.toutiao.com/search?keyword=闫妮携女儿现身大孤山)
1. [芯片公司股价为何暴跌](https://so.toutiao.com/search?keyword=芯片公司股价为何暴跌)
1. [DeepSeek联手华为能否击穿英伟达CUDA](https://so.toutiao.com/search?keyword=DeepSeek联手华为能否击穿英伟达CUDA)
1. [撞脸王祖贤女生去景区上班](https://so.toutiao.com/search?keyword=撞脸王祖贤女生去景区上班)
1. [邵永灵：“特朗普经济学”惨败](https://so.toutiao.com/search?keyword=邵永灵：“特朗普经济学”惨败)
1. [黑龙江省秋收生产基本结束](https://so.toutiao.com/search?keyword=黑龙江省秋收生产基本结束)
1. [波兰抗议风波因何而起](https://so.toutiao.com/search?keyword=波兰抗议风波因何而起)
1. [“攻击-21”成功起降](https://so.toutiao.com/search?keyword=“攻击-21”成功起降)
1. [如何看待乌一枚拦截弹击落两枚导弹](https://so.toutiao.com/search?keyword=如何看待乌一枚拦截弹击落两枚导弹)
1. [郑丽文批民进党为假议题对立撕裂](https://so.toutiao.com/search?keyword=郑丽文批民进党为假议题对立撕裂)
1. [大衣哥将迎11月首场演出](https://so.toutiao.com/search?keyword=大衣哥将迎11月首场演出)
1. [俄军为何专打北约共用枢纽](https://so.toutiao.com/search?keyword=俄军为何专打北约共用枢纽)
1. [专家：民进党无牌可打](https://so.toutiao.com/search?keyword=专家：民进党无牌可打)
1. [英国为何要求家庭准备物资](https://so.toutiao.com/search?keyword=英国为何要求家庭准备物资)
1. [普通人每天吃多少鸡蛋才科学](https://so.toutiao.com/search?keyword=普通人每天吃多少鸡蛋才科学)
1. [庞博孙乐言主持微博视界大会](https://so.toutiao.com/search?keyword=庞博孙乐言主持微博视界大会)
1. [波兰发生政变？总统紧急回国](https://so.toutiao.com/search?keyword=波兰发生政变？总统紧急回国)
1. [全面从严治党和鼓励担当作为内在统一](https://so.toutiao.com/search?keyword=全面从严治党和鼓励担当作为内在统一)
1. [纳指跌近3%英特尔创52年来最大日跌幅](https://so.toutiao.com/search?keyword=纳指跌近3%英特尔创52年来最大日跌幅)
1. [攻击21在四川舰上完成起降意味什么](https://so.toutiao.com/search?keyword=攻击21在四川舰上完成起降意味什么)
1. [黄金大跌 铜价为何创新高](https://so.toutiao.com/search?keyword=黄金大跌%20铜价为何创新高)
1. [WTT蒙彼利埃冠军赛男单8强诞生](https://so.toutiao.com/search?keyword=WTT蒙彼利埃冠军赛男单8强诞生)
1. [辟谣周榜｜辽宁大暴雨街道成海？假的](https://so.toutiao.com/search?keyword=辟谣周榜｜辽宁大暴雨街道成海？假的)
1. [校方再回应新生摆拍大体老师头骨](https://so.toutiao.com/search?keyword=校方再回应新生摆拍大体老师头骨)
1. [共享单车悄悄变贵了](https://so.toutiao.com/search?keyword=共享单车悄悄变贵了)
1. [新人包双层巴士和复古铛铛车接亲](https://so.toutiao.com/search?keyword=新人包双层巴士和复古铛铛车接亲)
1. [iPhone Duo的铰链是AI打造的吗](https://so.toutiao.com/search?keyword=iPhone%20Duo的铰链是AI打造的吗)
1. [小沈阳发文告别《披荆斩棘》](https://so.toutiao.com/search?keyword=小沈阳发文告别《披荆斩棘》)
1. [马斯克脑机接口最狠升级](https://so.toutiao.com/search?keyword=马斯克脑机接口最狠升级)
1. [于东来：建议制度支持消费入座](https://so.toutiao.com/search?keyword=于东来：建议制度支持消费入座)
1. [德国总统访华现场视频](https://so.toutiao.com/search?keyword=德国总统访华现场视频)
1. [遗体捐献对医学院意味着什么](https://so.toutiao.com/search?keyword=遗体捐献对医学院意味着什么)
1. [德总统夫妇在北京人艺观看《李白》](https://so.toutiao.com/search?keyword=德总统夫妇在北京人艺观看《李白》)
1. [中美科技公司估值为何差这么多](https://so.toutiao.com/search?keyword=中美科技公司估值为何差这么多)
1. [钱学森逝世17周年](https://so.toutiao.com/search?keyword=钱学森逝世17周年)
1. [选民嘴瓢喊万斯“总统先生”](https://so.toutiao.com/search?keyword=选民嘴瓢喊万斯“总统先生”)
1. [周启豪展望四分之一决赛](https://so.toutiao.com/search?keyword=周启豪展望四分之一决赛)
1. [菲军舰“跟踪”辽宁舰这场戏演给谁看](https://so.toutiao.com/search?keyword=菲军舰“跟踪”辽宁舰这场戏演给谁看)
1. [赵心童坦然接纳外界的声音](https://so.toutiao.com/search?keyword=赵心童坦然接纳外界的声音)
1. [机器人可以理解世界吗](https://so.toutiao.com/search?keyword=机器人可以理解世界吗)
1. [何炅被杨丽萍当场说哭](https://so.toutiao.com/search?keyword=何炅被杨丽萍当场说哭)
1. [美批准向乌出售500枚“爱国者”导弹](https://so.toutiao.com/search?keyword=美批准向乌出售500枚“爱国者”导弹)
1. [美官员称要“烦死”选民催投票](https://so.toutiao.com/search?keyword=美官员称要“烦死”选民催投票)
1. [热火给韦德雕像做了“换头手术”](https://so.toutiao.com/search?keyword=热火给韦德雕像做了“换头手术”)
1. [53岁阿姨减重15.8公斤 血糖实现逆转](https://so.toutiao.com/search?keyword=53岁阿姨减重15.8公斤%20血糖实现逆转)
1. [阿云嘎获《披荆斩棘》年度滚烫X-FIRE](https://so.toutiao.com/search?keyword=阿云嘎获《披荆斩棘》年度滚烫X-FIRE)
1. [《小城良方》制作方起诉一用户](https://so.toutiao.com/search?keyword=《小城良方》制作方起诉一用户)
1. [泽连斯基制裁俄版“星链”产业链](https://so.toutiao.com/search?keyword=泽连斯基制裁俄版“星链”产业链)
1. [《披荆斩棘2026》滚烫家族诞生](https://so.toutiao.com/search?keyword=《披荆斩棘2026》滚烫家族诞生)
1. [马斯克公司为何能影响战场通信](https://so.toutiao.com/search?keyword=马斯克公司为何能影响战场通信)
1. [为什么说23点后睡觉的人亏大了](https://so.toutiao.com/search?keyword=为什么说23点后睡觉的人亏大了)
1. [中国女子在西班牙因赖床错过事故列车](https://so.toutiao.com/search?keyword=中国女子在西班牙因赖床错过事故列车)
1. [CBA常规赛宁波町渥不敌辽宁本钢](https://so.toutiao.com/search?keyword=CBA常规赛宁波町渥不敌辽宁本钢)
1. [第一个15万亿经济大省要来了吗](https://so.toutiao.com/search?keyword=第一个15万亿经济大省要来了吗)
1. [《影之刃零》展现国产游戏怎样的处境](https://so.toutiao.com/search?keyword=《影之刃零》展现国产游戏怎样的处境)
1. [美科技巨头面临估值重估](https://so.toutiao.com/search?keyword=美科技巨头面临估值重估)
1. [研报：紧缩预期强化 金银分化寻底](https://so.toutiao.com/search?keyword=研报：紧缩预期强化%20金银分化寻底)
1. [长城汽车第三季度利润下滑超37%](https://so.toutiao.com/search?keyword=长城汽车第三季度利润下滑超37%)
1. [男孩不爱吃饭医生点肯德基当场治好](https://so.toutiao.com/search?keyword=男孩不爱吃饭医生点肯德基当场治好)
1. [邵永灵：乌克兰低头了](https://so.toutiao.com/search?keyword=邵永灵：乌克兰低头了)
1. [女生田径比赛跌倒爬过终点仍是第一](https://so.toutiao.com/search?keyword=女生田径比赛跌倒爬过终点仍是第一)
1. [男子负债千万后“净身出户”被判无效](https://so.toutiao.com/search?keyword=男子负债千万后“净身出户”被判无效)
1. [人民日报：警惕“中国AI跑偏论”](https://so.toutiao.com/search?keyword=人民日报：警惕“中国AI跑偏论”)
1. [女子万元手机火车上充电时被顺走](https://so.toutiao.com/search?keyword=女子万元手机火车上充电时被顺走)
1. [北京启动2026年网络辟谣宣传月活动](https://so.toutiao.com/search?keyword=北京启动2026年网络辟谣宣传月活动)
1. [72岁成龙展示一身紧实肌肉](https://so.toutiao.com/search?keyword=72岁成龙展示一身紧实肌肉)
1. [中国稀土股票11月2日起停牌](https://so.toutiao.com/search?keyword=中国稀土股票11月2日起停牌)
1. [媒体：银行“离柜概不负责”早该撤了](https://so.toutiao.com/search?keyword=媒体：银行“离柜概不负责”早该撤了)
1. [证监会：全力稳市场稳预期](https://so.toutiao.com/search?keyword=证监会：全力稳市场稳预期)
1. [理想i6卸掉宁德时代电池](https://so.toutiao.com/search?keyword=理想i6卸掉宁德时代电池)
1. [谁在牵引金价走势](https://so.toutiao.com/search?keyword=谁在牵引金价走势)
1. [中组部：解决“干好干坏一个样”问题](https://so.toutiao.com/search?keyword=中组部：解决“干好干坏一个样”问题)
1. [男子在星巴克不消费占座被劝离后报警](https://so.toutiao.com/search?keyword=男子在星巴克不消费占座被劝离后报警)
1. [为何说辽宁舰穿越菲腹地给美出难题](https://so.toutiao.com/search?keyword=为何说辽宁舰穿越菲腹地给美出难题)
1. [陈熠3-0淘汰王曼昱](https://so.toutiao.com/search?keyword=陈熠3-0淘汰王曼昱)
1. [历史数据复盘：沪指11月上涨比例60%](https://so.toutiao.com/search?keyword=历史数据复盘：沪指11月上涨比例60%)
1. [官方介绍五中全会最重要成果](https://so.toutiao.com/search?keyword=官方介绍五中全会最重要成果)
1. [邵永灵：乌克兰要把俄罗斯赶出联合国](https://so.toutiao.com/search?keyword=邵永灵：乌克兰要把俄罗斯赶出联合国)
1. [乌方：泽连斯基愿与普京磋商领土议题](https://so.toutiao.com/search?keyword=乌方：泽连斯基愿与普京磋商领土议题)
1. [小米出资17亿元入股欣旺达动力](https://so.toutiao.com/search?keyword=小米出资17亿元入股欣旺达动力)
1. [A股暖性因子吹响集结号](https://so.toutiao.com/search?keyword=A股暖性因子吹响集结号)
1. [英国为何要加码对乌克兰援助](https://so.toutiao.com/search?keyword=英国为何要加码对乌克兰援助)
1. [邀全网喝喜酒小伙家里布置1万枝玫瑰](https://so.toutiao.com/search?keyword=邀全网喝喜酒小伙家里布置1万枝玫瑰)
1. [中方驳斥女情报人员接触黄仁勋报道](https://so.toutiao.com/search?keyword=中方驳斥女情报人员接触黄仁勋报道)
1. [绕过不友好国家 俄外长穿休闲装抵美](https://so.toutiao.com/search?keyword=绕过不友好国家%20俄外长穿休闲装抵美)
1. [以色列为何再次陷入组阁僵局](https://so.toutiao.com/search?keyword=以色列为何再次陷入组阁僵局)
1. [台北选情激烈 白营选民成最大变量](https://so.toutiao.com/search?keyword=台北选情激烈%20白营选民成最大变量)
1. [朱之文回应遭黑粉举报：遇到软暴力](https://so.toutiao.com/search?keyword=朱之文回应遭黑粉举报：遇到软暴力)
1. [媒体：“离柜概不负责”别单向约束储户](https://so.toutiao.com/search?keyword=媒体：“离柜概不负责”别单向约束储户)
1. [沈晓明辞去湖南省人大常委会主任职务](https://so.toutiao.com/search?keyword=沈晓明辞去湖南省人大常委会主任职务)
1. [黄金消费回归性价比金饰品牌如何赚钱](https://so.toutiao.com/search?keyword=黄金消费回归性价比金饰品牌如何赚钱)
1. [台湾地区三大选举“奇观”](https://so.toutiao.com/search?keyword=台湾地区三大选举“奇观”)
1. [塞尔维亚前进党将启动改革计划](https://so.toutiao.com/search?keyword=塞尔维亚前进党将启动改革计划)
1. [我军飞行员喊话菲军机立即离开](https://so.toutiao.com/search?keyword=我军飞行员喊话菲军机立即离开)
1. [日本搞新型军国主义 德国要掺和吗](https://so.toutiao.com/search?keyword=日本搞新型军国主义%20德国要掺和吗)
1. [张雪替员工付首付](https://so.toutiao.com/search?keyword=张雪替员工付首付)
1. [小鹏汇天创始人谈特斯拉飞车](https://so.toutiao.com/search?keyword=小鹏汇天创始人谈特斯拉飞车)
1. [APEC工商领导人峰会美企报名踊跃](https://so.toutiao.com/search?keyword=APEC工商领导人峰会美企报名踊跃)
1. [横店系资本投了DeepSeek](https://so.toutiao.com/search?keyword=横店系资本投了DeepSeek)
1. [美国为何要北约盟友别挑衅俄罗斯](https://so.toutiao.com/search?keyword=美国为何要北约盟友别挑衅俄罗斯)
1. [武汉一企业向全球译制超2万部短剧](https://so.toutiao.com/search?keyword=武汉一企业向全球译制超2万部短剧)
1. [中国内地航线燃油附加费将上调](https://so.toutiao.com/search?keyword=中国内地航线燃油附加费将上调)
1. [《后会友期》是《再见爱人》代餐吗](https://so.toutiao.com/search?keyword=《后会友期》是《再见爱人》代餐吗)
1. [美国中期选举将如何影响资本市场](https://so.toutiao.com/search?keyword=美国中期选举将如何影响资本市场)
1. [长鑫科技Q3归母净利润544.35亿](https://so.toutiao.com/search?keyword=长鑫科技Q3归母净利润544.35亿)
1. [全球最大加密货币交易所疑遭黑客盗窃](https://so.toutiao.com/search?keyword=全球最大加密货币交易所疑遭黑客盗窃)
1. [爱尔兰将研究与北爱尔兰统一可能性](https://so.toutiao.com/search?keyword=爱尔兰将研究与北爱尔兰统一可能性)

<!-- END TOUTIAO -->

历史归档 [./archives/toutiao-search](./archives/toutiao-search)

## 知乎热搜榜

<!-- BEGIN ZHIHUSEARCH -->
<!-- 最后更新时间 Sun Nov 01 2026 01:42:09 GMT+0800 (China Standard Time) -->

1. [姆巴佩恐面临天文数字赔偿](https://www.zhihu.com/search?q=%E5%A7%86%E5%B7%B4%E4%BD%A9%E6%81%90%E9%9D%A2%E4%B8%B4%E5%A4%A9%E6%96%87%E6%95%B0%E5%AD%97%E8%B5%94%E5%81%BF)
1. [反诈博主徽剑被曝遇害](https://www.zhihu.com/search?q=%E5%8F%8D%E8%AF%88%E5%8D%9A%E4%B8%BB%E5%BE%BD%E5%89%91%E8%A2%AB%E6%9B%9D%E9%81%87%E5%AE%B3)
1. [摆拍大体老师头骨的学生被处分](https://www.zhihu.com/search?q=%E6%91%86%E6%8B%8D%E5%A4%A7%E4%BD%93%E8%80%81%E5%B8%88%E5%A4%B4%E9%AA%A8%E7%9A%84%E5%AD%A6%E7%94%9F%E8%A2%AB%E5%A4%84%E5%88%86)
1. [好奇岛装扮游戏](https://www.zhihu.com/search?q=%E5%A5%BD%E5%A5%87%E5%B2%9B%E8%A3%85%E6%89%AE%E6%B8%B8%E6%88%8F)
1. [波兰总理趁总统外访发动政变](https://www.zhihu.com/search?q=%E6%B3%A2%E5%85%B0%E6%80%BB%E7%90%86%E8%B6%81%E6%80%BB%E7%BB%9F%E5%A4%96%E8%AE%BF%E5%8F%91%E5%8A%A8%E6%94%BF%E5%8F%98)
1. [将有两名中国人登陆月球](https://www.zhihu.com/search?q=%E5%B0%86%E6%9C%89%E4%B8%A4%E5%90%8D%E4%B8%AD%E5%9B%BD%E4%BA%BA%E7%99%BB%E9%99%86%E6%9C%88%E7%90%83)
1. [10月30日A股集体收跌](https://www.zhihu.com/search?q=10%E6%9C%8830%E6%97%A5A%E8%82%A1%E9%9B%86%E4%BD%93%E6%94%B6%E8%B7%8C)
1. [四川悬崖秋千致游客死亡调查公布](https://www.zhihu.com/search?q=%E5%9B%9B%E5%B7%9D%E6%82%AC%E5%B4%96%E7%A7%8B%E5%8D%83%E8%87%B4%E6%B8%B8%E5%AE%A2%E6%AD%BB%E4%BA%A1%E8%B0%83%E6%9F%A5%E5%85%AC%E5%B8%83)
1. [DeepSeek发布super-agent构想](https://www.zhihu.com/search?q=DeepSeek%E5%8F%91%E5%B8%83super-agent%E6%9E%84%E6%83%B3)
1. [苏超决赛无锡2-1常州](https://www.zhihu.com/search?q=%E8%8B%8F%E8%B6%85%E5%86%B3%E8%B5%9B%E6%97%A0%E9%94%A12-1%E5%B8%B8%E5%B7%9E)
1. [英特尔股价创52年来最大日跌幅](https://www.zhihu.com/search?q=%E8%8B%B1%E7%89%B9%E5%B0%94%E8%82%A1%E4%BB%B7%E5%88%9B52%E5%B9%B4%E6%9D%A5%E6%9C%80%E5%A4%A7%E6%97%A5%E8%B7%8C%E5%B9%85)
1. [中科大给学生提供每日百元token](https://www.zhihu.com/search?q=%E4%B8%AD%E7%A7%91%E5%A4%A7%E7%BB%99%E5%AD%A6%E7%94%9F%E6%8F%90%E4%BE%9B%E6%AF%8F%E6%97%A5%E7%99%BE%E5%85%83token)

<!-- END ZHIHUSEARCH -->

历史归档 [./archives/zhihu-search](./archives/zhihu-search)

## 知乎热门话题

<!-- BEGIN ZHIHUQUESTIONS -->
<!-- 最后更新时间 Sun Nov 01 2026 01:45:32 GMT+0800 (China Standard Time) -->

1. [我国首次载人登月任务乘组计划由三人组成，两人着陆月球表面，哪些细节值得关注？此次任务重点在哪？](https://www.zhihu.com/question/2099856268898690000)
1. [红果短剧年营收超150亿，为什么有创作者称两个月11部剧只赚了9块6？](https://www.zhihu.com/question/2099456582853605400)
1. [如何评价理想、小米成欣旺达动力第二、第三大股东？](https://www.zhihu.com/question/2099592453800182500)
1. [西方发达国家那种木头房子，美观成本低、寿命又长，特别是抗震性能好，为何不在我国地震带地区推广呢？](https://www.zhihu.com/question/2098749313132269800)
1. [双缝干涉实验恐怖在哪？能用通俗易懂语言解释吗？](https://www.zhihu.com/question/329927724)
1. [黄金跌破3900美元、白银失守50美元，这一轮从历史高点的回落，是深度调整还是大级别上涨行情已经终结？](https://www.zhihu.com/question/2099634904501842200)
1. [同级同事在工作群直接指出我的工作错误，我承认自己的疏忽并表示会尽快修正，但对方抓住不放，怎么办？](https://www.zhihu.com/question/2098152098923919000)
1. [胡辣汤、泡馍这么御寒的食物，为什么没能在寒冷的东北流行起来？](https://www.zhihu.com/question/1973850877744916000)
1. [如何看待网友提出「初中禁绝游戏和电子产品，培养看云发呆的爱好，长大一天吃一个白面馒头也很开心」的观点？](https://www.zhihu.com/question/2098120639785841400)
1. [如何看待「三年内，扩散模型将全面替代大语言模型」的说法？这会给 AI Infra 带来哪些变化？](https://www.zhihu.com/question/2098823323752690400)
1. [国内游戏界的奇耻大辱（事件、现状等等）是什么？](https://www.zhihu.com/question/1932369918818484200)
1. [古风歌手吾恩已离世，与胃癌抗争近七年，曾有代表作《忘羡》《人间纵我》等，你对他有哪些印象？](https://www.zhihu.com/question/2099784358110257400)
1. [孙颖莎 4：3战胜早田希娜，晋级 WTT 蒙彼利埃冠军赛四强，如何评价本场比赛？](https://www.zhihu.com/question/2099997199270782500)
1. [2026年苏超总决赛，无锡 2-1 常州夺下冠军，如何评价本场比赛？](https://www.zhihu.com/question/2099949215132509400)
1. [懂球帝做错了吗？为什么要开始指责传播渠道，根源不是在姆巴佩吗？](https://www.zhihu.com/question/2099503804379145500)
1. [今年全国实现生娃基本不花钱，多地密集出台生育支持措施，涉及哪些方面？会带来哪些积极影响？](https://www.zhihu.com/question/2099768069723612000)
1. [人民锐评发文驳斥「中国 AI 跑偏论」，如何看待中美在 AI 落地路径上的差异？](https://www.zhihu.com/question/2099418216976102400)
1. [到底是编剧的水平问题，还是投资方的问题造成现在影视作品烂?](https://www.zhihu.com/question/10252504019)
1. [接触过一些身居高位的领导，感觉到他们的情绪都很稳定，这种观察普遍成立吗？](https://www.zhihu.com/question/2097963728851550700)
1. [游戏《影之刃零》有哪些轮椅武器或者道具、打法？](https://www.zhihu.com/question/2098861847550214100)
1. [杨奇称《黑神话》坚持三部曲且团队上限卡在 180 人，如何看待这一开发策略？](https://www.zhihu.com/question/2099641705439965700)
1. [没有世界杯冠军但是斩获2026金球奖，你觉得凯恩优秀在哪里？](https://www.zhihu.com/question/2098396530176685300)
1. [辽宁明明是一个东部沿海先发省份，为什么很多人印象中辽宁还是东北苦寒之地呢？](https://www.zhihu.com/question/2076754503601239600)
1. [「豆包们」正在成为医患之间的「第三人」，大量 AI 问诊对门诊医生造成了什么影响？会有哪些困扰？](https://www.zhihu.com/question/2096595801644299500)
1. [网上对心理学的负面评价很多，张雪峰老师也说它是天坑，那我这样的想法适合学心理学吗？](https://www.zhihu.com/question/2074878871351174400)
1. [网友无意中摔坏孩子的双层保温碗，发现里面满是霉菌，水都是臭的，为啥会这样？使用这种碗有啥风险？](https://www.zhihu.com/question/2096642260750357200)
1. [2627赛季英超联赛英超第9轮切尔西 2:0 曼联，如何评价这场比赛？](https://www.zhihu.com/question/2099963072882525000)
1. [阿维塔新车发布会取消，具体是咋回事？背后的原因可能是啥？](https://www.zhihu.com/question/2099095002139681300)
1. [如何评价芒果 TV 推出的友情治愈纪实真人秀《后会友期》？](https://www.zhihu.com/question/2096625673792238300)
1. [“天然良港”需要怎样的条件？](https://www.zhihu.com/question/31365407)

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
<!-- 最后更新时间 Sun Nov 01 2026 01:50:27 GMT+0800 (China Standard Time) -->

1. [近5000字公报严字贯穿始终](https://s.weibo.com//weibo?q=%23%E8%BF%915000%E5%AD%97%E5%85%AC%E6%8A%A5%E4%B8%A5%E5%AD%97%E8%B4%AF%E7%A9%BF%E5%A7%8B%E7%BB%88%23&Refer=new_time)
1. [苹果Duo中国版被指偷工减料](https://s.weibo.com//weibo?q=%E8%8B%B9%E6%9E%9CDuo%E4%B8%AD%E5%9B%BD%E7%89%88%E8%A2%AB%E6%8C%87%E5%81%B7%E5%B7%A5%E5%87%8F%E6%96%99&t=31&band_rank=1&Refer=top)
1. [孙颖莎把早田希娜打哭了](https://s.weibo.com//weibo?q=%E5%AD%99%E9%A2%96%E8%8E%8E%E6%8A%8A%E6%97%A9%E7%94%B0%E5%B8%8C%E5%A8%9C%E6%89%93%E5%93%AD%E4%BA%86&t=31&band_rank=2&Refer=top)
1. [五中全会释放了哪些信号](https://s.weibo.com//weibo?q=%23%E4%BA%94%E4%B8%AD%E5%85%A8%E4%BC%9A%E9%87%8A%E6%94%BE%E4%BA%86%E5%93%AA%E4%BA%9B%E4%BF%A1%E5%8F%B7%23&t=31&band_rank=3&Refer=top)
1. [王子璇 文吉儿](https://s.weibo.com//weibo?q=%E7%8E%8B%E5%AD%90%E7%92%87%20%E6%96%87%E5%90%89%E5%84%BF&t=31&band_rank=4&Refer=top)
1. [刘诗诗牵着关晓彤上台](https://s.weibo.com//weibo?q=%E5%88%98%E8%AF%97%E8%AF%97%E7%89%B5%E7%9D%80%E5%85%B3%E6%99%93%E5%BD%A4%E4%B8%8A%E5%8F%B0&t=31&band_rank=5&Refer=top)
1. [侯卓成杨汝晴官宣分手](https://s.weibo.com//weibo?q=%23%E4%BE%AF%E5%8D%93%E6%88%90%E6%9D%A8%E6%B1%9D%E6%99%B4%E5%AE%98%E5%AE%A3%E5%88%86%E6%89%8B%23&t=31&band_rank=6&Refer=top)
1. [姑娘别哭 真人好年轻](https://s.weibo.com//weibo?q=%E5%A7%91%E5%A8%98%E5%88%AB%E5%93%AD%20%E7%9C%9F%E4%BA%BA%E5%A5%BD%E5%B9%B4%E8%BD%BB&t=31&band_rank=7&Refer=top)
1. [4AM任和咚咚和好了](https://s.weibo.com//weibo?q=%234AM%E4%BB%BB%E5%92%8C%E5%92%9A%E5%92%9A%E5%92%8C%E5%A5%BD%E4%BA%86%23&t=31&band_rank=8&Refer=top)
1. [蔡磊想通过脑机接口拥抱儿子](https://s.weibo.com//weibo?q=%23%E8%94%A1%E7%A3%8A%E6%83%B3%E9%80%9A%E8%BF%87%E8%84%91%E6%9C%BA%E6%8E%A5%E5%8F%A3%E6%8B%A5%E6%8A%B1%E5%84%BF%E5%AD%90%23&t=31&band_rank=9&Refer=top)
1. [孙颖莎决胜局9比9敢出手](https://s.weibo.com//weibo?q=%E5%AD%99%E9%A2%96%E8%8E%8E%E5%86%B3%E8%83%9C%E5%B1%809%E6%AF%949%E6%95%A2%E5%87%BA%E6%89%8B&t=31&band_rank=10&Refer=top)
1. [被文吉儿霸凌当事人回应](https://s.weibo.com//weibo?q=%23%E8%A2%AB%E6%96%87%E5%90%89%E5%84%BF%E9%9C%B8%E5%87%8C%E5%BD%93%E4%BA%8B%E4%BA%BA%E5%9B%9E%E5%BA%94%23&t=31&band_rank=11&Refer=top)
1. [奔跑吧厉娜](https://s.weibo.com//weibo?q=%23%E5%A5%94%E8%B7%91%E5%90%A7%E5%8E%89%E5%A8%9C%23&t=31&band_rank=12&Refer=top)
1. [后会友期导演好听劝](https://s.weibo.com//weibo?q=%23%E5%90%8E%E4%BC%9A%E5%8F%8B%E6%9C%9F%E5%AF%BC%E6%BC%94%E5%A5%BD%E5%90%AC%E5%8A%9D%23&t=31&band_rank=13&Refer=top)
1. [孟子义看到刘学义躲镜头的表情](https://s.weibo.com//weibo?q=%23%E5%AD%9F%E5%AD%90%E4%B9%89%E7%9C%8B%E5%88%B0%E5%88%98%E5%AD%A6%E4%B9%89%E8%BA%B2%E9%95%9C%E5%A4%B4%E7%9A%84%E8%A1%A8%E6%83%85%23&t=31&band_rank=14&Refer=top)
1. [肖战刘铮亮差点喜提三个前女友](https://s.weibo.com//weibo?q=%23%E8%82%96%E6%88%98%E5%88%98%E9%93%AE%E4%BA%AE%E5%B7%AE%E7%82%B9%E5%96%9C%E6%8F%90%E4%B8%89%E4%B8%AA%E5%89%8D%E5%A5%B3%E5%8F%8B%23&t=31&band_rank=15&Refer=top)
1. [女子注射生长因子脸疯长成畸形](https://s.weibo.com//weibo?q=%23%E5%A5%B3%E5%AD%90%E6%B3%A8%E5%B0%84%E7%94%9F%E9%95%BF%E5%9B%A0%E5%AD%90%E8%84%B8%E7%96%AF%E9%95%BF%E6%88%90%E7%95%B8%E5%BD%A2%23&t=31&band_rank=16&Refer=top)
1. [厉娜评论区打脸来得太快](https://s.weibo.com//weibo?q=%E5%8E%89%E5%A8%9C%E8%AF%84%E8%AE%BA%E5%8C%BA%E6%89%93%E8%84%B8%E6%9D%A5%E5%BE%97%E5%A4%AA%E5%BF%AB&t=31&band_rank=17&Refer=top)
1. [孙颖莎比赛身体不适](https://s.weibo.com//weibo?q=%23%E5%AD%99%E9%A2%96%E8%8E%8E%E6%AF%94%E8%B5%9B%E8%BA%AB%E4%BD%93%E4%B8%8D%E9%80%82%23&t=31&band_rank=18&Refer=top)
1. [刘学义躲镜头](https://s.weibo.com//weibo?q=%23%E5%88%98%E5%AD%A6%E4%B9%89%E8%BA%B2%E9%95%9C%E5%A4%B4%23&t=31&band_rank=19&Refer=top)
1. [人民日报评随意恶意举报](https://s.weibo.com//weibo?q=%23%E4%BA%BA%E6%B0%91%E6%97%A5%E6%8A%A5%E8%AF%84%E9%9A%8F%E6%84%8F%E6%81%B6%E6%84%8F%E4%B8%BE%E6%8A%A5%23&t=31&band_rank=20&Refer=top)
1. [国考](https://s.weibo.com//weibo?q=%E5%9B%BD%E8%80%83&t=31&band_rank=21&Refer=top)
1. [学历进单位第二周就没意义](https://s.weibo.com//weibo?q=%E5%AD%A6%E5%8E%86%E8%BF%9B%E5%8D%95%E4%BD%8D%E7%AC%AC%E4%BA%8C%E5%91%A8%E5%B0%B1%E6%B2%A1%E6%84%8F%E4%B9%89&t=31&band_rank=22&Refer=top)
1. [刘诗诗嘟嘴逗笑关晓彤](https://s.weibo.com//weibo?q=%23%E5%88%98%E8%AF%97%E8%AF%97%E5%98%9F%E5%98%B4%E9%80%97%E7%AC%91%E5%85%B3%E6%99%93%E5%BD%A4%23&t=31&band_rank=23&Refer=top)
1. [建议大家都8点半睡觉](https://s.weibo.com//weibo?q=%E5%BB%BA%E8%AE%AE%E5%A4%A7%E5%AE%B6%E9%83%BD8%E7%82%B9%E5%8D%8A%E7%9D%A1%E8%A7%89&t=31&band_rank=24&Refer=top)
1. [4AM任 咚咚](https://s.weibo.com//weibo?q=4AM%E4%BB%BB%20%E5%92%9A%E5%92%9A&t=31&band_rank=25&Refer=top)
1. [发现大家都有省钱意识了](https://s.weibo.com//weibo?q=%E5%8F%91%E7%8E%B0%E5%A4%A7%E5%AE%B6%E9%83%BD%E6%9C%89%E7%9C%81%E9%92%B1%E6%84%8F%E8%AF%86%E4%BA%86&t=31&band_rank=26&Refer=top)
1. [宋威龙搞砸了](https://s.weibo.com//weibo?q=%23%E5%AE%8B%E5%A8%81%E9%BE%99%E6%90%9E%E7%A0%B8%E4%BA%86%23&t=31&band_rank=27&Refer=top)
1. [蒋劲夫吃了两斤米饭才七分饱](https://s.weibo.com//weibo?q=%23%E8%92%8B%E5%8A%B2%E5%A4%AB%E5%90%83%E4%BA%86%E4%B8%A4%E6%96%A4%E7%B1%B3%E9%A5%AD%E6%89%8D%E4%B8%83%E5%88%86%E9%A5%B1%23&t=31&band_rank=28&Refer=top)
1. [张若昀回应内娱刘关张](https://s.weibo.com//weibo?q=%23%E5%BC%A0%E8%8B%A5%E6%98%80%E5%9B%9E%E5%BA%94%E5%86%85%E5%A8%B1%E5%88%98%E5%85%B3%E5%BC%A0%23&t=31&band_rank=29&Refer=top)
1. [永夜星河开播两周年视频](https://s.weibo.com//weibo?q=%23%E6%B0%B8%E5%A4%9C%E6%98%9F%E6%B2%B3%E5%BC%80%E6%92%AD%E4%B8%A4%E5%91%A8%E5%B9%B4%E8%A7%86%E9%A2%91%23&t=31&band_rank=30&Refer=top)
1. [白小纯直播人数](https://s.weibo.com//weibo?q=%23%E7%99%BD%E5%B0%8F%E7%BA%AF%E7%9B%B4%E6%92%AD%E4%BA%BA%E6%95%B0%23&t=31&band_rank=31&Refer=top)
1. [田曦薇 腰臀比](https://s.weibo.com//weibo?q=%E7%94%B0%E6%9B%A6%E8%96%87%20%E8%85%B0%E8%87%80%E6%AF%94&t=31&band_rank=32&Refer=top)
1. [董珊珊案凶手仅坐牢三年半](https://s.weibo.com//weibo?q=%E8%91%A3%E7%8F%8A%E7%8F%8A%E6%A1%88%E5%87%B6%E6%89%8B%E4%BB%85%E5%9D%90%E7%89%A2%E4%B8%89%E5%B9%B4%E5%8D%8A&t=31&band_rank=33&Refer=top)
1. [PEL拿到大芒果了](https://s.weibo.com//weibo?q=%23PEL%E6%8B%BF%E5%88%B0%E5%A4%A7%E8%8A%92%E6%9E%9C%E4%BA%86%23&t=31&band_rank=34&Refer=top)
1. [W盛典阵容](https://s.weibo.com//weibo?q=W%E7%9B%9B%E5%85%B8%E9%98%B5%E5%AE%B9&t=31&band_rank=35&Refer=top)
1. [程靖淇谈孙颖莎4比3早田希娜](https://s.weibo.com//weibo?q=%23%E7%A8%8B%E9%9D%96%E6%B7%87%E8%B0%88%E5%AD%99%E9%A2%96%E8%8E%8E4%E6%AF%943%E6%97%A9%E7%94%B0%E5%B8%8C%E5%A8%9C%23&t=31&band_rank=36&Refer=top)
1. [白小纯青稚直播人数](https://s.weibo.com//weibo?q=%23%E7%99%BD%E5%B0%8F%E7%BA%AF%E9%9D%92%E7%A8%9A%E7%9B%B4%E6%92%AD%E4%BA%BA%E6%95%B0%23&t=31&band_rank=37&Refer=top)
1. [马天宇见面会](https://s.weibo.com//weibo?q=%E9%A9%AC%E5%A4%A9%E5%AE%87%E8%A7%81%E9%9D%A2%E4%BC%9A&t=31&band_rank=38&Refer=top)
1. [DeepSeek发布全新Agent架构](https://s.weibo.com//weibo?q=%23DeepSeek%E5%8F%91%E5%B8%83%E5%85%A8%E6%96%B0Agent%E6%9E%B6%E6%9E%84%23&t=31&band_rank=39&Refer=top)
1. [谁比这个小姐姐更抗压](https://s.weibo.com//weibo?q=%E8%B0%81%E6%AF%94%E8%BF%99%E4%B8%AA%E5%B0%8F%E5%A7%90%E5%A7%90%E6%9B%B4%E6%8A%97%E5%8E%8B&t=31&band_rank=40&Refer=top)
1. [早田希娜看笔记打孙颖莎](https://s.weibo.com//weibo?q=%23%E6%97%A9%E7%94%B0%E5%B8%8C%E5%A8%9C%E7%9C%8B%E7%AC%94%E8%AE%B0%E6%89%93%E5%AD%99%E9%A2%96%E8%8E%8E%23&t=31&band_rank=41&Refer=top)
1. [微博视界大会获奖名单](https://s.weibo.com//weibo?q=%E5%BE%AE%E5%8D%9A%E8%A7%86%E7%95%8C%E5%A4%A7%E4%BC%9A%E8%8E%B7%E5%A5%96%E5%90%8D%E5%8D%95&t=31&band_rank=42&Refer=top)
1. [切尔西2比0曼联](https://s.weibo.com//weibo?q=%23%E5%88%87%E5%B0%94%E8%A5%BF2%E6%AF%940%E6%9B%BC%E8%81%94%23&t=31&band_rank=43&Refer=top)
1. [谭松韵王凯拥抱](https://s.weibo.com//weibo?q=%23%E8%B0%AD%E6%9D%BE%E9%9F%B5%E7%8E%8B%E5%87%AF%E6%8B%A5%E6%8A%B1%23&t=31&band_rank=44&Refer=top)
1. [郭焱谈孙颖莎4比3早田希娜](https://s.weibo.com//weibo?q=%23%E9%83%AD%E7%84%B1%E8%B0%88%E5%AD%99%E9%A2%96%E8%8E%8E4%E6%AF%943%E6%97%A9%E7%94%B0%E5%B8%8C%E5%A8%9C%23&t=31&band_rank=45&Refer=top)
1. [鹿晗太帅了鹿大人](https://s.weibo.com//weibo?q=%23%E9%B9%BF%E6%99%97%E5%A4%AA%E5%B8%85%E4%BA%86%E9%B9%BF%E5%A4%A7%E4%BA%BA%23&t=31&band_rank=46&Refer=top)
1. [金价暴跌是买大金镯还是等7字头](https://s.weibo.com//weibo?q=%23%E9%87%91%E4%BB%B7%E6%9A%B4%E8%B7%8C%E6%98%AF%E4%B9%B0%E5%A4%A7%E9%87%91%E9%95%AF%E8%BF%98%E6%98%AF%E7%AD%897%E5%AD%97%E5%A4%B4%23&t=31&band_rank=47&Refer=top)
1. [文青只会爱上文盲](https://s.weibo.com//weibo?q=%E6%96%87%E9%9D%92%E5%8F%AA%E4%BC%9A%E7%88%B1%E4%B8%8A%E6%96%87%E7%9B%B2&t=31&band_rank=48&Refer=top)
1. [梁靖崑vs张禹珍](https://s.weibo.com//weibo?q=%E6%A2%81%E9%9D%96%E5%B4%91vs%E5%BC%A0%E7%A6%B9%E7%8F%8D&t=31&band_rank=49&Refer=top)
1. [兰香如故](https://s.weibo.com//weibo?q=%E5%85%B0%E9%A6%99%E5%A6%82%E6%95%85&t=31&band_rank=50&Refer=top)

<!-- END WEIBO -->

历史归档 [./archives/weibo-search](./archives/weibo-search)

## License

[trending-in-one/](https://github.com/cxyfreedom/trending-in-one) 的源码使用 MIT License 发布。具体内容请查看
[LICENSE](./LICENSE) 文件。

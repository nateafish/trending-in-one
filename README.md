# trending-in-one

> 本仓库基于上游项目 [huqi-pr/trending-in-one](https://github.com/huqi-pr/trending-in-one)
> 及其持续更新分支整理，补全了历史归档数据；内容由 GitHub Actions 自动抓取、归档并维护。

[![ci](https://github.com/nateafish/trending-in-one/actions/workflows/ci.yml/badge.svg)](https://github.com/nateafish/trending-in-one/actions/workflows/ci.yml)
[![license](https://img.shields.io/github/license/izukuuuu/trending-in-one)](https://github.com/nateafish/trending-in-one/blob/main/LICENSE)

今日头条热搜、知乎热搜榜、知乎热门话题、微博热搜榜；记录从 2020-11-29
日开始的热搜。每小时抓取一次数据，按天[归档](./archives)。知乎视频热榜已下线（2025-05
起停更），不再抓取，仅保留历史数据。

<!-- BEGIN ZHIHUCOOKIE -->

**知乎热榜 Cookie**：✅ 有效 ｜ 最近刷新：2026-08-07 13:14 ｜ 最近检测：2026-11-15 01:10:21

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
<!-- 最后更新时间 Sun Nov 15 2026 01:17:31 GMT+0800 (China Standard Time) -->

1. [中国乘客亲历全美停飞以为被空袭](https://so.toutiao.com/search?keyword=中国乘客亲历全美停飞以为被空袭)
1. [结束3连败！国足2-0马来西亚](https://so.toutiao.com/search?keyword=结束3连败！国足2-0马来西亚)
1. [APEC如何走进你我生活](https://so.toutiao.com/search?keyword=APEC如何走进你我生活)
1. [孙悦婚礼孙卓落泪拥抱姐姐](https://so.toutiao.com/search?keyword=孙悦婚礼孙卓落泪拥抱姐姐)
1. [特朗普：空管系统故障无关网络攻击](https://so.toutiao.com/search?keyword=特朗普：空管系统故障无关网络攻击)
1. [糖尿病早期无症状 出现5种表现要重视](https://so.toutiao.com/search?keyword=糖尿病早期无症状%20出现5种表现要重视)
1. [《谷雨》导演查了所有演员税务才开机](https://so.toutiao.com/search?keyword=《谷雨》导演查了所有演员税务才开机)
1. [原价129万/支的天价药进医保了](https://so.toutiao.com/search?keyword=原价129万/支的天价药进医保了)
1. [吴清：A股市情在全球独一无二](https://so.toutiao.com/search?keyword=吴清：A股市情在全球独一无二)
1. [国足对马来西亚46年保持不败](https://so.toutiao.com/search?keyword=国足对马来西亚46年保持不败)
1. [乌鲁木齐禁售马肉马肠制品？假的](https://so.toutiao.com/search?keyword=乌鲁木齐禁售马肉马肠制品？假的)
1. [曝娜然怀孕了](https://so.toutiao.com/search?keyword=曝娜然怀孕了)
1. [博主：没了张玉宁国足就像另外一支队](https://so.toutiao.com/search?keyword=博主：没了张玉宁国足就像另外一支队)
1. [男子上门推拿加钟时性侵技师获刑](https://so.toutiao.com/search?keyword=男子上门推拿加钟时性侵技师获刑)
1. [正部级彭金辉有新职](https://so.toutiao.com/search?keyword=正部级彭金辉有新职)
1. [安切洛蒂：主裁水平不够影响比赛结果](https://so.toutiao.com/search?keyword=安切洛蒂：主裁水平不够影响比赛结果)
1. [猪肉价格创10年新低](https://so.toutiao.com/search?keyword=猪肉价格创10年新低)
1. [男子尝汤面后连面带碗扔垃圾桶](https://so.toutiao.com/search?keyword=男子尝汤面后连面带碗扔垃圾桶)
1. [全球最大无人货运飞机W5000试飞成功](https://so.toutiao.com/search?keyword=全球最大无人货运飞机W5000试飞成功)
1. [徐子尧演绎经典山歌打支山歌过横排](https://so.toutiao.com/search?keyword=徐子尧演绎经典山歌打支山歌过横排)
1. [王冰汝：基础设施老化拖垮美航空系统](https://so.toutiao.com/search?keyword=王冰汝：基础设施老化拖垮美航空系统)
1. [奔驰女司机借300元加油钱后关机](https://so.toutiao.com/search?keyword=奔驰女司机借300元加油钱后关机)
1. [“肉比菜贱”到底是怎么回事](https://so.toutiao.com/search?keyword=“肉比菜贱”到底是怎么回事)
1. [新婚夫妻还没出蜜月双双确诊糖尿病](https://so.toutiao.com/search?keyword=新婚夫妻还没出蜜月双双确诊糖尿病)
1. [国内首款痛风靶向生物制剂纳入医保](https://so.toutiao.com/search?keyword=国内首款痛风靶向生物制剂纳入医保)
1. [中信建投：2027年金价有望震荡上行](https://so.toutiao.com/search?keyword=中信建投：2027年金价有望震荡上行)
1. [国谈亲历者：好药进医保不只是靠降价](https://so.toutiao.com/search?keyword=国谈亲历者：好药进医保不只是靠降价)
1. [16岁高中生确诊糖尿病酮症酸中毒](https://so.toutiao.com/search?keyword=16岁高中生确诊糖尿病酮症酸中毒)
1. [小伙5年开出1300家无人健身房](https://so.toutiao.com/search?keyword=小伙5年开出1300家无人健身房)
1. [日本3-2巴西全场数据](https://so.toutiao.com/search?keyword=日本3-2巴西全场数据)
1. [中美竞争人工智能欧洲为何焦虑](https://so.toutiao.com/search?keyword=中美竞争人工智能欧洲为何焦虑)
1. [产妇羊水栓塞母子双亡 法院判了](https://so.toutiao.com/search?keyword=产妇羊水栓塞母子双亡%20法院判了)
1. [媒体：日本队复仇巴西斗劲十足](https://so.toutiao.com/search?keyword=媒体：日本队复仇巴西斗劲十足)
1. [血糖超标别以为是“累”](https://so.toutiao.com/search?keyword=血糖超标别以为是“累”)
1. [李昊两连扑力保城门不失](https://so.toutiao.com/search?keyword=李昊两连扑力保城门不失)
1. [多国外长谴责以军空袭加沙医疗设施](https://so.toutiao.com/search?keyword=多国外长谴责以军空袭加沙医疗设施)
1. [全美停飞背后：空管系统服役50年](https://so.toutiao.com/search?keyword=全美停飞背后：空管系统服役50年)
1. [天价羽绒服滤镜被超市平替撕碎](https://so.toutiao.com/search?keyword=天价羽绒服滤镜被超市平替撕碎)
1. [谢霆锋杭州演唱会“坐在星球上飞”](https://so.toutiao.com/search?keyword=谢霆锋杭州演唱会“坐在星球上飞”)
1. [当心胰岛素抵抗埋下糖尿病隐患](https://so.toutiao.com/search?keyword=当心胰岛素抵抗埋下糖尿病隐患)
1. [贵州雷山“高山流水”好惊艳](https://so.toutiao.com/search?keyword=贵州雷山“高山流水”好惊艳)
1. [美国为何发生航班大规模停飞事件](https://so.toutiao.com/search?keyword=美国为何发生航班大规模停飞事件)
1. [王钰栋打破国足全队307分钟进球荒](https://so.toutiao.com/search?keyword=王钰栋打破国足全队307分钟进球荒)
1. [乌总统：美建议乌割领土加入北约](https://so.toutiao.com/search?keyword=乌总统：美建议乌割领土加入北约)
1. [周小川谈资本市场制度建设](https://so.toutiao.com/search?keyword=周小川谈资本市场制度建设)
1. [美联储为何担忧AI热潮](https://so.toutiao.com/search?keyword=美联储为何担忧AI热潮)
1. [乌对俄发动近5年来最大规模空袭](https://so.toutiao.com/search?keyword=乌对俄发动近5年来最大规模空袭)
1. [厉娜给许飞代笔写的留言找到了](https://so.toutiao.com/search?keyword=厉娜给许飞代笔写的留言找到了)
1. [苏起：台海若发生战争只有死路一条](https://so.toutiao.com/search?keyword=苏起：台海若发生战争只有死路一条)
1. [茅台放开全系产品销售意味着什么](https://so.toutiao.com/search?keyword=茅台放开全系产品销售意味着什么)

<!-- END TOUTIAO -->

历史归档 [./archives/toutiao-search](./archives/toutiao-search)

## 知乎热搜榜

<!-- BEGIN ZHIHUSEARCH -->
<!-- 最后更新时间 Sun Nov 15 2026 01:57:44 GMT+0800 (China Standard Time) -->

1. [RTX5080暴跌4000元](https://www.zhihu.com/search?q=RTX5080%E6%9A%B4%E8%B7%8C4000%E5%85%83)
1. [美国所有航班暂停起飞](https://www.zhihu.com/search?q=%E7%BE%8E%E5%9B%BD%E6%89%80%E6%9C%89%E8%88%AA%E7%8F%AD%E6%9A%82%E5%81%9C%E8%B5%B7%E9%A3%9E)
1. [业内称山姆399元羽绒服是钩子商品](https://www.zhihu.com/search?q=%E4%B8%9A%E5%86%85%E7%A7%B0%E5%B1%B1%E5%A7%86399%E5%85%83%E7%BE%BD%E7%BB%92%E6%9C%8D%E6%98%AF%E9%92%A9%E5%AD%90%E5%95%86%E5%93%81)
1. [黄仁勋再被曝出轨前高管](https://www.zhihu.com/search?q=%E9%BB%84%E4%BB%81%E5%8B%8B%E5%86%8D%E8%A2%AB%E6%9B%9D%E5%87%BA%E8%BD%A8%E5%89%8D%E9%AB%98%E7%AE%A1)
1. [黄仁勋为什么突然辞职](https://www.zhihu.com/search?q=%E9%BB%84%E4%BB%81%E5%8B%8B%E4%B8%BA%E4%BB%80%E4%B9%88%E7%AA%81%E7%84%B6%E8%BE%9E%E8%81%8C)
1. [江苏多地整改高中生超长待机](https://www.zhihu.com/search?q=%E6%B1%9F%E8%8B%8F%E5%A4%9A%E5%9C%B0%E6%95%B4%E6%94%B9%E9%AB%98%E4%B8%AD%E7%94%9F%E8%B6%85%E9%95%BF%E5%BE%85%E6%9C%BA)
1. [曝英伟达临时CEO是制衡黄仁勋重要力量](https://www.zhihu.com/search?q=%E6%9B%9D%E8%8B%B1%E4%BC%9F%E8%BE%BE%E4%B8%B4%E6%97%B6CEO%E6%98%AF%E5%88%B6%E8%A1%A1%E9%BB%84%E4%BB%81%E5%8B%8B%E9%87%8D%E8%A6%81%E5%8A%9B%E9%87%8F)
1. [交大医学院基因编辑事件官方通报](https://www.zhihu.com/search?q=%E4%BA%A4%E5%A4%A7%E5%8C%BB%E5%AD%A6%E9%99%A2%E5%9F%BA%E5%9B%A0%E7%BC%96%E8%BE%91%E4%BA%8B%E4%BB%B6%E5%AE%98%E6%96%B9%E9%80%9A%E6%8A%A5)
1. [黄仁勋在英伟达的最后数小时](https://www.zhihu.com/search?q=%E9%BB%84%E4%BB%81%E5%8B%8B%E5%9C%A8%E8%8B%B1%E4%BC%9F%E8%BE%BE%E7%9A%84%E6%9C%80%E5%90%8E%E6%95%B0%E5%B0%8F%E6%97%B6)
1. [DeepSeek发布全家桶应用API](https://www.zhihu.com/search?q=DeepSeek%E5%8F%91%E5%B8%83%E5%85%A8%E5%AE%B6%E6%A1%B6%E5%BA%94%E7%94%A8API)
1. [英伟达超97%员工希望黄仁勋回归](https://www.zhihu.com/search?q=%E8%8B%B1%E4%BC%9F%E8%BE%BE%E8%B6%8597%25%E5%91%98%E5%B7%A5%E5%B8%8C%E6%9C%9B%E9%BB%84%E4%BB%81%E5%8B%8B%E5%9B%9E%E5%BD%92)
1. [库克被提名为黄仁勋潜在继任者](https://www.zhihu.com/search?q=%E5%BA%93%E5%85%8B%E8%A2%AB%E6%8F%90%E5%90%8D%E4%B8%BA%E9%BB%84%E4%BB%81%E5%8B%8B%E6%BD%9C%E5%9C%A8%E7%BB%A7%E4%BB%BB%E8%80%85)

<!-- END ZHIHUSEARCH -->

历史归档 [./archives/zhihu-search](./archives/zhihu-search)

## 知乎热门话题

<!-- BEGIN ZHIHUQUESTIONS -->
<!-- 最后更新时间 Sun Nov 15 2026 01:10:21 GMT+0800 (China Standard Time) -->

1. [多地网约车司机称被特惠车、一口价订单逼「疯」，不开特惠单就变少，怎样才能让乘客打车实惠、司机有单可接？](https://www.zhihu.com/question/2104661988609614000)
1. [Faker 采访称「我们不可能一直是冠军，更看好决赛 GEN 能赢」，为什么今年 GEN 评价如此高？](https://www.zhihu.com/question/2104572702581159200)
1. [《持械入宋》制片人称算力投入超百万且没投流，团队每部短剧都盈利，怎样看待这一高收益性？哪些思路能借鉴？](https://www.zhihu.com/question/2104167693242691800)
1. [马化腾曾坦言腾讯AI「上了船才发现船漏水」，如今又把员工分成陆军和海军，这释放了什么信号？](https://www.zhihu.com/question/2104265147606889500)
1. [工商银行、农业银行、中国人保称合计约2750亿元股票定增已经获上交所核准，对此你怎么看？](https://www.zhihu.com/question/2104203733609493500)
1. [美国因出现特殊情况及安全原因，所有航班一度暂停起飞，目前停飞令已解除，具体情况如何？造成影响有多大？](https://www.zhihu.com/question/2104838863910691000)
1. [圆周率中可能存在100万个连续的0吗？](https://www.zhihu.com/question/2049344893462565600)
1. [闻着香吃着却不甜的街边烤红薯，真的是用香精浸泡过的吗？这是什么原理？可以如何辨别？](https://www.zhihu.com/question/2100400144176920000)
1. [如何评价《fx战士久留美》第七集？](https://www.zhihu.com/question/2104328228877885700)
1. [为什么要偶尔带孩子去外面吃饭？](https://www.zhihu.com/question/1971822160084439800)
1. [专家称今冬我国大部大概率是暖冬但寒潮偏多，该如何从气象学角度上理解这一结论？](https://www.zhihu.com/question/2094963741066523000)
1. [CFA 中国之队肇庆国际足球邀请赛，国足 2-0 马来西亚，终结 3 连败进球荒，如何评价这场比赛？](https://www.zhihu.com/question/2105016126656570600)
1. [《给阿嬷的情书》获金鸡奖最佳编剧时无人响应，《密档》获金鸡奖最佳导演时掌声一片，你怎么看？](https://www.zhihu.com/question/2104243850030204700)
1. [《影之刃零》沐小葵建模获海外好评，如何看待东西方游戏女性角色审美的差异？](https://www.zhihu.com/question/2101953371276064300)
1. [遗传角度来看，孙子是和爷爷奶奶血缘更近，还是和外公外婆？](https://www.zhihu.com/question/307479952)
1. [DeepSeek harness相比codex有什么劣势？](https://www.zhihu.com/question/2072669811511923000)
1. [孩子不喝粥，家长要不要干涉？](https://www.zhihu.com/question/2102333880317563400)
1. [每天上班这么辛苦，晚上回家你会选择是自己带娃还是叫老人帮忙带？](https://www.zhihu.com/question/2072660922632556800)
1. [时常感觉和周围的人相处很累，是不合群吗？](https://www.zhihu.com/question/23788333)
1. [INTJ 最缺乏一种什么能力？](https://www.zhihu.com/question/1987563761586938000)
1. [赵本山主演喜剧《走马上任》口碑如何？有哪些亮点与不足？](https://www.zhihu.com/question/2100641649147778300)
1. [家里有果树是一种什么样的体验？](https://www.zhihu.com/question/311114953)
1. [南京「零元面馆」爆火后被质疑影响周边商家，创始人称如周围有餐饮商家因此受损愿出钱补偿，如何看待此回应？](https://www.zhihu.com/question/2104599557053081000)
1. [2026 年 10 月央行公布金融数据，前 10 月住户贷款大降 1.46 万亿说明了什么？](https://www.zhihu.com/question/2104665840050356500)
1. [医学生看医疗剧是一种什么样的体验？](https://www.zhihu.com/question/286205200)
1. [现在的电视剧为何难以让人产生追剧冲动？](https://www.zhihu.com/question/2065000842206384600)
1. [现在全民进入纯过日子时代，请问有什么省钱小方法？](https://www.zhihu.com/question/2099909869750974000)
1. [怎么看 Anthropic IPO 提到 Claude适配全芯片训练和推理，接入 AMD只用 3 天？](https://www.zhihu.com/question/2103879116948771800)
1. [如何评价《虹猫蓝兔》动画系列中的蓝兔？](https://www.zhihu.com/question/343026485)
1. [员工使用化名上班，离职索赔被拒并称用假名字是欺诈，法院判决不构成欺诈，依据是什么？化名具有法律效应吗？](https://www.zhihu.com/question/2103462019873650000)

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
<!-- 最后更新时间 Sun Nov 15 2026 03:15:28 GMT+0800 (China Standard Time) -->

1. [和合共生](https://s.weibo.com//weibo?q=%23%E5%92%8C%E5%90%88%E5%85%B1%E7%94%9F%23&Refer=new_time)
1. [GEN对战BLG](https://s.weibo.com//weibo?q=%23GEN%E5%AF%B9%E6%88%98BLG%23&t=31&band_rank=1&Refer=top)
1. [八冠神罚](https://s.weibo.com//weibo?q=%23%E5%85%AB%E5%86%A0%E7%A5%9E%E7%BD%9A%23&t=31&band_rank=2&Refer=top)
1. [数读向新向优向好的中国经济](https://s.weibo.com//weibo?q=%23%E6%95%B0%E8%AF%BB%E5%90%91%E6%96%B0%E5%90%91%E4%BC%98%E5%90%91%E5%A5%BD%E7%9A%84%E4%B8%AD%E5%9B%BD%E7%BB%8F%E6%B5%8E%23&t=31&band_rank=3&Refer=top)
1. [白小纯居然是来报恩的](https://s.weibo.com//weibo?q=%E7%99%BD%E5%B0%8F%E7%BA%AF%E5%B1%85%E7%84%B6%E6%98%AF%E6%9D%A5%E6%8A%A5%E6%81%A9%E7%9A%84&t=31&band_rank=4&Refer=top)
1. [许飞听到不负少年不负卿上热搜的反应](https://s.weibo.com//weibo?q=%E8%AE%B8%E9%A3%9E%E5%90%AC%E5%88%B0%E4%B8%8D%E8%B4%9F%E5%B0%91%E5%B9%B4%E4%B8%8D%E8%B4%9F%E5%8D%BF%E4%B8%8A%E7%83%AD%E6%90%9C%E7%9A%84%E5%8F%8D%E5%BA%94&t=31&band_rank=5&Refer=top)
1. [王乐乐](https://s.weibo.com//weibo?q=%E7%8E%8B%E4%B9%90%E4%B9%90&t=31&band_rank=6&Refer=top)
1. [曝高迪抖音直播权限被永封](https://s.weibo.com//weibo?q=%23%E6%9B%9D%E9%AB%98%E8%BF%AA%E6%8A%96%E9%9F%B3%E7%9B%B4%E6%92%AD%E6%9D%83%E9%99%90%E8%A2%AB%E6%B0%B8%E5%B0%81%23&t=31&band_rank=7&Refer=top)
1. [曝高迪当年打刘叉叉前女友蛋蛋](https://s.weibo.com//weibo?q=%23%E6%9B%9D%E9%AB%98%E8%BF%AA%E5%BD%93%E5%B9%B4%E6%89%93%E5%88%98%E5%8F%89%E5%8F%89%E5%89%8D%E5%A5%B3%E5%8F%8B%E8%9B%8B%E8%9B%8B%23&t=31&band_rank=8&Refer=top)
1. [国足张玉宁踢到对手 不是点球](https://s.weibo.com//weibo?q=%E5%9B%BD%E8%B6%B3%E5%BC%A0%E7%8E%89%E5%AE%81%E8%B8%A2%E5%88%B0%E5%AF%B9%E6%89%8B%20%E4%B8%8D%E6%98%AF%E7%82%B9%E7%90%83&t=31&band_rank=9&Refer=top)
1. [GEN对战BLG首发名单](https://s.weibo.com//weibo?q=%23GEN%E5%AF%B9%E6%88%98BLG%E9%A6%96%E5%8F%91%E5%90%8D%E5%8D%95%23&t=31&band_rank=10&Refer=top)
1. [boss直聘暂停要求带咖啡公司账号权限](https://s.weibo.com//weibo?q=%23boss%E7%9B%B4%E8%81%98%E6%9A%82%E5%81%9C%E8%A6%81%E6%B1%82%E5%B8%A6%E5%92%96%E5%95%A1%E5%85%AC%E5%8F%B8%E8%B4%A6%E5%8F%B7%E6%9D%83%E9%99%90%23&t=31&band_rank=11&Refer=top)
1. [高迪 王乐乐](https://s.weibo.com//weibo?q=%E9%AB%98%E8%BF%AA%20%E7%8E%8B%E4%B9%90%E4%B9%90&t=31&band_rank=12&Refer=top)
1. [英雄联盟](https://s.weibo.com//weibo?q=%E8%8B%B1%E9%9B%84%E8%81%94%E7%9B%9F&t=31&band_rank=13&Refer=top)
1. [孩子觉得打包丢人被老师扣分引热议](https://s.weibo.com//weibo?q=%23%E5%AD%A9%E5%AD%90%E8%A7%89%E5%BE%97%E6%89%93%E5%8C%85%E4%B8%A2%E4%BA%BA%E8%A2%AB%E8%80%81%E5%B8%88%E6%89%A3%E5%88%86%E5%BC%95%E7%83%AD%E8%AE%AE%23&t=31&band_rank=14&Refer=top)
1. [厉娜我和雪梨飞雪合一下影](https://s.weibo.com//weibo?q=%23%E5%8E%89%E5%A8%9C%E6%88%91%E5%92%8C%E9%9B%AA%E6%A2%A8%E9%A3%9E%E9%9B%AA%E5%90%88%E4%B8%80%E4%B8%8B%E5%BD%B1%23&t=31&band_rank=15&Refer=top)
1. [小寒梦游](https://s.weibo.com//weibo?q=%E5%B0%8F%E5%AF%92%E6%A2%A6%E6%B8%B8&t=31&band_rank=16&Refer=top)
1. [无畏](https://s.weibo.com//weibo?q=%E6%97%A0%E7%95%8F&t=31&band_rank=17&Refer=top)
1. [男子欠10元10年不还将债主打骨折](https://s.weibo.com//weibo?q=%23%E7%94%B7%E5%AD%90%E6%AC%A010%E5%85%8310%E5%B9%B4%E4%B8%8D%E8%BF%98%E5%B0%86%E5%80%BA%E4%B8%BB%E6%89%93%E9%AA%A8%E6%8A%98%23&t=31&band_rank=18&Refer=top)
1. [清融尽力](https://s.weibo.com//weibo?q=%23%E6%B8%85%E8%9E%8D%E5%B0%BD%E5%8A%9B%23&t=31&band_rank=19&Refer=top)
1. [大美妈妈回应](https://s.weibo.com//weibo?q=%23%E5%A4%A7%E7%BE%8E%E5%A6%88%E5%A6%88%E5%9B%9E%E5%BA%94%23&t=31&band_rank=20&Refer=top)
1. [JDG超话](https://s.weibo.com//weibo?q=JDG%E8%B6%85%E8%AF%9D&t=31&band_rank=21&Refer=top)
1. [曝爱奇艺尖叫之夜座位双C](https://s.weibo.com//weibo?q=%23%E6%9B%9D%E7%88%B1%E5%A5%87%E8%89%BA%E5%B0%96%E5%8F%AB%E4%B9%8B%E5%A4%9C%E5%BA%A7%E4%BD%8D%E5%8F%8CC%23&t=31&band_rank=22&Refer=top)
1. [原来热暴力真的比冷暴力有用](https://s.weibo.com//weibo?q=%E5%8E%9F%E6%9D%A5%E7%83%AD%E6%9A%B4%E5%8A%9B%E7%9C%9F%E7%9A%84%E6%AF%94%E5%86%B7%E6%9A%B4%E5%8A%9B%E6%9C%89%E7%94%A8&t=31&band_rank=23&Refer=top)
1. [暖阳夺冠发文](https://s.weibo.com//weibo?q=%23%E6%9A%96%E9%98%B3%E5%A4%BA%E5%86%A0%E5%8F%91%E6%96%87%23&t=31&band_rank=24&Refer=top)
1. [高迪这么多年完全对不起大美](https://s.weibo.com//weibo?q=%23%E9%AB%98%E8%BF%AA%E8%BF%99%E4%B9%88%E5%A4%9A%E5%B9%B4%E5%AE%8C%E5%85%A8%E5%AF%B9%E4%B8%8D%E8%B5%B7%E5%A4%A7%E7%BE%8E%23&t=31&band_rank=25&Refer=top)
1. [许飞直接红温了](https://s.weibo.com//weibo?q=%23%E8%AE%B8%E9%A3%9E%E7%9B%B4%E6%8E%A5%E7%BA%A2%E6%B8%A9%E4%BA%86%23&t=31&band_rank=26&Refer=top)
1. [胎儿基因缺失竟牵出爸爸肠道癌变](https://s.weibo.com//weibo?q=%23%E8%83%8E%E5%84%BF%E5%9F%BA%E5%9B%A0%E7%BC%BA%E5%A4%B1%E7%AB%9F%E7%89%B5%E5%87%BA%E7%88%B8%E7%88%B8%E8%82%A0%E9%81%93%E7%99%8C%E5%8F%98%23&t=31&band_rank=27&Refer=top)
1. [葡足协将封存C罗版7号球衣](https://s.weibo.com//weibo?q=%23%E8%91%A1%E8%B6%B3%E5%8D%8F%E5%B0%86%E5%B0%81%E5%AD%98C%E7%BD%97%E7%89%887%E5%8F%B7%E7%90%83%E8%A1%A3%23&t=31&band_rank=28&Refer=top)
1. [超9成胃癌患者早期有这两个症状](https://s.weibo.com//weibo?q=%23%E8%B6%859%E6%88%90%E8%83%83%E7%99%8C%E6%82%A3%E8%80%85%E6%97%A9%E6%9C%9F%E6%9C%89%E8%BF%99%E4%B8%A4%E4%B8%AA%E7%97%87%E7%8A%B6%23&t=31&band_rank=29&Refer=top)
1. [中纪委罕见通报高官一把手职权腐败](https://s.weibo.com//weibo?q=%23%E4%B8%AD%E7%BA%AA%E5%A7%94%E7%BD%95%E8%A7%81%E9%80%9A%E6%8A%A5%E9%AB%98%E5%AE%98%E4%B8%80%E6%8A%8A%E6%89%8B%E8%81%8C%E6%9D%83%E8%85%90%E8%B4%A5%23&t=31&band_rank=30&Refer=top)
1. [这要放十年前谁会觉得假](https://s.weibo.com//weibo?q=%E8%BF%99%E8%A6%81%E6%94%BE%E5%8D%81%E5%B9%B4%E5%89%8D%E8%B0%81%E4%BC%9A%E8%A7%89%E5%BE%97%E5%81%87&t=31&band_rank=31&Refer=top)
1. [吃完鸡爪肚子痛服务区还有二十公里](https://s.weibo.com//weibo?q=%E5%90%83%E5%AE%8C%E9%B8%A1%E7%88%AA%E8%82%9A%E5%AD%90%E7%97%9B%E6%9C%8D%E5%8A%A1%E5%8C%BA%E8%BF%98%E6%9C%89%E4%BA%8C%E5%8D%81%E5%85%AC%E9%87%8C&t=31&band_rank=32&Refer=top)
1. [纯璇](https://s.weibo.com//weibo?q=%E7%BA%AF%E7%92%87&t=31&band_rank=33&Refer=top)
1. [解说瓶子](https://s.weibo.com//weibo?q=%E8%A7%A3%E8%AF%B4%E7%93%B6%E5%AD%90&t=31&band_rank=34&Refer=top)
1. [奚梦瑶给女儿买迷你爱马仕](https://s.weibo.com//weibo?q=%E5%A5%9A%E6%A2%A6%E7%91%B6%E7%BB%99%E5%A5%B3%E5%84%BF%E4%B9%B0%E8%BF%B7%E4%BD%A0%E7%88%B1%E9%A9%AC%E4%BB%95&t=31&band_rank=35&Refer=top)
1. [白鹿带着三个作品走了三次红毯](https://s.weibo.com//weibo?q=%23%E7%99%BD%E9%B9%BF%E5%B8%A6%E7%9D%80%E4%B8%89%E4%B8%AA%E4%BD%9C%E5%93%81%E8%B5%B0%E4%BA%86%E4%B8%89%E6%AC%A1%E7%BA%A2%E6%AF%AF%23&t=31&band_rank=36&Refer=top)
1. [爱一个不爱自己的人是僭越](https://s.weibo.com//weibo?q=%E7%88%B1%E4%B8%80%E4%B8%AA%E4%B8%8D%E7%88%B1%E8%87%AA%E5%B7%B1%E7%9A%84%E4%BA%BA%E6%98%AF%E5%83%AD%E8%B6%8A&t=31&band_rank=37&Refer=top)
1. [青稚再获巅峰挑战赛冠军](https://s.weibo.com//weibo?q=%23%E9%9D%92%E7%A8%9A%E5%86%8D%E8%8E%B7%E5%B7%85%E5%B3%B0%E6%8C%91%E6%88%98%E8%B5%9B%E5%86%A0%E5%86%9B%23&t=31&band_rank=38&Refer=top)
1. [GEN对战BLG预测](https://s.weibo.com//weibo?q=%23GEN%E5%AF%B9%E6%88%98BLG%E9%A2%84%E6%B5%8B%23&t=31&band_rank=39&Refer=top)
1. [男子求婚瞬间火山喷发](https://s.weibo.com//weibo?q=%E7%94%B7%E5%AD%90%E6%B1%82%E5%A9%9A%E7%9E%AC%E9%97%B4%E7%81%AB%E5%B1%B1%E5%96%B7%E5%8F%91&t=31&band_rank=40&Refer=top)
1. [央视曝光假牛肉案](https://s.weibo.com//weibo?q=%23%E5%A4%AE%E8%A7%86%E6%9B%9D%E5%85%89%E5%81%87%E7%89%9B%E8%82%89%E6%A1%88%23&t=31&band_rank=41&Refer=top)
1. [网红模范夫妻高迪塌房](https://s.weibo.com//weibo?q=%23%E7%BD%91%E7%BA%A2%E6%A8%A1%E8%8C%83%E5%A4%AB%E5%A6%BB%E9%AB%98%E8%BF%AA%E5%A1%8C%E6%88%BF%23&t=31&band_rank=42&Refer=top)
1. [厉娜把青改成卿太神](https://s.weibo.com//weibo?q=%E5%8E%89%E5%A8%9C%E6%8A%8A%E9%9D%92%E6%94%B9%E6%88%90%E5%8D%BF%E5%A4%AA%E7%A5%9E&t=31&band_rank=43&Refer=top)
1. [高迪发化学抒情小作文](https://s.weibo.com//weibo?q=%23%E9%AB%98%E8%BF%AA%E5%8F%91%E5%8C%96%E5%AD%A6%E6%8A%92%E6%83%85%E5%B0%8F%E4%BD%9C%E6%96%87%23&t=31&band_rank=44&Refer=top)
1. [WB夺冠](https://s.weibo.com//weibo?q=WB%E5%A4%BA%E5%86%A0&t=31&band_rank=45&Refer=top)
1. [梓墨FMVP](https://s.weibo.com//weibo?q=%E6%A2%93%E5%A2%A8FMVP&t=31&band_rank=46&Refer=top)
1. [看到这种外卖店名感觉特别诡异](https://s.weibo.com//weibo?q=%E7%9C%8B%E5%88%B0%E8%BF%99%E7%A7%8D%E5%A4%96%E5%8D%96%E5%BA%97%E5%90%8D%E6%84%9F%E8%A7%89%E7%89%B9%E5%88%AB%E8%AF%A1%E5%BC%82&t=31&band_rank=47&Refer=top)
1. [买车后才发现有车和没车区别挺大的](https://s.weibo.com//weibo?q=%23%E4%B9%B0%E8%BD%A6%E5%90%8E%E6%89%8D%E5%8F%91%E7%8E%B0%E6%9C%89%E8%BD%A6%E5%92%8C%E6%B2%A1%E8%BD%A6%E5%8C%BA%E5%88%AB%E6%8C%BA%E5%A4%A7%E7%9A%84%23&t=31&band_rank=48&Refer=top)
1. [男子高速路上开智驾直接躺倒睡觉](https://s.weibo.com//weibo?q=%23%E7%94%B7%E5%AD%90%E9%AB%98%E9%80%9F%E8%B7%AF%E4%B8%8A%E5%BC%80%E6%99%BA%E9%A9%BE%E7%9B%B4%E6%8E%A5%E8%BA%BA%E5%80%92%E7%9D%A1%E8%A7%89%23&t=31&band_rank=49&Refer=top)
1. [太阳雨男主生日bug](https://s.weibo.com//weibo?q=%23%E5%A4%AA%E9%98%B3%E9%9B%A8%E7%94%B7%E4%B8%BB%E7%94%9F%E6%97%A5bug%23&t=31&band_rank=50&Refer=top)

<!-- END WEIBO -->

历史归档 [./archives/weibo-search](./archives/weibo-search)

## License

[trending-in-one/](https://github.com/cxyfreedom/trending-in-one) 的源码使用 MIT License 发布。具体内容请查看
[LICENSE](./LICENSE) 文件。

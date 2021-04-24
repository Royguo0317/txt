###  [:house:返回首頁](https://github.com/ourhimalayas/txt)
---

## 有中共背景的黑客利用VPN漏洞攻击美国国防工业
` 倫敦英喜莊園 Himalaya UK` [轉載自GNews](https://gnews.org/zh-hans/1134928/)

新闻来源：《Reuters》| 作者：Christopher Bing and Raphael Satter | 发布时间：2021年4月21日

翻译/简评：村民彼得潘 | 校对：感恩 | 审核：万人往 | Page：我是球大哥

[!\[\]()!\[\](https://spark.adobe.com/page/y2hVue2ZjdoiB/images/58b9f190-ea96-4fae-9468-e620b0f64fb4.jpg?asset_id=713ff22f-1372-4f85-bf87-5fe2496debe9&amp;img_etag=%22332ece279f639f53ee456354c6165b0f%22&amp;size=1024)](https://spark.adobe.com/page/y2hVue2ZjdoiB/images/58b9f190-ea96-4fae-9468-e620b0f64fb4.jpg?asset_id=713ff22f-1372-4f85-bf87-5fe2496debe9&amp;img_etag=%22332ece279f639f53ee456354c6165b0f%22&amp;size=1024)

正如文中所引述，多年来美国曾多次指控中共国黑客窃取美国军事机密，而文中提及的火眼子公司Mandiant，也是因其早在2013年发布的一份针对中共国网络间谍活动的报告而一举成名。不难察觉，虽然中共国自互联网诞生以来，一直孜孜不倦地通过这种虚拟方式偷取情报、信息和技术，但互联网的发源地美国也从未停止对这些行径的追踪和反击。即使这些网络安全公司在公众场合仍无法采取直接表述，似乎一个私营企业对一个国家政府的直接指控存在着巨大风险与立场上的不对等，但具体情况究竟如何，这些黑客行动背后是否有一双中共的手在推动，我想美方从民间到官方都心知肚明。

令人感到有些意外的是，跟踪中共多年的Mandiant副总裁也会惊叹中共目前黑客手段的先进。诚然，作为网络安全公司本身，他们的利益考量存在着情况越危急则越有生意可做的成份。但经过了多年来的偷抢骗、“蓝金黄”，中共可以在生物武器的开发研究上巧立名目，借助外国的技术支援，在网络技术方面又何尝不能“师夷长技以制夷”呢？卡马卡尔此言“先进”想必也是可控范围内的“先进”，如非他有把握应对这些黑客攻击，恐怕也轮不到这一家公司来做呼吁了。由此即可看出，中共自以为手段高明弄来了什么“葵花宝典”，然而其不思进取的本性让它在不断革新的美国面前，从来不会有赢的机会。

值得注意的是，据个人了解，本文提到存在漏洞的Pulse Connect Secure套件的应用范围极为广泛，尤其对于需要全球数据联动的大型跨国企业以及本文提到的国防等本身非常敏感、对数据十分依赖的企业。它的基本功能可以概括为，用户在需要远程办公时，该程序在个人或公共网络与公司服务器之间建立加密通道，以保障信息只在公司内部流通。这意味着只要骇客了这套登入系统，那么使用该系统的所有公司都会受到极大的数据泄露威胁。而新冠病毒大爆发期间，在家办公十分普遍，这无疑让黑客更容易混淆其中。事实上，文中提到的思杰、思科也是为公司提供类似全套解决方案的巨头。在所有的行业，尤其尖端技术领域，都或多或少与信息技术相绑定的今天，想避开这两个名字是非常难的。简而言之，中共这回是在试图找到一把万能钥匙。我们不知道美方是如何放任中共到今天，使其有了足够的眼界与野心以及一定的技术和能力，瞄准了这样一个危险目标。但卡马卡尔并没有言过其实，美方是时候采取行动了。

**原文翻译：**

## **研究人员：与中共国有关联的黑客利用VPN漏洞锚定攻击美国国防工业**

[!\[\]()!\[\](https://spark.adobe.com/page/y2hVue2ZjdoiB/images/ab6a25ed-65b1-4a7e-9e80-d0439424e7a2.jpg?asset_id=e2997b6d-fe54-4c5e-b11a-5ff521c73c8f&amp;img_etag=%22381191eb26a7ce5fd488cf788a40b79a%22&amp;size=1024)](https://spark.adobe.com/page/y2hVue2ZjdoiB/images/ab6a25ed-65b1-4a7e-9e80-d0439424e7a2.jpg?asset_id=e2997b6d-fe54-4c5e-b11a-5ff521c73c8f&amp;img_etag=%22381191eb26a7ce5fd488cf788a40b79a%22&amp;size=1024)2010年9月24日，美国国土安全部的徽章被拍摄于弗吉尼亚州阿灵顿郡华盛顿特区郊外的国家网络安全与通信集成中心（NCCIC）。路透社/Hyungwon Kang

[!\[\]()!\[\](https://spark.adobe.com/page/y2hVue2ZjdoiB/images/6a11be7d-5104-447a-a9e8-1a14fbc58286.jpg?asset_id=488143cd-635c-45db-a8cb-99ea39efb6b7&amp;img_etag=%226a806482d70115e55f3f9d329e8f8e70%22&amp;size=1024)](https://spark.adobe.com/page/y2hVue2ZjdoiB/images/6a11be7d-5104-447a-a9e8-1a14fbc58286.jpg?asset_id=488143cd-635c-45db-a8cb-99ea39efb6b7&amp;img_etag=%226a806482d70115e55f3f9d329e8f8e70%22&amp;size=1024)在这幅2021年4月20日制作的插图中可以看到Ivanti的标志及网络二进制代码。路透社/Dado Ruvic/插图设计

研究人员和设备制造商周二表示，至少有两组与中共国有关联的黑客花了几个月时间，利用美国虚拟私人网络设备中一个先前未被披露的漏洞，对美国国防工业进行监视。

总部位于犹他州的IT公司Ivanti在一份声明中[称](https://blog.pulsesecure.net/pulse-connect-secure-security-update/)，这些黑客利用其Pulse Connect Secure套件中的漏洞，侵入“数量非常有限的客户”的系统。

Ivanti[表示](https://kb.pulsesecure.net/pkb_mobile#article/l:en_US/SA44784/s)，虽然他们已经采取了缓解措施，但对该问题的修复要到5月初才能实现。

关于谁可能对间谍活动负责，Ivanti没有提供任何细节，但在与Ivanti的公告同时发布的一份报告中，网络安全公司火眼（FireEye Inc,[FEYE.O](https://www.reuters.com/companies/FEYE.O)）称，他们怀疑至少有一个黑客团队代表中共国政府运作。

“我们怀疑涉案的另一个黑客组织与中共国发动的举措和案件丛集相吻和。”火眼旗下的Mandiant公司高级副总裁查尔斯·卡马卡尔（Charles Carmakal）在报告发布前表示。

将黑客与特定国家联系起来充满了不确定性，但卡马卡尔称，他的分析师们的判断是基于对黑客的战术、工具、基础设施和目标的审查——其中许多与过去跟中共国有关的入侵行为相呼应。

中共国大使馆发言人刘鹏宇表示，中共国“坚决反对并打击一切形式的网络攻击”，并将火眼的指控形容为“不负责任且居心不良”。

火眼拒绝透露黑客的目标，只将这些目标标识为“世界各地的国防、政府和金融机构”。它表示，这群被怀疑代表北京当局工作的黑客特别关注于美国国防工业。

国土安全部的网络部门在一份声明中称，他们正在与Ivanti合作，“以更好地了解Pulse Secure VPN设备的漏洞，并减少对联邦民用和私营领域网络的潜在风险。”

美国国家安全局拒绝发表评论。多年来，美方官员曾多次指控中共国黑客通过各种手段窃取美国军事机密。

最近，公司难以监控的网络设备已成为受数字间谍青睐的进攻路径。

2020年，火眼就曾[警告](https://www.fireeye.com/blog/threat-research/2020/03/apt41-initiates-global-intrusion-campaign-using-multiple-exploits.html)，与北京当局结盟的黑客们正瞄准进攻思杰系统公司（Citrix Systems Inc, [CTXS.O](https://www.reuters.com/companies/CTXS.O)）和思科系统公司（Cisco Systems Inc, [CSCO.O](https://www.reuters.com/companies/CSCO.O)）制造的设备，以入侵许多的公司，火眼称这是他们多年来看到的中共国黑客最广泛的活动之一。

虽然火眼的报告表示对最近这一系列的黑客行为的调查发生在“今年年初”，但没有明确说明黑客攻击的具体时间。

卡马卡尔补充道，黑客在美国的数字基础设施上操作，并借用受害公司的命名惯例来伪装他们的活动，这样他们看起来就像任何其他从家里登录的员工。

“我们正目睹相当先进的技术手段。”他表示。

[原文链接](https://www.reuters.com/technology/china-linked-hackers-used-pulse-secure-flaw-target-us-defense-industry-2021-04-20/?taid=607f1edf5a08ec0001320f83&amp;utm_campaign=trueAnthem:+Trending+Content&amp;utm_medium=trueAnthem&amp;utm_source=twitter)

- [点击阅读英国伦敦喜庄园在G-News 的更多精彩文章](https://gnews.org/zh-hans/author/himalaya_hawk/)
- [点击观看英国伦敦喜庄园在G-TV的精彩视频](https://gtv.org/web/#/UserInfo/5ee680a45bd6f123dd104807)
- [欢迎加入【英国伦敦喜庄园】Discord官方群](https://discord.gg/U9F97ur)


编辑：【英国伦敦喜庄园编辑部】

[!\[\]()!\[\](https://spark.adobe.com/page/y2hVue2ZjdoiB/images/5f252922-8534-476b-a824-827f4f372f36.jpg?asset_id=2dc784fd-dc93-4f64-b153-e60b7273e2dd&amp;img_etag=%22a8bb00791f167c919a809dcf9f5fb58b%22&amp;size=1024)](https://spark.adobe.com/page/y2hVue2ZjdoiB/images/5f252922-8534-476b-a824-827f4f372f36.jpg?asset_id=2dc784fd-dc93-4f64-b153-e60b7273e2dd&amp;img_etag=%22a8bb00791f167c919a809dcf9f5fb58b%22&amp;size=1024)

0

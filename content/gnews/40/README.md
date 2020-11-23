###  [:house:返回首頁](https://github.com/ourhimalayas/txt)
---

## 浅谈GTV的独特性与价值 &#8212; 多人直播
` 康州喜马拉雅农场` [轉載自GNews](https://gnews.org/zh-hans/582626/)

作者：康州农场-光头波波

审核：康州农场-Truemanman

GTV作为G系列第一款重磅产品，承载了传播真相，宣传爆料革命的重要使命。郭先生以及很多战友，都已经从市场需求、未来前景、产品竞争力等很多方面解读了GTV的价值[1,2,3,4,5,6]。笔者今天想从技术层面聊聊GTV的独特性和价值。

GTV是一个集直播、社交、通信为一体的综合性平台。如图1是笔者根据现有GTV APP和郭先生过往直播中的描述，简单概括的GTV目前和未来将要上线的功能。从功能模块上看，GTV目前的直播功能已实现从手机端到视频工作站全覆盖，不仅能让战友们打开手机、电脑就能直播，而且还能满足专业用户，如新中国联邦电视台等，外接专业摄像机、控制器的摄影棚级别的直播需求。而其余的的功能，未来都能拆分成独立的应用服务。比如现有的盖特功能，已经达到推特10%的体验（见郭先生11月15日视频[7]），在技术层面，达到或超过推特只是时间问题。考虑到推特与中共的勾结，未来盖特取代推特、脸书将是必然。端到端加密通信，视频会议等功能，未来也会有巨大的市场空间。配合G系列生态，GTV未来必将拓展成一个完整的高科技服务平台。

今天笔者想与大家聊聊GTV的直播功能，尤其是支持最多六人同时连线直播的功能。郭先生多次在直播中提到支持多人连线直播是GTV独一无二的功能。可能战友们对此没有概念，今天笔者就从需求和技术实现两个层面，浅谈为什么这个功能很重要，但也很难做到。
![](https://gnews-media-offload.s3.amazonaws.com/wp-content/uploads/2020/11/22204106/%E5%9B%BE%E7%89%871-31.png)
**1.**** ****直播是700亿美元的市场**

在线直播近两年火遍国内外，各种新兴词汇不绝于耳，游戏主播、直播带货、小姐姐、老铁…… 主播日入百万，直播带货一夜几十亿的消息刷遍各自媒体。洗脑式的宣传和想要一夜暴富，让很多人都加入直播大军。在浮躁、劣币驱逐良币的中国社会，由直播闹出的笑话不绝于耳，比如“萝莉变大妈” 等[8]。 更令人可悲的是，很多小朋友的梦想竟是长大当主播、当网红。[9]

暂不谈中共治下的社会乱象，根据报告[10]，直播市场预计在2021年达到700亿美元。同时，在CCP病毒影响之下，未来的商业模式将更多转到线上。视频直播以及其衍生应用将不断扩展。GTV作为后期之秀，“钱”途无量。

**2.**** ****为什么目前直播平台不具备多人连线直播**

以下是笔者收集的国内、国外主流的直播平台。这些平台主要服务于两个主题：电商和游戏娱乐。这些场景是属于一对多模式。一位主播对许多观众。比如李佳奇向百万粉丝 “OMG 买它！”， 或者游戏主播，实时分享游戏画面和他的头像。因此直播平台提供的所有的功能都是围绕这样的场景开发，如分享屏幕，打赏，抢红包，主播连麦等。但多人同时连线直播并不是此场景下的刚需。诚然，通过调查，笔者找到部分平台支持两位主播连线，跨直播间连线，和与观众连麦功能。不过连接数只有两位，而且并不是个平台的主打功能。
![](https://gnews-media-offload.s3.amazonaws.com/wp-content/uploads/2020/11/22204555/2-195.png)
图2   国内外视频直播平台 [11, 12]
那么，哪些场景需要多人连线呢? 新闻媒体采访，商务会议等涉及多方互动的场景。

**3.**** ****六人同时连线直播，GTV独一家**

在爆料革命的背景下，**GTV承载着媒体平台的功能**，多人连线直播功能是刚需。它可以让新闻更好更快的传播出去。比如大游行时连线前方战友，64建国日连线全球各地战友等。

可能战友们会问，多人连线直播已经不是新技术，比如《路德访谈》节目，路德先生可以与安红女士，博士军团们共同做节目。为什么还说该功能GTV独一家呢？

**因为便捷性。**现在的多人连线都是通过专业软件和外接设备，将多股视频流合成为一，再通过主播的账户直播出去的。比如Lightstream [13] 或者图3中路德社的专业设备。能让用户打开手机，直接连线直播的，GTV独一家。
![](https://gnews-media-offload.s3.amazonaws.com/wp-content/uploads/2020/11/22204324/%E5%9B%BE%E7%89%872-20.png)
**4.**** ****那么，多人连线到底难在哪？**

简单说，难在让画面和声音流畅、同步。

笔者画一个简单的多人连线直播技术架构图(图4)。从上到下，是六位主播的视频画面，传到GTV后端服务器上，六个画面实时合成为一个画面，然后再通过CDN网络，传送到世界各地战友们的屏幕上。
![](https://gnews-media-offload.s3.amazonaws.com/wp-content/uploads/2020/11/22204420/%E5%9B%BE%E7%89%873-18.png)
结构看似简单，但咱们需要考虑两个问题：观众人数众多（七哥直播都是百万级的），视频画面数据量大（高清画面）。

具体来说，这需要解决几个关键问题[15]:

1. **低延迟**：多人连线需要良好的互动、交流，如果延迟太高，就会出现主持人问了问题，过几秒才听到嘉宾回答的声音。
2. **音画不同步**：比如大家看到七哥嘴在动，但声音1秒钟后才听见
3. **卡顿率**：就是大家看到的画面很卡
4. **画质**：影响大家看七哥秀新西装
5. **延展性**：就是直播间要能同时容纳亿万战友同时观看


**5.**** ****GTV是如何实现的？**

GTV具体用了什么软件技术，笔者不得而知。但从以上的分析来看，GTV拥有非常强大的计算资源和网络带宽资源。

笔者给大家估算一笔账，来简单衡量一下GTV的实力。文贵先生的日常直播在线观看量都达到百万级别，比如他8月31日直播唱歌，同时有330万观众（不包括VPN和游客）在线观看。那么假设每台设备一分钟接收50MB数据量，那么这场直播，GTV需要约165TB每分钟的CDN带宽吞吐量。这个是什么概念呢,？按照阿里云在中国大陆的收费标准[16]，七哥那天直播，每分钟需要支付网费4,950美元, 三个小时下来，光网费就花了89.1万美元！

当然，GTV的实力远远不止这些。

对于想深入了解GTV技术的战友们，我为大家推荐一个GTV频道 Apple [17]，上面有讲解GTV的技术细节。
![](https://gnews-media-offload.s3.amazonaws.com/wp-content/uploads/2020/11/22204523/%E5%9B%BE%E7%89%874-15.png)
**6.**** ****小故事，为什么说螃蟹太坏了！**

螃蟹在最初的GTV代码中安插了非常多的后门。根据笔者了解的消息，螃蟹开发的GTV，使用了中国公司声网（Agora）的直播服务。这意味着，GTV所有视频数据，都会先发送到中国大陆声网公司，再由他们的服务器，分发给各位战友看。而这个关键的直播模块，对GTV团队，完全是黑盒，不知道里面藏着什么。螃蟹就能够借机做手脚。同时，由于咱们的特殊性，将数据流传回中国大陆是非常危险的。GTV在最初上线之时，连接非常不稳定，而且直播在线人数异常。郭先生的直播现在人数，永远被控制在7万左右。

但永远不要低估战友们的实力，在约翰叔叔（Joe），GTV团队和优秀的工程师战友团队一同努力下，在64建国日前，紧急封堵漏洞，实现了2000万人同时在线观看！

战友们，GTV背后的实力，是咱们无法想象的，咱们只管跟着七哥走！

参考资料:

[1] [https://gnews.org/zh-hans/255826/](https://gnews.org/zh-hans/255826/) 江财神谈GTV股票价值

[2] [https://gnews.org/zh-hans/581626/](https://gnews.org/zh-hans/581626/) 郭先生11.21:G系列改变传统赢利模式不向任何人弯腰、磕头

[3] [https://gnews.org/zh-hans/518088/](https://gnews.org/zh-hans/518088/) GTV成为世界主流媒体

[4] [https://gnews.org/zh-hans/503817/](https://gnews.org/zh-hans/503817/) 结合GTV谈投资的风险与回报

[5] [https://gnews.org/zh-hans/463967/](https://gnews.org/zh-hans/463967/) 史蒂夫·班农（Steve Bannon）和GTV将成为拯救西方文明的明灯

[6] [https://gnews.org/zh-hans/461885/](https://gnews.org/zh-hans/461885/)  班农和GTV担负起了拯救西方文明的责任

[7] [https://gtv.org/video/id=5fb15d10b2a6d15327826e0a](https://gtv.org/video/id=5fb15d10b2a6d15327826e0a) 郭先生20201115视频

[8] [https://new.qq.com/omn/20190801/20190801A00PIY00.html](https://new.qq.com/omn/20190801/20190801A00PIY00.html)  直播平台封停“萝莉变大妈”主播 事件系主播自主策划炒作

[9] [https://new.qq.com/omn/20191214/20191214A09ZG500.html?pc](https://new.qq.com/omn/20191214/20191214A09ZG500.html?pc)  “儿童网红”泛滥，女儿梦想做主播，孩子的梦想正在被“畸形”

[10] [https://www.visualstorytell.com/blog/how-to-plan-your-live-video-storytelling-strategy](https://www.visualstorytell.com/blog/how-to-plan-your-live-video-storytelling-strategy) The live streaming market worldwide is projected to grow from $30.29 Billion in 2016 to $70.05 Billion by 2021

[11] [http://www.woshipm.com/it/3753544.html](http://www.woshipm.com/it/3753544.html) 国内视频直播平台

[12] [https://www.onecause.com/wp-content/uploads/2020/09/streaming-platforms.jpg](https://www.onecause.com/wp-content/uploads/2020/09/streaming-platforms.jpg) 国外视频直播平台

[13] [https://golightstream.com/greenroom/](https://golightstream.com/greenroom/) Lightstream

[14] [https://www.youtube.com/watch?v=xYMHBT0rYjM&ab\_channel=%E8%B7%AF%E5%BE%B7%E7%A4%BELUDEMedia](https://www.youtube.com/watch?v=xYMHBT0rYjM&amp;ab_channel=%E8%B7%AF%E5%BE%B7%E7%A4%BELUDEMedia)  路德直播间

[15] [https://zhuanlan.zhihu.com/p/27086190](https://zhuanlan.zhihu.com/p/27086190) 直播连麦技术方案对比及测试方法

[16] [https://www.alibabacloud.com/zh/product/cdn/pricing](https://www.alibabacloud.com/zh/product/cdn/pricing) 阿里巴巴CDN

[17] [https://gtv.org/user/5ec2c38a82e098349f024a95](https://gtv.org/user/5ec2c38a82e098349f024a95) GTV用户Apple

1+

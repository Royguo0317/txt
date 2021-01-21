###  [:house:返回首頁](https://github.com/ourhimalayas/txt)
---

## 如何增加推文曝光度：2021年推特算法总结
` Himalaya Australia` [轉載自GNews](https://gnews.org/zh-hans/785174/)

作者：土小木

审稿：Jenny  编辑：MG1
![]()![](https://gnews.org/wp-content/uploads/2021/01/屏幕截图-2021-01-21-124150-2-2.png)（图片：推特创始人最初设计手稿 来源：https://en.wikipedia.org/wiki/File:Twttr\_sketch-Dorsey-2006.jpg）
作为全球最大的社交媒体平台之一，推特被许多商家用来宣传自己的产品或理念，其中不乏有各类付费广告。人们打开推特，往往都会看到其关注的账户最近发出的推文，以及推特认为用户可能会感兴趣的推文。那么推特是根据什么来决定所有这些推文的显示顺序，以及推文的选择呢？本文研究了目前为止能找到的相关文章，对此做一个总结。

根据推特工程师Nicolas Koumchatzky和Anton Andryeyev发布的一篇博客文章(1)，推特早期的推文显示算法非常简单：用户每次打开推特，看到的推文是上次打开推特之后，其关注的所有人发出的推文，按照发推时间倒序显示。

举例来讲，假设用户关注了三个推特账户：张三、李四、王五，发推时间如下：

早上9点：打开推特

早上10点：张三发推“传播香港危机真相”

下午1点：李四发推“传播闫博士中共病毒报告”

下午3点：王五发推“今天吃了巧克力”

下午5点：打开推特

那么此刻看到的推文应该分别是：

“今天吃了巧克力” – 王五

“传播闫博士中共病毒报告” – 李四

“传播香港危机真相” – 张三

这个先后顺序很简单，但是显而易见，它有很多缺陷，比如用户平时关注的主要是爆料革命相关的推文，而王五发的“今天吃了巧克力”跟爆料革命无关，只因为是关注者当中最新发推的账户，所以这条推文被放在了第一位。

推特也认识到了这个问题，于是加入了一套复杂的打分系统，每条推文都有一个评分（ranking），这个评分就决定了推文的显示或不显示以及显示的顺序。具体来说，每条推文都会根据以下几点来打分：

- 时效性：这条推文从发出到现在过了多久，越新的推文得分越高
- 互动性：这条推文被转推的次数，被点了多少次，多少次点赞以及被多少人看过，这些数字越高，得分则越高
- 多媒体：推文里包含的多媒体内容，如图片、视频以及动画图片（GIF），有多媒体的推文会有额外的得分
- 活跃度：发推的用户上次来推特距今有多久，被多少人关注，关注者是否频繁使用推特。比如一个没有人关注的账号，和一个上百万粉丝的账号，即便是发完全一样的推文，评分也是会倾向于上百万粉丝的账号得分更高。


这套打分系统为每一条推评估分数，而这个分数则被用来决定推文是否会被更多的人看到。根据推特的打分算法，可以从如下几点入手来增加推文的曝光度：

- 有间隔并持续的发推：假如需要发十条推文，一天里分十个时间段分别发出，效果会比一个时间连续发十条要好
- 保持固定的登陆习惯：比如每天都登陆推特，而不是好几天才打开一次
- 增加推文互动：这包括鼓励转推，常见的说法例如“RT if you agree”（如果你同意，请转推）；使用相关的标签（hashtag）；艾特相关的账户以及在分数高的相关推文下回复自己的推
- 尽快回应别人与你推文的互动：比如别人的推文里提到了你，别人回复或转发了你的推文，可以回复一条推文表示感谢
- 多媒体：如果可以，推文里增加与推文相关的图片或视频
- 发推账号：尽可能让自己的关注者多起来


希望本文对爆料革命的真相传播起到一定的作用。

本文纯属个人观点

参考文章：

(1) Use Deep Learning at Scale in Twitter’s Timelines: [https://blog.twitter.com/engineering/en\_us/topics/insights/2017/using-deep-learning-at-scale-in-twitters-timelines.html](https://blog.twitter.com/engineering/en_us/topics/insights/2017/using-deep-learning-at-scale-in-twitters-timelines.html)

Never miss important Tweets from people you follow: [https://blog.twitter.com/official/en\_us/a/2016/never-miss-important-tweets-from-people-you-follow.html](https://blog.twitter.com/official/en_us/a/2016/never-miss-important-tweets-from-people-you-follow.html)

Everything you need to know about social media algorithms: [https://sproutsocial.com/insights/social-media-algorithms/](https://sproutsocial.com/insights/social-media-algorithms/)
![]()![](https://gnews.org/wp-content/uploads/2021/01/1-澳喜Logo-1.jpeg)
+1

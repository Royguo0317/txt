###  [:house:返回首頁](https://github.com/ourhimalayas/txt)
---

## “多猫腻” Dominion 计票系统本身设计的可疑之处 选举舞弊的犯罪远超想象力
` 喜马拉雅凤凰农场–旧金山-金喜站` [轉載自GNews](https://gnews.org/zh-hans/565517/)

**编译：平民游侠 H-Ranger****喜马拉雅凤凰农场**-旧金山站

民主党部分关键人员参与执行了2020美国总统选举造假和舞弊的行为相信已经不再是什么秘密了。从公众已经获知的消息来看这次总统选举的舞弊行为主要表现为以下几点：

- 丢弃或撕毁川普总统的选票。
- 盗窃死人、老人的身份，以他们的名义寄出支持拜登的非法选票。
- 盗用隐私被泄漏的合法选民的身份，在他们去现场投票之前寄出支持白登的邮寄选票。这导致部分合法选民现场投票时发现系统提示自己已经投过票了。
- 硬造出不存在的人进行邮寄投票。这些选票甚至连签名都没有或者有数千张都是同一个人的名字。
- 把迟到的不合格邮寄选票当作合格的选票计入。
- 借助一些伪装手段将假选票在夜晚运到投票点。有的装在行李箱里，有的装在保温箱里。
- 渗透或控制计票系统通过篡改数据或验票规则来影响结果。凭空增加拜登的选票，把川普总统的选票判定为不合格，把川普的选票错计为拜等的选票等等都可以通过操控计票系统和软件来实现。


**川普总统今早发推：Dominion 计票機在操纵着我们的大选！**

![](https://lh4.googleusercontent.com/XOubgWfTFu208FOXDXhwfN33akNBkVeIVVU7p5SbTD9wdSVtExpSlrBYJvwJNQUs78HLKUnXbRNiiaV4wvHM5xSqQX-d4Mw1oKZUotim20FBGumNAJ4GlW5k1bYQpg)

最近有热心网友在研究了部分州所使用的Dominion计票系统的相关文档后提出了一系列疑问和系统设计的可疑之处。我们将这些内容翻译成了中文。联系到昨天爆出的Dominion中央服务器在德国法兰克福被美军查获的新闻。相信该系统的猫腻很快会大白于天下。

![](https://lh3.googleusercontent.com/zhrBAH_Z63Fd9Li1ebvcxneYzFPeV0DFkvS4Jvz-L6jLxS3fWyC2bG6LClGC5KSK85TQTWkvqS0LKc-hhegQgpOzsyS7b7_U7nxk_2ZTvP5n02ilpmfUbTKlYYpgYg)

1. 理论上系统可以将特定的“一条龙”（Straight Ticket Vote)选票判定为无效。“一条龙”选票的处理规则基于很多复杂的选项设置进行工作。这个设定可以利用例如“ Repubiican”之类的拼写错误来作弊。

（Votes can theoretically be ignored for individuals if a straight ticket vote is selected. This setting could very well enable “Repubiican”-style typo fraud. Many complex rules decide how the “straight ticket” option works.）

2. 所有的软件访问键值都使用由同一组密钥，这使得该软件在网络安全上显得非常薄弱。这种薄弱的防护措施不能有效防止别有用心的人进入投票系统篡改设置。而且因为所有人使用同一组密钥访问系统，就算发现系统设置被人篡改了也难以证明是被谁篡改的。

（Network Security is very weak since all software access keys use the same cryptographic pair. This gives plausible deniability to whoever potentially decides to mess around with voting settings. It can’t be proven who changed a setting since everybody has the same key）

3. Dominion的数字证书没有使用密码保护，而且Dominio的用户手册明确说明不需要输入密码。这使得不法分子有机会使用中间人攻击的方式威胁到终端设备和中央服务器之间的通信。

（Digital certificates are not protected by password, and Dominion user manual explicitly says not to enter a password. This enables potential for bad actors to MITM attack data traveling over network between precinct tabulator and central tabulator.）

4. Dominion系统有一个隐藏的“拆分旋转”（split rotation）功能用来限制最大误差。但是，这个功能没有明确的定义和说明，所以我们无法确定这个功能到底在这里起什么作用。

（Cryptic “split rotation” function that features the ability to “force a maximum deviation”. There is no definition of a “split rotation”, so we cannot know what “force a maximum deviation” means in this instance.）

5. 投票点本地的IT人员有权限调试系统或更改系统设置。这种权利没有任何监督和制衡。我们也不清楚IT人员对系统修改后会不会留下日志。这种不受限制的修改系统设置的权利足以让这些人有能力将选举颠倒黑白。（Local IT guys have ultimate power to clandestinely change settings, thus having the ability to potentially alter an entire election. There are no checks and balances or observers of the local IT guy when he accesses machine debug and admin settings. It‘s unclear if logs exist.）

6. Dominio系统收集每个终端的投票数据然后传输到中央服务器。我们无法找到中央服务器及其包含的软件的使用说明和安全性验证报告。中央服务器对我们来讲是个无法看到内部工作原理的黑盒子。（Dominion is a black box with votes ultimately tabulated in a central server system. Who has access to the central server and where is the manual and security reviews of that server software?）

7. 理论上系统设置可能在计票日当天晚上暂停计票的那段时间被修改。直接修改几百台计票设备的系统设置远比造几千张假选票容易得多。这只需要一两个人就能办到。（Settings could theoretically have been changed during evening downtime on first night of voting. Much easier to change settings on hundreds of machines than to forge thousands of ballots. A couple of people could have done it quickly.）

8. 宾西法尼亚州对Dominion软件进行了文字语义的更改。“生效”（Cast）被改为“印制”（Print），这让投票者无法确切地知道自己的投票什么时候生效。宾西法尼亚并没有公布这个修改的原因。（State of Pennsylvania requested semantic changes to the Dominion voting software, possibly to aid in their lawfare efforts. The word “Cast” became “Print”, obfuscating the moment when your vote becomes officially cast. For what reason is currently unknown.

9. There is an option to force the vote scanner to “overrun” a preset amount of ballots EVERY time anybody pauses the scan mid-batch. “Overrun” is undefined. Potential for abuse is high with this function, which was added shortly after 2018 mid-term elections.）

Dominion有一个在2018年中期选举后不久被添加的“超额处理”(Overrun)选项。这个选项允许任何人只要中途暂停扫描就能强制选票扫描器处理超出原定限额的投票数量。这个功能极有可能被用来作弊。

我们相信以上从公开信息中发现的疑点只是冰山一角。Deep State在整个投票舞弊案中的违法犯罪行为应该远远超出普通人想象能力。我们相信美国法律会让这些破坏美国民主法制的犯罪团伙付出应有的代价。美国的民主法制将继续成为全球文明的灯塔。



![](https://lh5.googleusercontent.com/zTONqONK6lAVWRUIx-cr03juz9KhkYQdB83pdzoj3Xgqk2fF1ZVzvIxyKS2kc7duwUSy38sJTipmWHs2NVrWhYwK9m4RWAM0xABiWx6FKhYOIl-4ahESztASTt6lFg)

英文参考资料链接：

网友推文原文：**https://twitter.com/codemonkeyz/status/1326715838850764802?s=24**

**Dominion选举计票系统相关的公开文档：**

[https://www.dos.pa.gov/VotingElections/Documents/Voting%20Systems/Dominion%20Democracy%20Suite%205.5-A/Dominion%20Democracy%20Suite%20Final%20Report%20scanned%20with%20signature%20020119.pdf](https://www.dos.pa.gov/VotingElections/Documents/Voting%20Systems/Dominion%20Democracy%20Suite%205.5-A/Dominion%20Democracy%20Suite%20Final%20Report%20scanned%20with%20signature%20020119.pdf)

[https://www.eac.gov/sites/default/files/voting\_system/files/Dominion\_Voting\_Systems\_D-Suite\_5.5\_Test\_Report\_Rev\_A.pdf](https://www.eac.gov/sites/default/files/voting_system/files/Dominion_Voting_Systems_D-Suite_5.5_Test_Report_Rev_A.pdf)

[https://www.sos.texas.gov/elections/forms/sysexam/oct2019-mechler.pdf](https://www.sos.texas.gov/elections/forms/sysexam/oct2019-mechler.pdf)

0

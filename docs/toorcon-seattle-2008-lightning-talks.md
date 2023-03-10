# 西雅图 2008:闪电对话

> 原文：<https://hackaday.com/2008/04/22/toorcon-seattle-2008-lightning-talks/>

第二个 ToorCon Seattle 上周五在公共书呆子区进行了一轮[闪电会谈](http://seattle.toorcon.org/2008/conference.php)，开局很快。每场讲座限于 5 分钟，涵盖广泛的主题。一些会谈只是提供大量信息，而其他的则是呼吁个人项目的行动。这里有一些我们觉得有趣的演讲。

(I)ruid]开篇解释了他的手柄，因为他因为它是 l33tsp34k(应该是大写的“I”)而受到了很多批评。事实证明，这个名字非常有趣，因为它打破了一些不能正确过滤输入的系统。在黑帽 2006 注册导致数据库错误。在 ShmooCon 黑客街机上，他输入了自己的玩家名字，然后直接被丢到了一个 root shell。它在许多网络应用程序上也相当糟糕。他的观点是:为什么不选择一个 l33t 的名字，并且即使在你不尝试的时候，也能享受总是弄模糊和打破东西的乐趣呢？

[nous]为 Ninja Network 的 phreaking 大赛做了一个快速的宣传。去年的 Defcon 是他们举办的第一个活动。第一项任务是在 25 对块上使用[对接集](http://en.wikipedia.org/wiki/Lineman's_handset)来找到可用的线。一旦随机线路被发现，他们就被放入语音邮件系统进行探索。比赛的后台是[星号](http://www.asterisk.org/)加上一些定制的 Perl 脚本。下个月你可以在 LayerOne 看到这个比赛的预览版[。](http://layerone.info/?page_id=29)

[jrandom]谈到了刮刮卡的玩法。使用明亮的灯光或表面笔可以帮助你玩需要一定刮刮乐顺序的游戏。其他卡片可以通过生产过程中发现的迹象来识别。赢家和输家通常分两批生产。每组的卡片都有相同的切割质量、对齐缺陷、印刷颜色，甚至字体也会改变。有时，卡片上甚至有代码来表示获胜者(可能是简单的 W 和 L)。所有这些都很棒，但制造商可能只是为了引起注意而故意这样做。

【Travis Goodspeed】为了兼容性，简单介绍了一下 [Econolite ASC/3 红绿灯控制器](http://www.econolite.com/products/controllers/controllers.asp?product=asc3)的倒车。这是一个运行 VxWorks 5.x 的 PowerPC 机器，支持 snmp 和 FTP。FTP 提供简单的匿名访问。所有的控制值都存储在 ASC3 中。被校验和的 DB 二进制文件。[Travis]建立了一种方法来[将二进制文件结构描述为 XML](http://frob.us/projects/mmg/)并生成用于以多种语言原生读取二进制文件的库。

我们也认为[迪安·皮尔斯]的[网络测试可视化框架](http://code.google.com/p/seedsofcontempt/)很有趣。[Joel Voss]试图为 IAX2 协议编写一个软电话，结果使用了 Asterisk。来自攻击者的 30kB 可能会导致来自 Asterisk 的大量数据包。他现在有了一个[框架来测试协议](http://www.altsci.com/concepts/page.php?s=asteri&p=2)的所有方面。
# 推特墙开关让荷兰黑客知道什么时候该玩了

> 原文：<https://hackaday.com/2011/03/08/twittering-wall-switch-lets-dutch-hackers-know-when-its-time-to-play/>

![hackerspace_open_switch](img/8e760bc6ddfc8cc8b71369449416f09d.png "hackerspace_open_switch")

荷兰阿纳姆的黑客空间 Hack42 最近搬进了一些新的住所，他们想要一种简单的方法让他们的成员知道他们是否营业。固定的工作时间通常不适合这种组织，所以这是不可能的。取而代之的是，他们在墙上安装了一个开关，让会员知道他们何时开始营业。

该交换机将两个以太网端口的 TX 和 RX 引脚分开，这两个端口位于嵌入墙壁的旧接入点中。当黑客空间打开时，开关打开，电路闭合。cron 作业每分钟检查一次 eth1 端口的状态，一旦注意到状态变化，就向 Twitter 和 IRC 发送“Open”状态消息。当再次扳动开关，eth1 端口关闭时，会广播一条“关闭”消息。

这是一个简单但很酷的黑客，非常适合黑客空间。

* *没有直接的谷歌翻译链接，尽管 Chrome 会毫无问题地为您翻译。

[谢谢，_Danny_]
# 监控桶容量、二氧化碳和温度

> 原文：<https://hackaday.com/2009/12/14/monitor-keg-volume-co2-and-temp/>

![](img/28c6f1825a85c7c8067223c25d616b83.png "keg_display")

[Jean-Michel]向我们透露了他的[啤酒桶监控设置](http://www.vachementcool.com/MooSpace/Blog/Entries/2009/11/1_I_built_a_Kegbot.html)。它可以告诉你每个桶里还有多少啤酒，罐子里还有多少二氧化碳，它还可以监控和调节温度。

Arduino mega 是系统的大脑。建造了一个屏蔽来连接力传感器，测量桶的重量来估计还有多少啤酒。模拟温度传感器允许温度监测和压缩机调节控制。信息可以通过 XBee 无线通信显示在图形 LCD 或计算机上。

这是沿着 [SparkFun kegerator](http://hackaday.com/2009/09/10/sparkfun-kegerator-goes-to-eleven/) 的路线，但我们喜欢增加的功能。这需要推特吗？可能不会，但是如果你想要的话，只需要一点软件就可以了。
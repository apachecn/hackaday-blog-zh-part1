# 用您最喜欢的微控制器控制基于 X10 的家庭自动化

> 原文：<https://hackaday.com/2012/01/17/commandeer-x10-based-home-automation-with-your-favorite-microcontroller/>

![](img/23825f6229edbc3de648cb302be8a692.png "firecracker_interface")

X10 已经存在很久了。这是一套用于开关家中电气设备的无线模块的品牌名称。有各种不同的单元(灯泡插座、电源插座和插头通道等。)而且它们是大规模生产的，所以非常便宜。无论你已经有一些 X10 控制的设备，还是只是计划以后添加它们，我们认为你会发现[Jeff Ledger]关于[用螺旋桨芯片控制系统的帖子很有趣](http://www.gadgetgangster.com/news/45-designer-news/524)。该技术不是特定于螺旋桨的，可以简单地移植到你选择的微控制器上。

[杰夫]他手上有一个 X10 的鞭炮。这提供了一个用于计算机控制的 DB-9 串行连接。但是接口非常简单，你只需要两个 I/O 引脚来为上面看到的电平转换器电路供电。你可以用不到一美元买到 TC4427，而 Firecrcker 模块只需 6 美元。由于[Jeff]已经介绍了通过 ENC28J60 添加以太网，他继续详细介绍了一个让他可以切换设备的网络服务器，所有这些都是由 Propeller 芯片提供的。

这里有[一个不同的 ENC28J60 以太网教程](http://hackaday.com/2010/07/08/stepping-beyond-the-ethernet-shield/)给那些对微控制器网页感兴趣的人。如果你对使用 X10 模块的想法不感兴趣，那么还有一个 ZigBee 家庭自动化项目。
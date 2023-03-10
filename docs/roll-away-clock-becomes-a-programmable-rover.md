# 滚动时钟成为一个可编程的漫游者

> 原文：<https://hackaday.com/2011/03/22/roll-away-clock-becomes-a-programmable-rover/>

![](img/9ce8bc3f30b49dba6758963ba7491917.png "roll-away-clock-becomes-programmable-robot")

上图中裸露的部分组成了一个可滚动的闹钟，当你不起床时，它就会逃跑。这是一个有趣的想法，但考虑到大多数人不会睡在硬木地板上，我们可以理解为什么[TheRafMan]能够以低于 5 美元的价格买到这块宝石。这是一笔不小的交易，因为顶部有一个非常有用的 LCD 模块。但在这次黑客行动中，他专注于使用齿轮头马达制造可编程漫游车。

为了实现这种可编程,[TheRafMan]必须添加一个微控制器。他选择了一个 Arduino 变种，叫做 Ardweeny。这是一块搭载 ATmega328 的电路板。但是他没有使用股票。[他已经改变了它](http://www.instructables.com/id/Ardweeny-2-How-to-customize-an-Ardweeny/)来很好地玩跳线。由于 L293D h 桥电机驱动芯片，uC 能够与齿轮头电机接口。正如你在跳跃后的剪辑中看到的，现在可以使用 Wii 双截棍或通过 USB 连接来驱动漫游车。如果你有一个蓝牙模块，这就不难成为一个无线解决方案，可以用 Wii 遥控器上的加速度计来控制。

[https://player.vimeo.com/video/21343780](https://player.vimeo.com/video/21343780)
# NES 控制器得到一个隆隆声巴基斯坦

> 原文：<https://hackaday.com/2010/10/11/nes-controller-gets-a-rumble-pak/>

![](img/4156a6277508d643282b0a09a7727fbc.png "nes-rumble-pack")

通过使 NES 控制器振动，为其增加一些反馈。这个功能通常被称为[隆隆](http://en.wikipedia.org/wiki/Rumble_Pak) [帕克](http://en.wikipedia.org/wiki/Rumble_Pak)，这是任天堂 64 的一个控制器附件，它作为一个游戏功能振动。这个版本增加了一个小的 DC 电机(在右上方),一个螺丝偏心焊接到电机轴上。

[Andy Goetz]和他的朋友建造了这个机器人控制器，利用了闩锁和时钟引脚。正常情况下，当两个引脚都保持高电平时，什么都不会发生，这是一个信号，使用“与”门很容易将其接入。这实际上是一个巧妙的发现，因为当锁存器为高电平且时钟被选通时，添加内部微控制器可以增加双向通信。
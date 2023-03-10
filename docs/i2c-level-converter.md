# I2C 电平转换器

> 原文：<https://hackaday.com/2011/12/07/i2c-level-converter/>

![](img/d237a6e4e84903dc3ceba3628ccf716c.png "i2c-level-converter")

您有几个通过 I2C 协议通信的设备，但其中一些只能在 3.3V 下工作，而其余的则渴望 5V 连接。怎么办？[Linux-works] [建造了这个 I2C 电平转换器](http://www.flickr.com/photos/linux-works/6433044007/)来解决这个问题。

该电路来自关于该问题的恩智浦应用笔记 (PDF)。你可以快速地[瞥一眼那份文件中的建议原理图](http://www.flickr.com/photos/linux-works/6433372523/)。该设计在适配器的每一侧使用两个 MOSFETS。或许更好的解释方式是，在总共四个器件的两条数据线上，一条用于较高电压，一条用于较低电压。这允许两条总线作为一条总线进行通信，同时仍有各自的 3.3V 和 5V 上拉电阻。

[Linux-works]承认有专门为你设计的芯片，但他能够在当地采购 BSS138 MOSFETs，每片大约 10 美分。这是订购零件的一个不错的选择。
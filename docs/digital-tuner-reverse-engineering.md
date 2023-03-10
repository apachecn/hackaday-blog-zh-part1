# 数字调谐器逆向工程

> 原文：<https://hackaday.com/2009/10/27/digital-tuner-reverse-engineering/>

![hvr-1600-i2c-sniffing](img/157f358e9bbe200d79db7f10252a91a0.png "hvr-1600-i2c-sniffing")

黑客校友伊恩·莱斯内特向我们透露了 HVR-1600(一种模拟和数字电视编码器/调谐器)的一些 T2 逆向工程。当[Devin]注意到他的 Hauppauge HVR-1600 在 Linux 中不能像在 Windows 中那样很好地调谐频道时，这个项目诞生了。他有预感这是由于调谐器芯片或解调器的初始化设置不正确。

为了解决这个问题，他在板上用两个测试点接入 [I2C 总线](http://en.wikipedia.org/wiki/I2c)。使用[一个逻辑分析器](http://hackaday.com/2009/03/06/tools-saleae-logic-logic-analyzer/)，他在运行 Linux 时捕获了来自总线的命令流量，然后在运行 Windows 时捕获。通过使用一点 Perl 过滤结果，并使用 [diff](http://linux.die.net/man/1/diff) 比较它们，他追踪并找到了两个驱动程序发送的命令的差异。在研究了 Linux 源代码并做了必要的修改之后，他提高了 Linux 包的调优能力。

[Devin]的工作看起来足够简单，事实也的确如此。这个过程的困难之处在于足够聪明地知道你在寻找什么，以及一旦你找到了，你会得到什么。
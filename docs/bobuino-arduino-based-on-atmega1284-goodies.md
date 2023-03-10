# Bobuino:基于 ATmega1284 + Goodies 的 Arduino

> 原文：<https://hackaday.com/2011/08/17/bobuino-arduino-based-on-atmega1284-goodies/>

![](img/ab3e23332a0eb9191f33c869a6a13ba0.png "bobuino")

[Erik]写信告诉我们他刚刚完成了 Bobuino 的开发，这是一款基于 atmega 1284 的 Arduino。该芯片漂亮而结实，最明显的是具有 16 KB 的 SRAM，但它也拥有 4 KB 的 EEPROM 和 128 KB 的程序存储器。

但是升级的芯片并不是它带来的唯一东西。很容易发现上图中的板载 SD 卡插槽。同样值得注意的是电池供电的 DS1307 实时时钟，它带有一个跳线，可以将方波输出路由到微控制器上的两个引脚之一。

这种设计与标准 Arduino 屏蔽兼容，这得益于熟悉的一对引脚插座，并且仍然可以通过 USB 插座进行编程。由于 AVR 芯片比普通芯片有更多的 IO，所以也有引脚头来断开 PORTC 引脚，用于 JTAG 连接器和 RS232 端口。
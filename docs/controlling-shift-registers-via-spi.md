# 通过 SPI 控制移位寄存器

> 原文：<https://hackaday.com/2011/11/05/controlling-shift-registers-via-spi/>

![](img/895981fc7c4aa23a62775153b3ea06b1.png "spi")

Hack a Day 自己的(也是非常多产的贡献者)[Mike Szczys]提供了一个关于如何用 SPI 接口驱动移位寄存器的教程。

[Mike]早先的 595 移位寄存器的[教程逐个引脚地介绍了移位寄存器的功能。在 a 595 中，寄存器中每个位置的位一次发送一位。大多数微处理器都有一个串行外设接口，使用 SPI 总线意味着少了很多麻烦。](http://jumptuck.com/2011/11/02/how-shift-registers-work/)

ATmega168 用于这一构建，尽管大多数 Atmel 芯片[可以作为 SPI 主设备工作。只有三条线将微控制器连接到移位寄存器——SER、SRCLK 和 RCLK。像任何其他移位寄存器设置一样，可以通过将第一个 595 的 QH 引脚连接到第二个 595 的 SER 引脚来扩展构建。](http://arduino.cc/playground/Code/USI-SPI)

[Mike]大方地提供了他的版本的所有代码。休息后的视频是一个 16 位二进制计数器，这是[迈克]重建他的[拉森扫描仪/赛昂/凯特](http://jumptuck.com/2011/10/27/developing-a-larson-scanner/)之前的一个很好的停止点，从基于 PWM 的构建转移到基于寄存器的构建。

[https://www.youtube.com/embed/_goH3VUTHvI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_goH3VUTHvI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
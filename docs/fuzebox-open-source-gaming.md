# Fuzebox，开源游戏

> 原文：<https://hackaday.com/2008/11/25/fuzebox-open-source-gaming/>

![fuzebox](img/106cc35541a7e5e587e5f2fbd6483eb1.png "fuzebox")

Adafruit 刚刚将他们基于 Uzebox 的控制台投入生产。 [Fuzebox](http://www.adafruit.com/index.php?main_page=index&cPath=30 "Adafruit Industries, Unique & fun DIY electronics and kits") 是一款基于 ATmega644-20PU 微控制器的 8 位游戏控制台。全 256 色 240×224 分辨率视频输出由复合连接或 svideo 提供。板上有一个 SD 卡插槽，用于将来扩展。芯片负责所有的 I/O，所以你只需要在它上面用 C 写你的游戏代码。

这个套件看起来很容易组装。几乎所有的元件都是通孔的。视频芯片是 SMD，预焊在电路板上。该套件包括两个 SNES 控制器端口，但你也可以使用 [NES](http://www.mahalo.com/Nintendo_Entertainment_System "Nintendo Entertainment System - Mahalo") 端口。有三种方法可以将程序载入电路板:6 引脚 FTDI、ICSP10 和 ICSP6。
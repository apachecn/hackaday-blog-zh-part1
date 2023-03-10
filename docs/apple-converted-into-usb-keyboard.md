# 苹果][转换成 USB 键盘

> 原文：<https://hackaday.com/2011/06/06/apple-converted-into-usb-keyboard/>

![](img/4b1e998c089804d21681fc3fc57d17fe.png "appleII")

有时候，Hack a Day 上的东西显然没有实际用途，但我们不知道[安德鲁·菲勒]的[苹果][ USB 键盘](http://afiler.com/apple-ii-plus-as-a-usb-keyboard/)是否符合这一条件。

在通读了电子版和死树版的非常详尽的文档后，安德鲁认为苹果会制造出一个伟大的 USB 键盘。与现代键盘不同，像 TRS-80、Commodore 64 和 Apple 这样的老式电脑会返回 7 位 ASCII 值的按键，而不是扫描码。键盘生成的 ASCII 码通过一个运行着【安德鲁】的[键盘的](https://github.com/afiler/keyduino)草图的 Teensyduino 发送。

[现代 PS/2 键盘](http://www.computer-engineering.org/ps2keyboard/)使用读取键盘矩阵的微控制器发送的接通和断开扫描代码。例如，字母“A”的接通代码是 1C，而断开代码是 F0 1C。这种设计是有原因的，但对于 DIYer 来说，如果没有独立的微控制器，连接键盘就成了一个挑战。我们认为[Andrew]的 keyduino 可能是在项目中放置键盘的一种很好的方式，但我们不会为了得到键盘而毁掉我们的苹果和 c64。
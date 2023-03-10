# PIC 供电的 AVR 编程器

> 原文：<https://hackaday.com/2009/11/18/pic-powered-avr-programmer/>

![](img/c406aa01b585a1781721302519794979.png "pic-powered-avr-programmer")

[Texane]写信告诉我们他已经使用 PIC 微控制器实现了 [AVR ISP 编程。他为 18F4550 编写了一些代码，这些代码使用 STK500 标准进行系统编程。这意味着他的硬件与开源 AVR 编程软件](http://github.com/texane/picisp) [AVRdude](http://savannah.nongnu.org/projects/avrdude) 兼容。关于 PIC 和 AVR 孰优孰劣的争论由来已久，但我们说为什么不能两者兼得呢？如果您已经用 PIC 磨练了您的编程能力，您可以构建自己的程序员并尝试一下 Atmel 系列。

当前的实现使用串行端口将编程器连接到计算机。请密切关注这一点，因为[texane]计划添加 USB 连接，并告诉我们，一旦完成，他将发布该设备的原理图。
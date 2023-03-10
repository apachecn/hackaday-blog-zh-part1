# Versaloon 可以对几个制造商的硬件进行编程

> 原文：<https://hackaday.com/2010/12/25/versaloon-can-program-hardware-from-several-manufacturers/>

![](img/14db9a670669da65ea598a8cfbd1f030.png "versaloon-nano")

Versaloon 是一个开源的 USB 连接项目，它以一个 [STM32 处理器](http://hackaday.com/2010/10/12/arm-prototyping-on-the-cheap-with-stm32-discovery/)为中心，并提供一个标准的 JTAG 引脚排列。上面你看到的是 Nano 版本，它有一个 10 针的 JTAG 连接器，但在 Handy 模型上也有一个 20 针的选项。太好了，又一个 JTAG 程序员。这个可以做更多的事情。在软件的一点帮助下，它已经变成了十种不同硬件的编程器。显然，这应该能够编程任何与 JTAG 协议一起工作的东西，但是脚本也使它适合作为系统内(或电路内)程序员工作。到目前为止[的编程目标列表](http://www.versaloon.com/doc/versaloon/doc_versaloon_programmer_platform.html#doc_versaloon_programmer_connection_to_targets)包括 STM32、LPC1000、LPC900、STM8、AR8、MSP430 和其他一些。

我们很难找到这个硬件的实际图片。如果你有一个，拍一张照片，在评论中留下链接和你对这个设备的想法。

[谢谢 Geekabit]
# FPGA 上的 AVR8 虚拟处理器

> 原文：<https://hackaday.com/2009/11/19/avr8-virtual-processor-on-fpga/>

![](img/ea244eab0b57e960bd66e1b7c6201f34.png "butterfly-fpga-platform")

[Jack]来信让我们了解一个[项目，该项目通过使用现场可编程门阵列，基于 ATmega103 创建了一个虚拟微处理器内核](http://www.gadgetfactory.net/gf/project/avr_core/)。太好了，我们想。这是另一个相当深奥的项目，像 FPGA 上的 NES T2，但是它背后的动机是什么？我们询问了[Jack]，他提供了几个非常有用的场景。

实施 AVR 内核允许将已经为芯片编写的代码轻松移植到 FPGA，而无需重写代码。这样，如果在项目开始后很长一段时间内，您的需求超出了微控制器的能力，您可以保留代码，并从该点开始利用门阵列的附加功能。已经实现了核心之后，您只需要使用 HDL 来处理 AVR 无法处理的项目部分。他还指出，拥有一个开源 AVR 核心实现为已经熟悉 AVR 的人在学习 VHDL 时提供了一个很好的工具。

有了像这个项目所围绕的蝴蝶，或者我们过去见过的[枫树](http://hackaday.com/2009/08/22/maple-beats-up-arduino-takes-its-shields/)这样的产品，[可编程逻辑](http://hackaday.com/2008/12/11/how-to-programmable-logic-devices-cpld/)对于休闲黑客来说开始变得更容易了。
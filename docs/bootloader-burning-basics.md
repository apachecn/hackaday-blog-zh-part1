# 引导加载程序刻录基础知识

> 原文：<https://hackaday.com/2011/08/17/bootloader-burning-basics/>

![](img/5ad3fec297f19489e19e2fc23e540f5e.png "bootloader-burning")

[Charles Gantt]和其他几个人在将 Sanguino 引导程序刻录到 ATmega644 芯片时遇到了问题。在[Nils Vogil]通过 RepRap IRC 提供的一些帮助下，[Charles]解决了这个问题，并以 ISP 程序员的身份写了一个使用 Arduino 烧录引导程序的指南。

我们不熟悉 Sanguino 引导程序的具体细节，但[Charles]提到，如果没有谐振器，他无法将其闪存到 AVR 芯片上。谐振器充当芯片的外部时钟源。我们打赌编程过程会改变芯片上的保险丝设置，以使用外部电源。没有那个信号源，你以后就不能和芯片交流了。

该解决方案只是将谐振器添加到编程电路中。这在使用 Arduino 刻录任何引导程序时会很有用。但这确实让我们想知道，是否有一种替代方法可以让你从 Arduino 本身提取时钟信号？
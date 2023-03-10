# 自动 JTAG 引脚检测

> 原文：<https://hackaday.com/2007/09/29/automatic-jtag-pinout-detection/>

![](img/01ef4bf02d0515dba14e1f98cc8c4feb.png)

在许多黑客攻击中，找出设备上的 JTAG 引脚是最耗时的硬件部分。[hunz]启动了一个名为 [JTAG 探测器](http://www.c3a.de/wiki/index.php/JTAG_Finder)的项目，使用 8 位 AVR ATmega16/32L 微控制器自动检测任意设备上的 JTAG 引脚。请查看演讲中的[幻灯片](http://hunz.org/jtag.pdf) (PDF)，它们详细说明了如何在任意设备上找到 JTAG 端口，无论有无引脚检测工具。[hunz]正在找人接手他中断的项目。

一旦你确定了正确的引脚排列，你将需要一个 JTAG 电缆:有两种主要类型，缓冲和无缓冲，这两种都是我从这些电路图中焊接和测试的(完整的缓冲电缆图[在这里](http://hackaday.com/wp-content/uploads/2007/09/jtagbuffered.jpg))。今天大多数硬件人使用的软件是 [openwince JTAG 工具](http://openwince.sourceforge.net/jtag/)。要让 JTAG 工具编译，直接从他们的 CVS 库获取最新的源代码。

我们上一次介绍 JTAG 是在 Linksys 设备上的[，但是上面列出的工具可以应用到任何带有 JTAG 的设备上。](http://www.hackaday.com/2006/04/07/dd-wrt-running-on-wrt54g-version-5/)

*   [永久链接](http://www.c3a.de/wiki/index.php/JTAG_Finder)
# 初学者概念:级联移位寄存器

> 原文：<https://hackaday.com/2010/05/31/beginner-concepts-cascading-shift-registers/>

![](img/9f758d42fdaf58d51c13dc3dfddd22f0.png "shift-register-tutorial")

有上百万的教程描述了如何使用移位寄存器。如果你刚刚进入嵌入式系统，你应该知道如何使用它们，因为它们允许你使用三个微控制器引脚，并几乎无限制地扩展它们。这是由于这些集成电路的串行输入并行输出特性。这些芯片的一个关键特征是能够溢出，或者级联到下一个芯片，这提供了可扩展性。

Protostack 刚刚发布了一个教程，使用这个硬件通过两个移位寄存器来[连接 16 个 led。解释简明扼要，并附有易于理解的代码示例。他们干净利落的面包板工作也值得一提。](http://www.protostack.com/forum/blog.php?u=2&b=35&sid=50384afa8d72f982e6ce2b736934eefc)

看看他们是如何做到的，然后用这个概念[制作一个别致的时钟](http://hackaday.com/2009/09/21/blokclok-abstract-time-display/)或者减少[驱动显示器](http://hackaday.com/2008/06/13/3-wire-lcd-display/)所需的引脚。
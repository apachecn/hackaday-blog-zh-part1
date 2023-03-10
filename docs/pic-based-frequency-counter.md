# 基于 PIC 的频率计数器

> 原文：<https://hackaday.com/2011/03/15/pic-based-frequency-counter/>

![](img/9d8af893512fadd4741ecc3019fa1f19.png "pic-frequency-counter-uses-pc")

这里的[是一个基于 PIC 的频率计数器](http://panteltje.com/panteltje/pic/freq_pic/)，它通过 RS232 串行连接输出计数。在看到[我们昨天展示的基于 AVR 的计数器](http://hackaday.com/2011/03/14/frequency-counter-for-10-worth-of-parts/)后，他向我们透露了这个消息。这个项目有点老，有点脏。

在金属 DB9 外壳内，你会发现只有七个部分。最重要的是 PIC 16F628，它处理计数和串行通信。我们不太确定它是如何在没有某种电平转换的情况下与 USB 转串行转换器进行对话的。由于该微控制器不是专用计数器芯片，因此必须进行一点微调，以使精度符合规格。还涉及一些物理修整。为了让一切都适合小外壳，电路是自由形成的，没有 PCB 或原型板，DIP 芯片的外壳必须稍微接地。至于读数，一个简单的脚本可以获取数据并在终端中显示出来。

[via [Piclist](http://www.piclist.com/techref/microchip/freq2rs232-jp.htm) ]
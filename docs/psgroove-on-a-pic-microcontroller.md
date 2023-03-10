# PIC 微控制器上的 PSGroove

> 原文：<https://hackaday.com/2010/09/15/psgroove-on-a-pic-microcontroller/>

![](img/2d1e0890a99be05cede6ec742f8c0b2d.png "psgroove-pic-uc")

现在有一种使用 PIC 微控制器开发 PlayStation 3 的方法。这是围绕一个 PIC 18F2550，它一直是[在过去的黑客](http://hackaday.com/2010/08/05/rgb-vu-meter/)流行，因为它内置的 USB 串行端口。这再次利用了[PS groove 开源利用代码](http://hackaday.com/2010/09/01/open-source-version-of-the-play-station-3-jailbreak/)，并且像[TI 计算器版本](http://hackaday.com/2010/09/10/playstation-3-exploit-using-a-ti84-calculator/)一样，寻求扩展代码运行的硬件选择。

除了芯片和 PIC 编程器，你还需要 CCS 编译器，因为其他人无法成功编译这段代码。因为 CCS 编译器的演示版本不支持这种特殊的芯片，所以需要一个许可的副本。此外，由于时间的原因，可能需要多次尝试才能利用漏洞，您可能会发现自己对这一发展感到失望。但总有改进的空间，这是新架构经过验证的第一步。

【感谢 das _ coach via[PS 3 hax](http://www.ps3hax.net/downloads.php?do=file&id=399)via[Elotrolado](http://www.elotrolado.net/viewtopic.php?f=179&t=1479909&p=1721567279#p1721567279)
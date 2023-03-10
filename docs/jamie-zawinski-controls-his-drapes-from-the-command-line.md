# [杰米·扎温斯基]从命令行控制他的窗帘

> 原文：<https://hackaday.com/2012/01/14/jamie-zawinski-controls-his-drapes-from-the-command-line/>

![](img/a3b88481f58a563fcdcb60353df9f423.png "curtain")

作为 Netscape 和 Mozilla 项目的创始人之一，[Jamie Zawinski]对由语法错误、糟糕的实现以及本该工作却无法工作的事情所引发的挫折感并不陌生。这种对挫败感的熟悉是【jwz】的[命令行控制的窗帘](http://www.jwz.org/curtain/)如此伟大的原因；很少看到如此精通技术的人因为 Arduino 以太网上缺少 DHCP 而抓狂。

[Jamie]的项目像许多人一样开始——修改一个现有的硬件来连接互联网。这说起来容易做起来难，因为[Jamie]同时烧坏了 USB 集线器、FTDI 电缆和 Arduino 以太网。终于打开了[seed 中继盾](http://seeedstudio.com/wiki/Relay_Shield)，【jwz】忙着写剧本为他的幕布供电。

当然，如果没有良好的集成，这种程度的自动化就什么都不是。在[杰米]意识到他的投影仪(一台松下 PT-D5500U)和接收器(Denon AVR-2805)可以与他的电脑对话后，他开始忙着用 Griffin PowerMate 将它们混合在一起。按住 PowerMate 上的按钮可以打开投影仪并关闭窗帘。还有一个 cron 作业正在运行，这样[杰米]就会想起天空中发光的橙色球。
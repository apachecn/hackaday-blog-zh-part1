# 微型 USB 名片

> 原文：<https://hackaday.com/2010/10/29/tiny-usb-business-card/>

![](img/39361552a4f03946872b54541fbbbbb4.png "usbbusinesscard_1")

[Frank Zhao]组装了一张 USB 名片。它甚至把说明书印在印刷电路板的丝网上，解释如何使用它。他的设计基于 AVR ATtiny85 微控制器。它运行处理 USB 识别和通信协议的 V-USB 包。硬件的其余部分相当标准，uC 从 5V USB 轨获取电源，用一对 3.6V 齐纳二极管将两条数据线降至适当的水平。

一旦插上电源，它会一直等待，直到连续检测到三个 caps lock 键，然后吐出一串自己的按键，在文本编辑器窗口中键入[Frank 的]联系信息(休息后的视频)。它不像大容量存储名片那样可重复使用，因为【弗兰克】没有断开控制器上的引脚。但是我们仍然喜欢看到让你脱颖而出的[名片。](http://hackaday.com/2008/12/01/gears-embeded-in-busines-cards/)

这是一个用你新获得的 AVR 编程技能来解决的伟大项目。

[https://www.youtube.com/embed/vX1tDk_iwOo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vX1tDk_iwOo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢哈拉尔德]
# 用 PIC 连接光电鼠标

> 原文：<https://hackaday.com/2011/01/28/patching-into-an-optical-mouse-with-a-pic/>

![](img/9a9ad5c12658400fd3d67ba9de427f91.png "mouse-pic-communications")

[MikyMouse]打开了几个不同的光学鼠标(或者是鼠标？)以便[处理来自](http://ferretrobotics.blogspot.com/2011/01/interfacing-optical-mouse-usb-with-pic.html)内部芯片的数据通信。一旦他弄清楚了协议，获取数据用于他自己的项目并不困难。控制鼠标的芯片是他观察的两个芯片之一，不是 ADNS2051 就是 ADNS2610。它们在 5V 电压下运行，通过 SDIO 和 SCK 引脚使用串行通信。休息之后的剪辑显示了测试设备在 LCD 屏幕上显示鼠标的坐标。这似乎是一种从项目中获取位置数据的简单而廉价的方法。唯一棘手的部分是决定何时以及如何将地点归零。

对这种类型的鼠标攻击不感兴趣？我们可以用这个[鼠标自动开火项目](http://hackaday.com/2010/12/20/adding-auto-fire-to-a-computer-mouse/)来激发你的好奇心吗？

[https://www.youtube.com/embed/ccebebWv_fI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ccebebWv_fI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
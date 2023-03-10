# 即兴灯运行 Linux

> 原文：<https://hackaday.com/2011/12/15/impromptu-lamp-runs-linux/>

![](img/1bcdc5c3f54828136df7e5d91883f4d8.png "linux-lamp")

这种 LED 灯使用汽水杯作为灯罩，多亏了 Linux 板 ( [翻译](http://translate.google.com/translate?sl=auto&tl=en&js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&u=http%3A%2F%2Fchuckoggy.wordpress.com%2F2011%2F02%2F19%2Flampeweb%2F))才能够[上网。说这个系统被压制是一种保守的说法。但至少还有很大的增长空间。](http://chuckoggy.wordpress.com/2011/02/19/lampeweb/)

lamp 实际上只是 Linux 板的硬件扩展。六个彩色发光二极管由一个 ATmega8 和几个晶体管驱动。Fox LX832 板通过 i2c 协议将颜色指令推送到微控制器。[Gibus]选择这款主板是因为它有一个内置的以太网端口，非常适合通过智能手机浏览器进行通信。这是该项目的大部分工作发生的地方。他编写了一个 Flash 应用程序，可以让你从任何不运行 iOS 的设备上选择颜色、色调和饱和度数据。这些命令由运行在 Linux 板上的 C 应用程序处理。观看 web 应用程序的演示，以及中断后剪辑中的颜色变化。

[https://www.youtube.com/embed/Rw4Dijq4AkU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Rw4Dijq4AkU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
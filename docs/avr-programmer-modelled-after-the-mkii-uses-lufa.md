# 模仿 MkII 的 AVR 编程器–使用 LUFA

> 原文：<https://hackaday.com/2011/07/30/avr-programmer-modelled-after-the-mkii-uses-lufa/>

![](img/9254949cba7c697cc877dc6e87e63225.png "mkii_slim_3")

这里有一个新的选择来建立你自己的 AVR 程序员。它被称为 MkII Slim T1，小巧的尺寸让它名副其实。这个设计相当简单，只使用了三个芯片；电压调节器、MAX3002 电平转换器和 Atmel AT90USB162 作为主微控制器。该芯片内置 USB 模块，无需单独的 FTDI 芯片。

固件构建在用于 AVR(LUFA)的[轻量级 USB 框架上。这是一个 USB 堆栈实现，最初称为 MyUSB，由[Dean Camera]开发。AVRfreaks 论坛上的常客会认出[Dean]的名字或他的昵称[abcminiuser]是那里许多高质量 AVR 教程的来源。但是我们跑题了。](http://code.google.com/p/lufa-lib/)

程序员提供了你想要的系统内程序员的所有特性。由于芯片上运行的引导加载程序，它可以很容易地用未来的更新进行刷新。有跳线可选电源选项，它可以编程目标运行在 3.3V 或 5v。包括代码和插图的完整开发包可以从上面链接的站点下载。为了您的方便，我们在休息后嵌入了原理图。

[![](img/cf7f4dd2c03517fa4a4fd8bb7cd62c04.png "mkII-clone-schematic")](http://hackaday.com/wp-content/uploads/2011/07/mkii-clone-schematic.png)
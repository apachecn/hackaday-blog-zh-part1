# 为您的项目轻松旋转编码

> 原文：<https://hackaday.com/2012/01/02/easy-rotary-encoding-for-your-projects/>

![](img/6a4074ceec47c8b56d6b6580caa19f43.png "rotary-encoder-add-on")

想监控你的项目中一个轮子转动了多少？那么你需要一个旋转编码器！这里有一种方法可以在不改变车轮安装方式的情况下增加旋转编码。[Jorge]添加它是为了提高这个循线机器人的功能。它使用由光学传感器监控的纸质编码器轮。

纸轮由白色和黑色的饼块交替组成。你可以用毡尖记号笔做这个，或者使用类似我们几年前推出的工具[打印出一张按照你自己的规格制作的光盘](http://hackaday.com/2010/06/20/hackaday-links-june-20-2010/)。这是粘在车轮内侧，并由 CNY70 反射传感器监测(在那个[电子键盘改装](http://hackaday.com/2010/10/07/playing-piano-with-optical-sensors/)中使用的同一个)。

可以看到，装有传感器的自制电路板安装在每个车轮电机的顶部。它需要三条线，电压、地和数据。数据线连接到 CNY70 封装中的光电晶体管的输出，因此它可以与微控制器中断一起使用，以便与驱动机器人的固件轻松集成。

[Jorge]详细介绍了添加的数据如何帮助提高速度性能，在休息后的剪辑中可以看到。

[https://www.youtube.com/embed/2SBk3J5ikjM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2SBk3J5ikjM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢汤姆]
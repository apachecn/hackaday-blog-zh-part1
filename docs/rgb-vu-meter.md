# RGB VU 测量仪

> 原文：<https://hackaday.com/2010/08/05/rgb-vu-meter/>

![](img/0b5f9241ea280914c424def6f38740eb.png "VU_Meter_board")

[Simon Inns]生产了这款带有 16 个 RGB 发光二极管的[VU 电表](http://www.waitingforfriday.com/index.php/USB_RGB_LED_VU_Meter)。他在这个项目中使用了三个 16 位 TLC5940NTG LED 驱动器。他们不是便宜的芯片，但他们做得很好。如果你想节省一些部件,[Simon]发现有足够多的亮度，由于多路复用造成的任何损失都不是问题。得益于 PIC 18F2550，该设备通过 USB 连接到计算机，他在[过去的 VU 仪表项目](http://hackaday.com/2010/04/22/usb-vu-meter/)中使用过 PIC 18f 2550。他的设计选择之一是使用开关电源。LM2576 ( [数据手册](http://www.onsemi.com/pub/Collateral/LM2576-D.PDF))在 5V 下提供 3A 电流没有问题，除了两个通常与线性调节器一起使用的电解电容之外，您只需要添加一个二极管和一个电感。

该血糖仪提供了几种不同的配置，这些配置设置在事物的 PC 端。这些包括使用的颜色，以及是否将整个小节用作一个节拍或分成几个部分来显示两个音频通道。休息之后来看看。

[https://www.youtube.com/embed/J3BraNUj2cY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/J3BraNUj2cY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
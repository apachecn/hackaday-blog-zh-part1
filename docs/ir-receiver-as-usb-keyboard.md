# 红外接收器作为 USB 键盘

> 原文：<https://hackaday.com/2010/10/04/ir-receiver-as-usb-keyboard/>

![](img/401f11967efdc54569e611494f2751a0.png "ir-usb-keyboard")

[亚瑟]造了一个红外接收器和 XBMC 一起使用。因为它是特定于软件的，所以他将 USB 上的设备识别为键盘，并将 IR 命令作为流行媒体平台使用的击键来传递。

通常，[自制红外接收器](http://hackaday.com/2008/10/30/how-to-usb-remote-control-receiver/)会使用 [LIRC](http://www.lirc.org/) ，Linux 红外遥控软件。但是这个方法并不要求你运行它。事实上，它不需要在 PC 端进行任何设置。任何使用[索尼 SIRC 协议](http://www.sbprojects.com/knowledge/ir/sirc.htm)的遥控器都可以立即工作。

[Arthur]为该项目选择了 PIC 18f2550。它是一款受欢迎的微控制器，因为它内置了 USB 处理功能。不过，我们对硬件设计有点怀疑。我们没有具体看到他使用的 IR 接收器，但许多需要某种类型的滤波，因此请查看数据手册中针对您的模块建议的布局。
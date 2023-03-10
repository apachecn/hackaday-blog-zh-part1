# 遥控 USB 开关

> 原文：<https://hackaday.com/2011/09/29/remote-controlled-usb-switch/>

![](img/364063e4866f75a7ced3224bcbcba378.png "USB")

当[beerninja]想把他的 USB 键盘从一个游戏机换到另一个游戏机而不用摆弄电线时，他[向 Hack A Day 论坛](http://forums.hackaday.com/viewtopic.php?f=10&t=1144&p=6934#p6934)寻求帮助。[Meseta](又名[UAirLtd])来解救，并为[beerninja]制造了一个[遥控 USB 开关](http://blog.meseta.co.uk/2011/09/ir-controlled-usb-switch.html)。

在打开一个[无名 USB 开关](http://3.bp.blogspot.com/-6P7j7Vdpl7o/Tn61i8Qsd_I/AAAAAAAAAVQ/Vh6sK6fTeKo/s320/2011-09-25-01.34.47.jpg)后，【Meseta】发现开关是用简单的继电器和开关完成的。一个巨大的超功率[前脑臂开发板](http://www.universalair.co.uk/forebrain)被用来拉低每个开关几百毫秒，以切换输出 USB 端口。

对于红外遥控器，[Meseta]钻研了 [Lady Ada 的红外传感器教程](http://www.ladyada.net/learn/sensors/ir.html)并解码了天空电视遥控器上的按钮 1 至 4。从一到四的每个按钮都对应 USB 共享开关上的按钮。“0”按钮也被解码，以方便将前脑置于重新编程模式。在[钻了一个红外接收器的小洞](http://2.bp.blogspot.com/-TjQx0T_uW4s/ToAPDzz3JeI/AAAAAAAAAV0/pzcVtMGriGo/s320/2011-09-26-05.28.36.jpg)后，完成的项目被塞回原来的钢制外壳中。

休息之后，请观看交换机运行的视频。

[https://www.youtube.com/embed/2SHXNDUEl_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2SHXNDUEl_E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
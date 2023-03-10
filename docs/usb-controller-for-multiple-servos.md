# 多伺服系统的 USB 控制器

> 原文：<https://hackaday.com/2011/02/04/usb-controller-for-multiple-servos/>

![USB_controller_for_6_servos](img/5d3d2fe3ed06e1d4de89c29655afda8f.png "USB_controller_for_6_servos")

[dunk]构建了一个易于使用的基于 AVR 的 USB 控制器，能够[一次驱动多达六个遥控业余伺服系统](http://www.societyofrobots.com/member_tutorials/node/25)。虽然他使用的 USB 供电的 Atmega8 为所有伺服系统提供必要的 PWM 信号，但为了提供每个伺服系统所需的 5v 电源，3A 额定电压高达 30v 的外部电源是必要的。他的项目是由[[罗纳德·沙滕](http://www.schatenseite.de/index.php?id=219&L=2)建造的 USB 伺服控制器的扩展，包括几项重大升级。除了增加 5 个伺服系统之外，[dunk]切换到 AVRlib 例程进行多伺服控制和 PWM 管理，并增加了上述电源，以防止 USB 端口上的过度电流消耗。他的教程包括完整的零件列表、Eagle PCB 原理图、所需的 USB 伺服源代码，以及可以发送给伺服控制器的命令样本。
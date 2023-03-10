# 通过 Arduino 进行 AVR ISP 编程

> 原文：<https://hackaday.com/2009/07/15/avr-isp-programming-via-arduino/>

![ardunio avr isp programming](img/b5b4f1b1708eee57f7d4940a0dab8478.png "ardunio avr isp programming")

我们发现这个 [Arduino AVR ISP 程序员](http://www.flickr.com/photos/drug123/3718355976/in/pool-76206823@N00)特别有意思。AVR 微控制器可以利用一种称为系统内编程的接口。ISP 允许芯片在实际电路中通过引脚头进行编程或重新编程。Atmel 的解决方案是 T2 的 AVR ISP MKII 编程工具 T3。MKII 也可以像 AVR 一样重新编程。这里的区别是，大多数人不太可能修改 MKII 来用作除了程序员之外的任何东西。另一方面，如果你已经有了 Arduino，[获取 avr.isp.03 固件](http://code.google.com/p/mega-isp/)和 AVRdude。然后使用 Ardunio 作为编程器对设备进行编程，例如 ATtiny13 上的[。所有项目信息都是在 CC BY-NC-SA 3.0 许可下提供的。在相关说明中，我们介绍了一份](http://www.flickr.com/photos/drug123/3718360064/)[微控制器备忘单](http://hackaday.com/2009/06/18/microcontroller-cheat-sheet/)，其中涵盖了 AVR 器件和 ISP 引脚排列。
# 使用 AT90USBKey

> 原文：<https://hackaday.com/2010/06/23/working-with-the-at90usbkey/>

![](img/747de69d34ed9f61b79392e92efdde29.png "at-90-usb-key")

Genearic HID 工具是一种创建你自己的人机界面设备的简单方法。这个项目的额外好处是向我们展示了如何[黑 AT90USBKey 开发板](http://generichid.sourceforge.net/hardware.htm)上的硬件。这款基于 AVR 的设备，我们看到它曾被用来使[成为 SNES 盒式磁带阅读器](http://hackaday.com/2009/06/19/usb-reader-for-snes-game-carts/)，售价略高于 30 美元，但有一些说明。首先，引脚的转接焊盘间距不是 0.1 英寸，需要一些创造性的焊接才能轻松实现。但是，演练还包括转换电路板，使其在 USB 主机模式下以 5v 电压运行，以及改变填充的元件，以回收 AT90USB1287 芯片上的引脚。乐趣不仅限于这款主板，还有基于同一芯片的自制替代产品[。](http://www.franksworkshop.com.au/CNC/GenericHIDBoard1.0/GenericHIDBoard1.0.htm)

[谢谢胡安]
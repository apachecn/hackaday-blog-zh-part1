# AVR ATtiny25 USB 点击计数器

> 原文：<https://hackaday.com/2008/10/05/avr-attiny25-usb-hit-counter/>

![](img/b515e0883905e6ba2b081d5cad327e96.png "usb-physical-hit-counter-11")

[鲍勃]有一个 [USB 页面点击计数器](http://www.bobhobby.com/2008/04/22/usb-physical-hit-counter-based-on-avr-attiny25/)，它使用 ATtiny25 运行一个 [MAX7219](http://www.maxim-ic.com/quick_view2.cfm/qv_pk/1339) ，后者驱动八个 7 段显示器。在 AVR 上使用固件实现 [USB 很容易，不需要任何 USB 到 RS232 的转换。主机软件是用 Delphi 编写的，位于 Windows 托盘中。代码示例看起来足够简单，可以扩展到您自己的显示程序中。](http://www.obdev.at/products/avrusb/index.html)
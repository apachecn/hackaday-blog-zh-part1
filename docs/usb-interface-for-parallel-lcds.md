# 并行液晶显示器的 USB 接口

> 原文：<https://hackaday.com/2006/02/02/usb-interface-for-parallel-lcds/>

![](img/25ef89a7c562616ed20b395324e9cee2.png "usblcdtop")

Pontus fr nder 为任何使用 HD44780 控制器的 LCD 组装了一个非常简单的 [USB 接口。他使用 FTDI 的 USB 芯片在主机上创建一个虚拟的 COM 端口。这与控制 LCD 的 Atmel ATtiny2313 相连。AVR 有两个 PWM 输出，用于控制背光和对比度。如果背光的电流足够低，它可以直接从 USB 驱动，因为它看起来像一个标准的串行显示器，你可以使用像](http://www.e.kth.se/%7Epontusf/usb2lcd.html) [LCD Smartie](http://lcdsmartie.sourceforge.net/) 这样的程序与它交谈。

*   [永久链接](http://www.e.kth.se/~pontusf/usb2lcd.html)
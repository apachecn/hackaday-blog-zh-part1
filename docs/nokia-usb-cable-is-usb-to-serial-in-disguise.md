# 诺基亚 USB 线是 USB 转串口的伪装

> 原文：<https://hackaday.com/2010/02/25/nokia-usb-cable-is-usb-to-serial-in-disguise/>

![](img/a4e5b6e6b7eb9283b9ac0a99d38cd16f.png "usb-ftdi-hack")

[Jethomson]想出了一个办法，在 USB 转串行线处[使用诺基亚 USB 线。他能够以不到 3 美元的价格买到这些电缆中的一根。经过一点探索，他找到了合适信号的导体，并由此开发出一种方法，用分压器保护 3.3v 信号电平。](http://jethomson.wordpress.com/2010/02/21/diy-usb-to-serial-cable-for-3usd/)

看到[Will O'Brien 的]关于诺基亚手机串行通信的帖子，这并不奇怪。在那篇文章中，我们了解到诺基亚的电话使用 TTL 通信。一旦你完成了[Jethomson]对线缆的修改，你就可以按照他的例子将它与 Arduino 结合使用。
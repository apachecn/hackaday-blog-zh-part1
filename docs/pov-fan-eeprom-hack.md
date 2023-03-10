# POV 风扇 EEPROM 黑客

> 原文：<https://hackaday.com/2009/10/09/pov-fan-eeprom-hack/>

![pov_fan_eeprom_hacking](img/7bd8ae2a986537274aeb41620500a896.png "pov_fan_eeprom_hacking")

用口香糖进行黑客攻击得到了一个持续视觉显示的粉丝，这是今年 [Blackhat](http://hackaday.com/2009/07/29/black-hat-2009-breaking-ssl-with-null-characters/) 上 [Cenzic](http://www.cenzic.com/) 分发的。这不是我们见过的[最大的粉丝视角显示器](http://hackaday.com/2009/07/22/ceiling-fan-pov/)，但它仍然是一个可以摆弄的有趣设备。他们[侵入设备](http://hackingwithgum.com/2009/10/06/hacking-the-cenzic-pov-fan/)上的 EEPROM，以改变风扇显示的信息。

这与我们最近[看到的另一个](http://hackaday.com/2009/09/24/steal-the-administrator-password-from-an-eeprom/) [EEPROM 读/写](http://hackaday.com/2009/09/25/eee-pc-bios-resurrection/)非常相似。Gum 黑客从 EEPROM 中读取数据，然后拆开它，以发现信息数据是如何存储在芯片上的。通过注意风扇运行时显示的消息，这变得更加容易。数据的第一个字节显示消息中的字数，然后每个字数据块前面有一个字节，代表该作品中的字母数。数据长度是根据每个显示字符的像素数计算的。一旦他知道了数据存储方案，就只需要用同样的方式格式化他自己的信息并覆盖芯片。

如果你正在寻找关于对未知硬件系统进行逆向工程的初级读本，这是一篇很好的文章。如果你对尝试我们的[条形码](http://hackaday.com/2009/10/07/barcode-challenge/) [挑战](http://hackaday.com/2009/10/08/barcode-challenge-part-2/)很感兴趣，也许从一个简单的设备上破译 EEPROM 数据应该是你的下一个任务。

[谢谢詹姆斯]
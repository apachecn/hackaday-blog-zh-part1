# 侵入密码保护的硬盘

> 原文：<https://hackaday.com/2010/08/26/hacking-a-code-protected-hard-disk/>

![](img/03279768246ebbf793a210e4771bde7b.png "istorage-diskgenie-hacking")

我们的朋友[Sprite_TM]带着[去看看一个代码保护硬盘](http://spritesmods.com/?art=diskgenie)的安全性。 [iStorage diskGenie](http://www.istorage-uk.com/diskgenie_over.php) 是一个加密的 USB 硬盘，有一个用于输入密码的键盘。打开后，他发现处理键盘的芯片是 PIC 16F883 微控制器。他戳戳内部，发现了一些有趣的东西。例如，有一个板载 LED，根据输入的代码闪烁不同；一路用于正确的代码，另一路用于正确位数的错误代码，第三路用于位数错误的错误代码。这个信号可以被修补成暴力攻击，但有一个更快的方法。微控制器一次一位地检查正确的代码。因此，通过测量芯片的响应时间，攻击者可以确定前导数字何时是正确的，并减少破解代码所需的时间。有一种暴力保护可以监视多个不正确的密码，但是[Sprite_TM]甚至找到了一种方法来绕过它。他附加了一个 AVR 芯片来监控 PIC 响应时间。如果输入正确密码的时间过长，AVR 会在将错误的尝试数据写入 EEPROM 之前复位 PIC。这可能是一个缓慢的过程，但他认为应该可行。我们很开心[看着闪光毁灭者](http://hackaday.com/2010/06/14/update-flash_destroyer-final-destroys-eeprom/)锤打，我们希望看到一个设置工作从这个设备获取代码。
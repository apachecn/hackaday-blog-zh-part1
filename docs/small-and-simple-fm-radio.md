# 小巧简单的调频收音机

> 原文：<https://hackaday.com/2010/09/21/small-and-simple-fm-radio/>

[gpsKlaus] [基于 AR1010 IC 建造了这个小小的调频收音机](http://comwebnet.weimars.net/forum/showthread.php?tid=487&amp;pid=3246#pid3246) ( [翻译](http://translate.google.com/translate?hl=en&sl=de&tl=en&u=http://comwebnet.weimars.net/forum/showthread.php%3Ftid%3D487%26amp;pid%3D3246%23pid3246))。该芯片由 ATtiny45 微控制器通过 I2C 控制。他的调谐实现依赖于在固件中预设 16 个电台，并用白色电位计选择它们。

FM 芯片来自 SparkFun 的分线板。还不错，大约 15 美元，因为它包括晶体，一些帽子和几个电阻，你不必尝试和焊接到那个微小的封装上的细间距焊盘。我们有点不确定该器件包含的功能，因为数据表缺乏细节，并且[spark fun 在描述中包含的参考数据表](http://www.sparkfun.com/datasheets/Wireless/General/TEA5767.pdf)显然是针对功能更加全面的芯片。不过，如果你已经厌倦了闪烁的 led 灯，这将是一件有趣的事情。

如果你不想让集成电路做所有繁重的工作[,试试这篇文章](http://hackaday.com/2010/07/25/hackaday-links-july-25-2010/),看看如何构建你自己的收音机调谐器。
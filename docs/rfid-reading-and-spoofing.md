# RFID 读取和欺骗

> 原文：<https://hackaday.com/2011/11/10/rfid-reading-and-spoofing/>

![](img/e657bbb2c5b7bc2008ad30759163495c.png "RFID")

锁总是暂时的障碍。在决定打开他部门的 RFID 安全锁后，[Tixlegeek]建造了一个设备来[读取和欺骗 RFID 标签](http://www.tixlegeek.com/?2011/11/06/332-details-de-mon-rfid-spoofer-home-made-fraude-frauduleux-acces-tag-rf-badge)(法语，谷歌翻译[这里](http://translate.google.com/translate?sl=fr&tl=en&js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&u=http%3A%2F%2Fwww.tixlegeek.com%2F%3F2011%2F11%2F06%2F332-details-de-mon-rfid-spoofer-home-made-fraude-frauduleux-acces-tag-rf-badge&act=url))。

该系统以 ATMega32 微控制器为核心，配有 16×2 LCD 显示屏。一个商业 RFID 阅读器模块负责所有的嗅探/克隆任务，一个小的调制电路负责将这些位泵送到一个锁。目前，欺骗者只能读取和欺骗 125kHz 的 RFID 标签，没有加密或授权。比[胶带 RFID 标签](http://hackaday.com/2011/05/20/using-an-avr-as-an-rfid-tag/)更复杂的标签不起作用。

[Tixlegeek]的小项目确实开辟了一些有趣的途径来探索那些最肯定是非法的东西。该项目的一个较小版本可以放置在门或其他 RFID 阅读器附近，以 125 千赫的频率用 32+62 位密码开锁。它不会是业内最快的保险箱窃贼，但只要有电，它就会自动工作。

如果你对[Tixlegeek]的 RFID 欺骗器有任何想法，请在评论中留言。
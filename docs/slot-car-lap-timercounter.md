# 老虎机圈计时器/计数器

> 原文：<https://hackaday.com/2011/06/17/slot-car-lap-timercounter/>

![](img/a1a87b2845463c11cc6e2f8eb2d8a1e6.png "Detail")

在他的第一个项目中，使用 TI Launchpad [VOJT4]为老虎机建造了一个圈计时器和计数器。对我们来说，想出建造什么的主意总是最难的，我们认为他在这里找到了一个很棒的主意。

每当赛车通过赛道的终点线时，它就会触动一个簧片开关，这个开关被热粘在赛道段的下面。两个簧片开关都有一个电容来平滑输入(这是作为硬件去抖吗？).然后，MSP430G2553 将时间和圈数推送到图形 LCD 上。

您必须登录到[VOJT4]发布该项目的论坛才能看到图片。正因为如此，我们在休息后嵌入了它们(包括原理图)和一个演示视频。但是一定要看看他的项目线程，听听他的想法，仔细阅读他写的代码。

[https://www.youtube.com/embed/Fwz0Ui2cySw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Fwz0Ui2cySw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)[![](img/3016db7698fc85e034e344c5cbc67c89.png)](https://hackaday.com/wp-content/uploads/2011/06/detail-e1308347284696.jpg)[![](img/601f64fbca66fb70f0b1b5a23ee1bbf7.png)](https://hackaday.com/wp-content/uploads/2011/06/schema.png)[![](img/b2182fed72b3a38fb49e447b0ee463f0.png)](https://hackaday.com/wp-content/uploads/2011/06/sensors.jpg)[![](img/f57684c186f3205d006f4fb89e4353bd.png)](https://hackaday.com/wp-content/uploads/2011/06/testtrack.jpg)

[通过 [43oh](http://www.43oh.com/2011/06/count-slot-car-lap-times-with-the-launchpad/) 感谢操作码]
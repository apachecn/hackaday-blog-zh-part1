# 简单的 MP3 播放器

> 原文：<https://hackaday.com/2005/11/14/simple-mp3-player/>

![mp3](img/3bd06cc8cdce374b312892084786f067.png)

我见过很多 MP3 播放器项目，但这肯定是迄今为止最简单的设计之一。控制来自一个 PIC16LF877。文件按照复制的顺序从闪存卡的根目录中读取。该数据通过内置 DAC 逐字节流入 vs1001k 解码器芯片。

如果这个项目看起来有点难，你可能想看看拉斐尔的其他项目:[现在的短闹钟](http://www.walrus.com/%7Eraphael/clock_short_now/clocknow.htm)【通过[制造](http://www.makezine.com/blog/archive/2005/11/how_to_alarm_clock_of_the_shor.html)。它是为像我这样睡眠时间不规律的人设计的。

[谢谢 iamdigitalman]

*   [永久链接](http://www.walrus.com/~raphael/html/mp3.html)
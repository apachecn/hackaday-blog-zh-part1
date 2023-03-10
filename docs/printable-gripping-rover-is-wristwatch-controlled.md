# 可印刷的抓握漫游车由手表控制

> 原文：<https://hackaday.com/2011/03/29/printable-gripping-rover-is-wristwatch-controlled/>

![](img/2980faab83d2fe7de2c84577740b810a.png "SAMSUNG")

[Lars Kristian Roland]正在用手表控制这辆漫游车。机器人本身是一个实用的建筑，有一个基于【Thingiverse 项目的抓手。正如你在休息后的视频中看到的，它基于来自 [TI ez430 Chronos 腕表](http://hackaday.com/2009/11/25/ti-sports-watch-for-hacking/)的加速度计数据进行变速控制。

手表通过 CC1110 开发板无线连接到机器人，开发板通过串行连接将通信中继到板上的 Arduino。看起来使用这种设置进行缓慢而精确的移动有点麻烦，但这可能会通过调整如何解释加速度计值来改变(使用非线性方程将允许您在低速时进行更多控制，而不会牺牲电机的最高速度)。

因为它使用与 IM-ME 相同的 RF 硬件，我们不禁想知道 CC1110 开发板是否可以换成一个未使用的 [IM-ME 加密狗](http://hackaday.com/2010/10/23/im-me-usb-dongle-hacking/)？

[https://www.youtube.com/embed/WhE8F9rWmAg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WhE8F9rWmAg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢雨果]
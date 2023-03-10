# 采用 MSP430 芯片的复合视频

> 原文：<https://hackaday.com/2010/12/04/composite-video-with-msp430-chip/>

![](img/9901154b5bdf9ff501e56af96ca30034.png "msp430-composite-video")

[NatureTM]利用感恩节假期的部分时间[用 MSP430](http://naturetm.com/?p=47) 微控制器获得复合视频输出。他使用的是 TI Launchpad 附带的一种芯片，这是一个很大的硬件限制，因为代码内存和 RAM 相对较小。该芯片以 192×40 像素的分辨率显示一幅静止图像。尽管如此，这仍然是了解复合视频信号的一个很好的方式，因为许多其他项目[使用 TVout 库来省去你的麻烦](http://hackaday.com/2010/10/24/hackvision-is-build-your-own-retro-game/)。你只需要一个 TI 发射台、一个 16 MHz 晶体振荡器、两个电阻和一个 RCA 插孔。深入研究代码，看看[NatureTM]在尽可能多地将工作转移到芯片外设上做得有多好。
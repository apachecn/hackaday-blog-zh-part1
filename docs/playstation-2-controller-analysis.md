# Playstation 2 控制器分析

> 原文：<https://hackaday.com/2008/06/19/playstation-2-controller-analysis/>

不久的将来实验室的人们正试图用一个微控制器[模仿 Playstation 2 控制器](http://www.nearfuturelaboratory.com/2008/06/19/playstation2-logic-analysis/)的行为。他们用这里找到的[控制器信息](http://www.gamesx.com/controldata/psxcont/psxcont.htm)写了一些初始代码，但是决定弄清楚发生了什么的最好方法是探测接口。他们使用的是一个[逻辑端口](http://www.pctestinstruments.com/)，它有 34 个通道和两个时钟通道。它们只需要六个通道，因为 PS2 实现了一个 SPI 协议和一条 ACK 线路。这篇文章只是一个初步的调查，但是会让你对 Logicport 是如何工作的有一点了解，以及为什么你会觉得它有用。

*   [永久链接](http://www.nearfuturelaboratory.com/2008/06/19/playstation2-logic-analysis/)
# 巴塞尔艺术展上的群光

> 原文：<https://hackaday.com/2010/06/20/swarm-light-at-art-basel/>

![](img/dc6de646d71de6ac8729e01cbe41d464.png "Swarm-Light")

什么东西有 9000 个发光二极管、3000 个 MSP430 处理器、6 个 XMOS XC-2 以太网模块，并且闪烁不停？这是 [Swarm Light](http://petrinis.se/blog/swarm-light/) ，一个在今年[巴塞尔艺术展](http://www.artbasel.com/go/id/ss/lang/eng/)上展示的艺术装置。[Fredrik Petrini]负责构建由三个 3D 立方体 LED 光模块组成的小组的硬件。与我们看到的许多艺术作品不同，他分享了这件作品的设计细节。在上图中，你可以看出每个立方体包含几个 LED 模块棒。每个杆都是三个轨道，除了作为物理结构之外，还提供电源、接地和串行数据。每个模块上有三个 led，由一个 MSP430 处理器控制。每个 XMOS 单元控制一个立方体中的一半棒，通过以太网连接从运行. NET framework 程序的 PC 获取指令。如果说这只是升级版的 [LED 立方体](http://hackaday.com/2008/06/20/3x3x3-led-cube/)，那是一种保守的说法。休息之后，看看正在进行的展览。它使用一种算法来分析音乐，从房间的环境声音中获取输入，以控制灯光波动。

[https://player.vimeo.com/video/12525044](https://player.vimeo.com/video/12525044)

[谢谢保罗]
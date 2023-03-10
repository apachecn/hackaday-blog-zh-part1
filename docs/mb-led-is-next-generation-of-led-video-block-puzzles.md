# MB LED 是下一代 LED 视频块拼图

> 原文：<https://hackaday.com/2011/07/06/mb-led-is-next-generation-of-led-video-block-puzzles/>

![](img/cce4eb2eb183cdc4c48838631dbdf26a.png "mb-led-video-led-puzzle")

[认识一下 MBLed](http://mbled.wordpress.com/) ，一组互动的 8×8 LED 瓷砖。把它们放在一起，它们会把自己定位到一个视频屏幕上，这个屏幕就是这些部分的总和。如果这听起来很熟悉，那是因为我们以前在[GLiP 项目](http://hackaday.com/2010/07/02/great-interactive-led-puzzle/)中见过这个概念。[Guillaume]告诉我们，MB Led 是 GLiP 的新版本，从我们看到的情况来看，他们已经取得了很大的进步。

硬件设计得很好。一个 PCB 承载 STM32 微控制器和一对接收 RGB LED 矩阵模块的引脚接头。一对 AA 电池支架构成了该设备的腿。每个都在四个边缘上有红外接收器/发射器对，并且不断地轮询它的邻居。

真正让我们印象深刻的是他们用于通信的算法。FreeRTOS 在 ARM 处理器上运行，并开发了一系列消息，允许块选举一个领导者，并通过分布式系统遵循其命令。在上面链接的页面上查看更多关于这些算法的信息，休息后加入我们观看演示视频。

[https://www.youtube.com/embed/dxhkEBGJZMA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dxhkEBGJZMA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
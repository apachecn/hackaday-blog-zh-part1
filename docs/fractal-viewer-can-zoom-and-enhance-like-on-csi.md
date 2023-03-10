# 分形浏览器可以像 CSI 一样缩放和增强

> 原文：<https://hackaday.com/2012/01/31/fractal-viewer-can-zoom-and-enhance-like-on-csi/>

![](img/6abec102195501f87f81640f2483b286.png "Mandelbrot_400x300")

这个分形浏览器是一个很好的方式让你的脚湿了现场可编程门阵列。这个项目会给你一些视频输出、用户输入和一大堆数学和内存管理的经验。[仓鼠]使用 Papilio Plus 板构建，该板承载 Spartan 6 FPGA。这延续了他在硬件设计领域的冒险历程；[我们在 12 月](http://hackaday.com/2011/12/30/so-you-wanna-learn-fpgas/)看到了其中的一部分。

开发板的 arcade Megawing 使他可以轻松地使用滚动和缩放分形设计所需的控件。产生形状的计算以 240 MHz 运行，VGA 输出以 80 MHz 运行。该器件具有足够的马力和 SRAM 来显示 800×600 像素的输出，刷新率为 60 Hz。

我们真的很喜欢[仓鼠]在计划如何处理计算时绘制的逻辑图。这并不太复杂，但是我们花了一些时间来概念化所有的东西是如何组合在一起的。与他上次的尝试相比，这无疑是一个进步，因为我们无法理解那张流程图。

如果你只是对漂亮的形状和颜色感兴趣，休息后会有一个演示。

[https://www.youtube.com/embed/dR4jbX332jU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dR4jbX332jU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
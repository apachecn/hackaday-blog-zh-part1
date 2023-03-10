# 10 美元的摄像头模块，适合您的下一个 FPGA 项目

> 原文：<https://hackaday.com/2012/03/07/10-camera-module-for-your-next-fpga-project/>

![](img/72895e99d529f573634fb833600035e8.png "ov7670-camera-on-fpga-board")

这里是[Voelker]展示他的基于 FPGA 的摄像头硬件。他在易贝花了大约 10 美元买了一台 ov7670 相机，然后开始提取像素并处理图像。他现在能够每秒抓取 30 帧，并将其推送到自己的 Java 显示应用程序中。他用的是凤蝶板，如果你想自己尝试一下，你也许可以[为这个单元搞到一个免费的分线板](http://www.gadgetfactory.net/2012/03/10-vga-camera-on-the-papilio-one-how-about-a-free-pcb-to-try-it-yourself/) (wing)。

[沃克尔的]方法是抓取每一帧，并准备好快速串行传输。输入帧的分辨率为 640×480。他将其缩小到 80×60，并以 3 兆波特传输。使用的硬件资源实际上是相当轻量级的。他编写了自己的传输和照片处理模块，使用很少的 RAM 进行缩减，并使用一个 128 字节的缓冲区进行数据传输。听起来好像他计划使用相机来查看和检测一条线，以创建自己的循线机器人。

想知道以前在哪里见过 ov7670 模块吗？这是 TRAKR 机器人上使用的部件[。](http://hackaday.com/2010/08/30/spy-video-trakr-the-teardown/)
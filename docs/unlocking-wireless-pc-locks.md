# 解锁无线电脑锁

> 原文：<https://hackaday.com/2011/07/27/unlocking-wireless-pc-locks/>

![](img/c389994fd5a06c32fa0b868b186b4a9e.png "blog-USBRemote-arrows")

Pantz 先生]给我们指了一个我们认为你会感兴趣的网页。它使用一个通用软件无线电外设(USRP)处理[黑客 PC 锁。](http://intrepidusgroup.com/insight/2011/07/usrp-101-unlocking-wireless-pc-locks-and-freeing-dolphins/)当你不在的时候，遵循注销或锁定你的工作站的好习惯，让用户真正做到这一点是非常困难的。这些小工具是一个 2 件设置一个是 usb 加密狗，另一个是一个徽章一样的设备。如果徽章关闭或距离超过 30 英尺，信号将丢失，电脑将被锁定。

从那以后，你真正需要做的就是弄清楚 2 在什么频率下运行，什么代码在空中飞行。一些仔细的目测表明，它在 434MHz 区域工作，很像你的汽车的遥控加密狗，一旦设备被拆开，对板上 2 个 IC 的一些研究证实了这一点。使用 [GNU Radio](http://gnuradio.org/) 频谱分析仪，可以快速捕获、转储信号，并创建一个脚本将信号发送出去，前提是您有正确的硬件来执行此操作。
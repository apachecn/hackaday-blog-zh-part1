# 不要相信你的硬件

> 原文：<https://hackaday.com/2005/11/09/dont-trust-your-hardware/>

![flash drive](img/971c71cdc0adadf5090c5c88971275b8.png)

我没能在 Toorcon 上看到 David Maynor 的“你就是特洛伊”( [pdf](http://toorcon.org/2005/slides/dmaynor-youarethetrojan.pdf) )演讲，但这确实是一个有趣的主题。人们如此重视通过防火墙和 IDS 系统加强外围安全，攻击是如何通过的呢？用户:将笔记本电脑带到现场，通过 VPN 连接家庭系统，或者为了速度而牺牲安全性。

外围设备也可能是一个主要威胁。USB 和其他计算机组件使用直接内存访问(DMA)来绕过处理器。这允许高性能的数据传输。CPU 完全不知道 DMA 活动。这种情况需要很多信任。这是如何被利用的:像一个勤奋的人一样，你锁定了你的 Windows 会话。有人拿着被黑的 USB 钥匙走进来，把它插到你的电脑里。USB key 使用其 DMA 来终止锁定您的会话的进程。瞧啊。你的终端现在是完全开放的，他们所要做的就是插入他们的 USB 钥匙，PSP，iPod
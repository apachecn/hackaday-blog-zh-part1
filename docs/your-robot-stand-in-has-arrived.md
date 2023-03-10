# 你的机器人替身已经到了

> 原文：<https://hackaday.com/2011/03/28/your-robot-stand-in-has-arrived/>

![](img/5c71fe9c62ea2459c27ca1ef6b074239.png "balancing-telepresence")

通过摆反转来认识 TIPI，即[遥现接口。TIPI 是一种代理，通过平衡六英尺框架顶部的 LCD 屏幕和摄像头，为远程工作者提供物理存在。用户可以完全控制机器人的移动，他们自己的摄像头图像显示在显示器上，这样其他与机器人互动的人就可以与他们交谈。](http://patfairbank.com/tipi/)

一对 12.5 英寸的车轮通过一个传动比为 37:1 的齿轮箱与 DC 汽车公司相连。这些规格是从突然的 20 度失去平衡中恢复所必需的，对于这种身材的机器人来说相当令人印象深刻。一个猩猩 SVP 板监控一个双轴加速度计和一个陀螺仪，以获得精确的定位数据。这个板自动保持平衡，同时从第二个控制器，一个比格犬板接收用户命令。Beagle 板处理通信，包括发送和接收视频信号，以及向猩猩传递传入的位置控制数据。将两个系统分开，确保可能面临速度变慢或锁定的硬件与负责平衡的硬件在物理上分开，从而防止屏幕破碎。

检查刹车后的视频剪辑，看看一些平衡的好处。以比一些商业版本所享受的[$ 15，000 的价格标签低得多的价格来构建你自己的版本并不困难。](http://hackaday.com/2010/05/24/bamf2010-qb-goes-to-meetings-shoots-lasers-from-eyes/)

[https://www.youtube.com/embed/PmhrrKtjYDs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PmhrrKtjYDs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
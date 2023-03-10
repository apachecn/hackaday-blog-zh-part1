# 台式激光雕刻机也做一些切割

> 原文：<https://hackaday.com/2011/03/11/bench-top-laser-engraver-does-some-cutting-too/>

![](img/02360d2a6c0c1ce83b836d00be730f1c.png "Pocket-laser-engraver")

拿起你放在角落里的那堆旧光驱，[开始制作这台激光雕刻机](http://www.instructables.com/id/Pocket-laser-engraver)。[Groover]正在采取一种严肃的方式来构建，我们认为它足够简单，可以被非常广泛的受众所接受。

物理组件使用两个光驱中的底座。这些都安装在一些角撑架上。由于激光切割在一个特定的焦距，不需要 Z 轴(大大简化了建设)。事实上，我们认为组装中最难的部分是从 DVD-R 驱动器中取出激光二极管，并将其包装起来用于该设置。

电子产品是一些消费产品的组合。两个预制电机驱动器用于控制光学底座上的步进电机。它们从 Arduino 接收命令。一个名为 [GRBL](http://dank.bengler.no/-/page/show/5470_grbl?ref=mst) 的包读入 g 代码(【Groover】展示了如何从 Inkscape 生成 g 代码)，并依次向 Arduino 发送命令。

结果相当显著。它可以雕刻木头，分辨率和对比度都很高。收支平衡后的视频显示它从建筑用纸中剪出形状。现在我们仍然想要我们自己的[全尺寸激光切割机](http://hackaday.com/2010/01/27/building-a-bigger-better-laser-engraver/)，但是这个项目对我们来说在财政上更有可能。

[https://www.youtube.com/embed/BLAEMLuRJSo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BLAEMLuRJSo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
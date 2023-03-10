# 用这台 BS 吃角子老虎机跳过拉斯维加斯

> 原文：<https://hackaday.com/2009/10/01/skip-vegas-with-this-bs-slot-machine/>

![bs2_slot_machine_DisplayInterface](img/d35f19953a31c2a13a05c50f48394f64.png "bs2_slot_machine_DisplayInterface")

我们在 YouTube 上瞥见了这个[基本 Stamp 2 控制的电子老虎机](http://www.youtube.com/watch?v=q3BAeWJwGdE)。我们非常感谢[Mike Donahue]愿意与我们分享他的项目。

他使用触觉开关，而不是将硬币投入投币口，杠杆式开关启动独臂强盗。这个动作显示在一个 1.5 英寸的有机发光二极管-128-G1 屏幕上，这个屏幕有自己的控制器(这解释了为什么它在相对较慢的 BS2 上运行得如此之好)。对于现实主义来说，压电扬声器提供了一些非常好的声音效果。休息之后，我们将看看代码、图形和一些视频。

![Slot Game_scaled](img/774d40950a6d7ac1c303d29a2ab1a923.png "Slot Game_scaled")

连接非常简单，而且[Mike]已经在基本的 Stamp 2 作业板上建立了项目。显示器通过两条串行线和一个复位引脚寻址。

他使用 MSpaint 生成图形，创建了三个几乎不变的全屏图像。旋转转盘的图标要小得多，并覆盖在较大图像的顶部。这些图标中的三个在内存中相邻存储。这样，指针可以前进，下一个图像将开始滚动，就像一个旋转的圆柱体。如果你需要的话，这里有略大的原理图和图片。

这是一个有趣的玩具，而且做得很好。如果你有兴趣看看引擎盖下的东西，[这里有一份源代码的副本](http://blog.mahalo.com/hackaday/misc/oLED_Slot_1.1.zip)。

[https://www.youtube.com/embed/q3BAeWJwGdE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q3BAeWJwGdE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
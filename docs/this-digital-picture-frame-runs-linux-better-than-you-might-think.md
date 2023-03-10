# 这个数码相框运行 Linux 比你想象的要好

> 原文：<https://hackaday.com/2012/01/10/this-digital-picture-frame-runs-linux-better-than-you-might-think/>

![](img/8d0d921d684ce3641eba705985597a69.png "parrot-df3120-running-linux")

啊，在你的工作台上散布一些可破解硬件的好处。这恰好是来自 Parrot DF3120 数码相框的电路板和液晶屏。考虑到你仍然可以以 25 美元左右的价格买到这款设备，它的功能相当强大。你将获得 3.5 英寸屏幕、8MB 或 RAM 的 ARM9 处理器、蓝牙、倾斜传感器等。似乎[BusError]、[Sprite_tm]、[Claude]和其他一些人真的去了镇上，并且[泄露了这个设备必须提供的所有秘密](https://sites.google.com/site/repurposelinux/df3120)。

他们的黑客目标是运行他们自己的 Linux 内核。可以使用 JTAG 接口对处理器进行重新编程。如果你真的想深入了解有用的东西，借助微通孔网格，你可以访问电路板底部的所有 BGA 引脚。但是，只要修改一个升级镜像，就可以欺骗设备刷新你自己的固件。

你可以得到一个很好的主意，一旦你在休息后更换了视频中的固件。RAM 升级(使用旧 PC133 棒的芯片)让视频流畅运行，因为它是通过 Wii 遥控器控制的。

[https://www.youtube.com/embed/cwN6eztHQSA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cwN6eztHQSA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[34 分钟后谢谢]
# 使用 NES 控制器在 IBM XT 上玩游戏

> 原文：<https://hackaday.com/2010/12/24/gaming-on-an-ibm-xt-using-an-nes-controller/>

![](img/438a159c21b45e45734558898d152537.png "Exif_JPEG_PICTURE")

[Frode]觉得在他的旧 IBM XT 电脑上用键盘玩游戏实在是太吵了。他想出了一个更安静的游戏方式，为原来的 NES 控制器制作了一个 XT 适配器。如果您还没有研究过 NES 外设使用的通信协议，这是一个很好的学习方法。在里面你会发现一个 CMOS 移位寄存器，当它接收到一个锁存信号时，可以捕捉按钮的状态。考虑到这一点，[Frode]设计了一种电路来收集控制器的位，并使用 XT 键盘协议生成输入命令，而不使用微控制器。所有这些在休息后的演示中都有解释。

我们看到的大多数 NES 控制器黑客[会永久改变硬件](http://hackaday.com/2010/06/30/nes-controller-to-usb-gamepad/)。很高兴看到一个不用打开就能用的。

[https://www.youtube.com/embed/wfOzZSU_dO8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wfOzZSU_dO8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
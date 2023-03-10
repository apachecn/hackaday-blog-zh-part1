# AVR 俄罗斯方块

> 原文：<https://hackaday.com/2010/01/14/avr-tetris/>

![](img/155ea0cdbb36c2cba7644c37d694b1c0.png "avr-tetris")

俄罗斯方块，永恒的经典，是那些有人试图在每一个可以想象的硬件平台上运行的概念之一。我接受了挑战，用手头的硬件从头开始编写俄罗斯方块的克隆版本。构建的核心是 ATmega168 微控制器。游戏显示在 KS0108 128×64 LCD 模块上，带有五个瞬时按钮开关，提供方向、旋转和输入控制。您可以看到中断后嵌入的最终单色动作。

在写游戏代码的时候，我心中有几个目标。我希望代码是可移植的，以便电路板的大小和所用屏幕的类型可以很容易地改变。考虑到这一点，我开发了用于诺基亚 3595 手机屏幕的主干和用于图形 LCD 的平行分支[。最初我使用的是 ATmega8，但经过升级后，我可以在手机屏幕所需的 3.3v 电压下工作。](http://code.google.com/p/tetrapuzz/source/browse/#svn/branches/GLCD)

图形 LCD 分支的固件编译为 6 kB 多一点，这意味着它仍然可以在 mega8 上运行。此外，ATmega168 与 Arduino Duemilanove 中使用的处理器相同，因此另一个[俄罗斯方块端口](http://hackaday.com/2007/01/03/pin-terminal-tetris/)也不是不可能的。我刚刚得到了我的第一个 Arduino，所以我们将看看我是否有时间在代码中开始一个新的分支。

[https://www.youtube.com/embed/ELX09og_2x0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ELX09og_2x0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
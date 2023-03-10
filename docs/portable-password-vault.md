# 便携式密码保险库

> 原文：<https://hackaday.com/2010/09/26/portable-password-vault/>

![](img/e5fe74b834e12bdfaf5e8d5d7865bfac.png "SANYO DIGITAL CAMERA")

这个小盒子会记住你所有的用户名和密码。在里面你会发现一个 Atmel AT89S5131 微控制器，它具有内置 USB 功能。当盒子插入 USB 端口时，它被识别为键盘。操作顶部和侧面的按钮将选择和打印出各种存储的用户名和密码。密码由随机种子在芯片上生成，作为一项安全功能，设备本身需要在通电后输入密码。

[SigFLUP 的]包括一个非常漂亮的配置算法。它不依赖于终端连接，因为该设备是一个键盘，您可以在编辑器窗口中与它通信(这应该使它独立于平台)。没有可用的代码，但休息后尝试根据演示中概述的规范编写自己的代码将成为一个有趣的周末项目。

[https://www.youtube.com/embed/BD3F3iBIl7c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BD3F3iBIl7c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

(我们差一点就可以看到帖子的结尾，没有说“ [Setec 天文学](http://en.wikipedia.org/wiki/Sneakers_(film))”)
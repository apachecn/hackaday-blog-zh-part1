# 使用调试模式的 Propeller-Android 通信

> 原文：<https://hackaday.com/2011/03/29/propeller-android-communications-using-debug-mode/>

![](img/b9ebf2a6bb029ab8c55a78d63c6d0cac.png "android-propeller-bridge")

这是一种连接 Android 手机和 Propeller 微控制器的新方法。它被称为[prop bridge](http://robots-everywhere.com/re_wiki/index.php?title=PropBridge)，使用一个非常简单的电路，带有一个稳压器、几个晶体管和几个电阻。这种方法的诀窍在于创造性地使用 Android 硬件上已经存在的软件功能，即 [Android 调试桥(ADB)](http://developer.android.com/guide/developing/tools/adb.html) 。ADB 的加入是出于开发的考虑，但由于它对这些设备的某些部分提供底层控制，所以它只是等待被纳入黑客攻击。

Propeller 本身使用固件使 Android 认为它是两个不同的外部连接硬件设备之一。它可以像运行 ADB 客户端的 PC 一样运行，也可以模仿 TCP 连接。uC 上仍然有足够的空间来添加您自己的固件，并且大多数 I/O 引脚对于基本连接都是不需要的。休息之后，请观看视频，快速了解该系统。

如果你在自己的项目中使用 Android 之前需要一些 Android 编程方面的帮助，请查看我们的 Android 开发系列。

[https://www.youtube.com/embed/QcR0ZG_7YC8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QcR0ZG_7YC8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
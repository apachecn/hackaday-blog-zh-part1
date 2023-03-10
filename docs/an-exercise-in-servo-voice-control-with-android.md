# Android 下的伺服语音控制练习

> 原文：<https://hackaday.com/2011/11/20/an-exercise-in-servo-voice-control-with-android/>

![voice-controlled-android-lock](img/d110a508341185d4261daf4b1878d9d1.png "voice-controlled-android-lock")

[Shazin]有一些空闲时间，所以他决定做一些他一直想做的事情——学习 Android 编程。他走了一条间接的路线，最终使用了 Android 的脚本层(SL4A ),这让他在这个过程中领先一步。SL4A 介于 Android API 和 Python 等脚本语言之间，允许他将自己已经熟悉的东西应用到 Android 环境中。

他认为尝试建立一个依靠声音命令来上锁和开锁的门禁系统会很酷。使用 Android 的 Google Voice API 和 Arduino，他构建了一个小的 Python 应用程序，允许他通过对着手机说话来切换伺服系统。

一旦谷歌语音解码了[Shazin]发出的命令，他手机上的应用程序就会通过 WiFi 与 Arduino 进行通信。Arduino 控制一个伺服系统，理论上可以控制门上的锁定机制。

经过一点调整和一些额外的安全性，他的概念证明肯定可以派上用场。

看看下面的短视频，看看[Shazin 的]声控伺服在行动。

[https://www.youtube.com/embed/nYG2_Dgq-OA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nYG2_Dgq-OA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
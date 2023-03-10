# 机器人 G1 控制的机器人

> 原文：<https://hackaday.com/2009/01/25/forknife-android-g1-controlled-robot/>

![g1bot](img/0674ab90fb276c27a2159e0b937fbef4.png "g1bot")

当我们第一次看到[Jeffrey Nelson]的基于 G1 的机器人时，我们立即想知道控制的传输是什么。 [G1](http://www.mahalo.com/T_Mobile_G1 "T Mobile G1 - Mahalo") 的硬件支持移动中的 [USB](http://www.mahalo.com/USB) ，但它还没有在 Android 中实现。原来他实际上是通过[耳机适配器](http://www.mahalo.com/Headphones)使用 [DTMF](http://en.wikipedia.org/wiki/DTMF "Dual-tone multi-frequency - Wikipedia, the free encyclopedia") 音调来发送命令。音频插孔连接到一个 DTMF 解码器，该解码器向机器人的 [Arduino](http://hackaday.com/tag/arduino/ "arduino  - Hack a Day") 发送信号。他用 Java 编写了客户机/服务器代码，向机器人发出命令。你可以在他的网站上找到代码和一个简单的原理图。下面嵌入了机器人的视频。

[https://www.youtube.com/embed/PddThiIbGz4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PddThiIbGz4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[via [Engadget](http://www.engadget.com/2009/01/26/video-t-mobile-g1-powered-forknife-robot-goofs-off-eats-cupcak/ "T-Mobile G1-powered Forknife robot goofs off, eats cupcakes - Engadget")
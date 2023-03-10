# 从 Android 设备进行 3D 打印

> 原文：<https://hackaday.com/2012/03/10/3d-printing-from-an-android-device/>

![](img/770a24ae8fc0a7b4d41773c52536c52a.png "print")

[skullkey]在南非比勒陀利亚的 House4Hack hackerspace，他们希望找到一种方法，让孩子们对技术和桌面制作实验室感到兴奋。为了让孩子们对科技的发展有一种发自内心的感受，他创造了 [Makerdroid](http://www.house4hack.co.za/makerdroid) ，这是一个 android 应用程序，允许在 Android 平板电脑上创建 3D 对象，并准备将它们打印在 Reprap 或 Makerbot 上。

这个版本真正有趣的不仅仅是[skullkey]和他可爱的测试人员正在生成。STL 文件，目标文件也在 Android 上被转换成 GCode，而不需要传统的计算机。Makerdroid 使用非常流行的 [Skeinforge](http://fabmetheus.crsndoo.com/) 来为打印机生成指令(尽管很多人都转而使用 [Slic3r](http://slic3r.org/) )。

Makerdroid 不需要 PC 来在 3D 打印机上打印对象，但我们认为用 SD 卡将 GCode 文件从平板电脑转移到打印机的过程有点过时。使用目前正在开发的 [Android 蓝牙 Reprap 应用程序](http://www.thingiverse.com/thing:13506)，可以通过蓝牙直接从 Android 平板电脑上打印。尽管如此，我们仍然喜欢在触摸屏上打印我们刚刚创建的对象的想法，正如休息后的 Makerdroid 演示视频所示。

[https://www.youtube.com/embed/b1iYwOiiI-o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/b1iYwOiiI-o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# 用安卓手机控制 LED 矩阵

> 原文：<https://hackaday.com/2012/01/23/controlling-an-led-matrix-with-an-android-phone/>

![](img/3688790c327b508f8201424ebf315faa.png "panel")

尽管每个拥有智能手机的人口袋里都有一台小而强大的计算机，但我们还没有看到许多使用内置摄像头的便携式处理能力的应用。[迈克尔]决定改变这一点，并建立了一个 [LED 矩阵](http://nootropicdesign.com/projectlab/2012/01/22/displaying-android-video-on-led-matrix/)，显示来自手机摄像头的数据。

为了建造，[迈克尔]使用了两块来自 Adafruit 的 [32×32 LED 面板](http://www.adafruit.com/products/607)以及一个 [IOIO](http://ytai-mer.blogspot.com/2011/04/meet-ioio-io-for-android.html) 和一个 Arduino。为了构建 Android 应用，[Michael]使用了 Android [OpenCV 计算机视觉库](http://opencv.willowgarage.com/wiki/Android)，该库从 Android 相机中抓取图像，并将其下采样为 64×32 像素。这些数据通过串行连接从手机传输到 IOIO，再从 IOIO 传输到 Arduino。尽管每帧是 1024 字节，但[Michael]在他的 LED 矩阵显示器上仍能达到每秒 4 帧的速度。

休息过后，你可以看看[迈克尔]的成果。由于帧率问题，视频有点断断续续，但在 Android 软件开发类别中，它仍然是一个有趣的构建。

[https://www.youtube.com/embed/yhA4Jne7o14?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yhA4Jne7o14?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) [https://www.youtube.com/embed/zn6Ky3Qc5w4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/zn6Ky3Qc5w4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
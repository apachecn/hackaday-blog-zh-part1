# 在 LED 显示屏上处理和回放网络摄像头图像

> 原文：<https://hackaday.com/2011/04/10/webcam-images-processed-and-played-back-on-led-display/>

![](img/5a74312f389d54486db656193953dd71.png "webcam-displayed-on-led-matrix")

[Mathieu]让 bee 改进运行在 LED 矩阵上的代码，[在这个过程中添加了一些简洁的显示技巧](http://www.limpkin.fr/index.php?post/2011/04/07/Electronic-projects-and-matlab)。他想让显示器可以直接从电脑上寻址。 [96×64 双色 LED 显示屏](http://hackaday.com/2010/08/19/fpslic-powered-led-matrix/)由 Atmel FPSLIC 供电，并已使用双缓冲。让 PC 能够直接写入其中一个缓冲区并不太难，只需要一点优化就能获得正确的时间。从休息后的视频来看，他做到了。

使用 Matlab 处理每个图像，从网络摄像头流中生成视频源。只需 50 行代码即可捕获一帧，对其进行适当的大小调整，将结果转换为黑白图像以进行边缘检测，然后通过压缩图像数据以传输到嵌入式处理器来完成这项工作。我们想说这听起来更简单，但我们对这项工作印象深刻。在当前设置下，显示管理约 42 Hz。

[https://www.youtube.com/embed/ILnxZHLTEpE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ILnxZHLTEpE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
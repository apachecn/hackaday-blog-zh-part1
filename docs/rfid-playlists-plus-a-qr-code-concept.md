# RFID 播放列表加上二维码概念

> 原文：<https://hackaday.com/2012/03/15/rfid-playlists-plus-a-qr-code-concept/>

![](img/fe2bbef15a61b49e37b3dfd1acaece55.png "more-physical-toke-jukebox-ideas")

这是另一个音频播放黑客，使用物理令牌来选择你在听什么。它使用 Touchatag [RFID 硬件来控制 iTunes](http://eopossum.blogspot.com/2012/03/itunes-touchable-songcard-project.html) 。这个概念非常类似于[我们周三看到的独立 Arduino 点唱机](http://hackaday.com/2012/03/14/rfid-jukebox-for-the-kids/)，除了这个与你的电脑接口，标签选择整个专辑而不是一首歌。shell 脚本处理来自阅读器的输入标签 ID，用相关唱片集的所有曲目填充播放列表，然后执行 AppleScript 来启动该播放列表。休息之后，请观看简短的演示。

但真正吸引我们眼球的是二维码阅读器的概念，詹尼斯希望在未来的某个时候实现这一概念。计算机方面的事情不需要改变，但我们喜欢将基于 FPGA 的摄像头组装在一起以识别和解码 QR 图像的挑战。看起来[非常适合那个 10 美元的相机模块](http://hackaday.com/2012/03/07/10-camera-module-for-your-next-fpga-project/)，而且是 FPGA 驱动！

[https://www.youtube.com/embed/OBlZb2SDSNk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OBlZb2SDSNk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
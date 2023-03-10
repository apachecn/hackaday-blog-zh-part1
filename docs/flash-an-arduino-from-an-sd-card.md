# 从 SD 卡刷新 Arduino

> 原文：<https://hackaday.com/2012/02/21/flash-an-arduino-from-an-sd-card/>

![](img/7f536d8179703fd32f24ae29052d8dc2.png "ardu")

[Kevin]一直在对 Arduino IDE 使用的协议进行逆向工程，并将其移植到 Arduino 平台上。现在他的 [BootDrive](http://baldwisdom.com/bootdrive/) 项目即将完成，他准备让每个 Arduino 都能够通过 SD 卡编写另一个 Arduino。

BootDrive 与使用一个 [Arduino 作为 ISP](http://arduino.cc/en/Tutorial/ArduinoISP) 并没有太大的不同，只是现在 AVRdude 运行在 Arduino 本身上，不需要计算机将新的固件放入目标 Arduino 中。[凯文]将一个 [MicroSD 分线板](http://www.adafruit.com/products/254)连接到一个兼容 Arduino 的克隆体上。当克隆启动时，它会在 SD 卡中搜索一个名为“program.hex”的文件。该文件会被发送到目标 Arduino 并安装新固件。

虽然如果你只有几个从不离开工作台的 Arduinos，这可能不是非常实用，但我们认为，如果你需要更新已经“在现场”作为气象站或自制游戏摄像头的主板上的软件，这将是一个非常宝贵的工具。[Kevin]发布了他的 BootDrive 项目的演示；休息之后你可以去看看。

[https://www.youtube.com/embed/i4wJ4kRO80Ew=470?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/i4wJ4kRO80Ew=470?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
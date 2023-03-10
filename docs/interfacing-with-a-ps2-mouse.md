# 与 PS/2 鼠标接口

> 原文：<https://hackaday.com/2011/09/24/interfacing-with-a-ps2-mouse/>

![](img/b9bc55eeed61cfa65e39bd0b25b14375.png "ps2mouse_1")

[David]提交了他用 PIC 微控制器和一些 LED 显示器读取 PS/2 鼠标的实现。当然，这紧随使用带有 [PS/2 键盘](http://hackaday.com/2011/09/23/interfacing-with-a-ps2-keyboard/)的 PIC 之后，所以现在可能是时候开始从你的垃圾堆中挖掘出你的旧外设了。

[David]开始了他的项目，试图找出如何将鼠标连接到他的试验板上。在把 PS/2 鼠标延长线上的塑料去掉之后，他按照 T2 的针脚把所有的东西连接起来。编程 PIC 来理解 PS/2 命令有点奇怪。[David]习惯于让他的微控制器提供时钟信号。PS/2 协议有点奇怪，因为外设设置时钟。由于 PS/2 是双向协议，鼠标也接受命令。主机——大卫的 PIC——必须向鼠标发送命令，开始发送运动数据。

因为 USB 键盘和鼠标向后兼容 PS/2 端口，所以[David]试用了一些带有 USB 转 PS/2 适配器的 USB 鼠标。每次使用 USB 鼠标的尝试都失败了。奇怪的是，当一个蓝牙鼠标被尝试(通过蓝牙到 USB 到 PS/2)时，一切都完美地工作。休息之后，请查看[David]的 PIC 鼠标演示。

[https://player.vimeo.com/video/26532934](https://player.vimeo.com/video/26532934)
# 扫描仪中的数控热线切割机

> 原文：<https://hackaday.com/2009/10/19/cnc-hot-wire-cutter-from-scanners/>

![hot-wire-cutter-from-scanners](img/b26fd625483334dbf460f0f4d152702d.png "hot-wire-cutter-from-scanners")

[Raul] [造了一个数控热钢丝切割机](http://codinglab.blogspot.com/2009/09/poors-man-cnc-hot-wire-cutter-part-1.html)，他用它来切割泡沫的形状。他的设备使用两个平板扫描仪来提供两个运动平面。一个扫描臂上安装有泡沫，并提供 Y 轴移动。另一个扫描仪上安装了热线，并提供 X 轴移动。切割线安装在由大规格衣架线制成的弯曲弓上。

他接入了一台扫描仪的逻辑板以获取运动的信息。另一个通过几个 H 桥连接。两者都由 Atmel AVR ATmega128 控制，Atmel AVR atmega 128 又通过与计算机打印机端口的连接接收命令。python 程序使用 SVG 格式的矢量图形文件，并跟踪切割轮廓。

休息之后我们有一段视频。在我们的要求下，[Raul]花了一些时间贴了一组图片并对它们进行了评论。感谢您的辛勤工作和出色的工作！T3[https://www.youtube.com/embed/y1G15yUXb04?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/y1G15yUXb04?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
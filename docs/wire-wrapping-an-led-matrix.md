# 绕线 LED 矩阵

> 原文：<https://hackaday.com/2010/06/03/wire-wrapping-an-led-matrix/>

![](img/badd2993e28927d83fe9ef30fe22f54c.png "Exif JPEG")

普通读者[Osgeld]搭建了[一个 1024 LED 显示矩阵](http://www.arduino.cc/cgi-bin/yabb2/YaBB.pl?num=1267250236)。这是一个概念验证设计，他不可否认地超载了组件。最值得注意的是，如果所有八个引脚都是活动的，595 移位寄存器([在周末](http://hackaday.com/2010/05/31/beginner-concepts-cascading-shift-registers/)展示)提供了太多的电流。这很容易在下一个设计中通过升级到级联 LED 驱动器来解决。代替[焊接显示器上的每一个连接](http://hackaday.com/2009/10/02/smd-led-matrix/)，【奥斯格德】将组件焊接到位，然后使用绕线进行点对点连接。这一定为他节省了大量的时间和挫折。我们迫不及待地想看看第一个原型会产生什么。
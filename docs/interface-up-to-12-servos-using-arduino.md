# 使用 Arduino 连接多达 12 个伺服系统

> 原文：<https://hackaday.com/2010/11/24/interface-up-to-12-servos-using-arduino/>

![](img/df74e198dee3617af36d87864369c16b.png "arduino-multi-servo-control")

[Brian]正在使用一个 [Arduino 来控制多个伺服电机](http://principialabs.com/arduino-python-4-axis-servo-control/)。这并不是什么新鲜事，从 Arduino 的早期就一直在发生。但是[Brian]并没有开发一个项目并分享它，而是做了一项了不起的工作，使代码可伸缩、可读，甚至解释了不同部分如何工作。

他的代码监听串行命令，并相应地操纵马达。他使用 pyserial 编写了一个 Python 脚本，可以与 Arduino 对话。例如，他使用操纵杆发送 X 和 Y 轴以及俯仰和滚动的数据。想知道那些串行通信是如何工作的吗？他详细解释了那件事。他还概述了在标准 Arduino 上从 4 个伺服演示扩展到 12 个伺服的过程。听起来似乎是时候使用[Brian]组装的工具来构建自己版本的[鼠标控制的 Lynxmotion 手臂](http://hackaday.com/2010/07/22/mouse-controlled-manipulator-arm/)了。
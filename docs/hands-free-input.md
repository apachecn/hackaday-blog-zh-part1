# 免提输入

> 原文：<https://hackaday.com/2010/07/20/hands-free-input/>

![](img/d41e63f05e6441d0bb6b6a2166474cdb.png "hands-free-input-device")

这是[Tech B]为残障用户打造的概念输入设备。该设备使用加速度计以及压电传感器(右键单击)和按钮(左键单击)来充当鼠标。Arduino 位于帽子侧面的试验板中，通过串行连接与计算机通信，[使用 PySerial](http://www.hellboundhackers.org/articles/923-pyserial-and-serial-devices.html) 将微控制器数据转换为光标命令，具有 Python 编程语言的强大功能和易用性。

在开发过程中，[Tech B]使用一个基本的图章制作了一个概念验证视频，您可以在休息后观看。他发现这种输入设备比他的网络摄像头红外跟踪系统更简单、更准确，而且资源消耗更少。
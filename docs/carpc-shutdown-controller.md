# CarPC 关机控制器

> 原文：<https://hackaday.com/2006/04/06/carpc-shutdown-controller/>

![inverter](img/2016eceecb131b65a2268329f743cc9b.png)

我相信大多数已经开发了 CarPC 的人都已经熟悉了[关机控制器](http://www.mp3car.com/vbulletin/showpost.php?p=383433&postcount=21)，但是我认为这个黑客非常聪明。电脑不喜欢突然关机，所以你需要弄清楚如何安全地关闭电脑。这个电路有一个串行连接器，在 XP 看来是一个普通的 UPS。当点火开关关闭时，它切断了到 COM 针脚 8 的 5V 线路。XP 的反应是休眠。一旦计算机关闭，电源逆变器的继电器就会打开。当点火开关打开时，逆变器通电，计算机打开。

[感谢银丸]

*   [永久链接](http://www.mp3car.com/vbulletin/showpost.php?p=383433&postcount=21)
# 超声波测距仪作为扫描雷达

> 原文：<https://hackaday.com/2011/10/10/ultrasonic-rangefinder-as-scanning-radar/>

![](img/b487ad48ed9e9a7e591bdfd7368079c4.png "ultrasonic-scanning-radar")

超声波测距仪是一种收集避障数据的廉价而简单的方法。当添加到伺服电机上时，它们就形成了一种用于近距离物体的扫描雷达。

在该实现中，[Rui Cabral]驱动伺服系统，并使用 PIC 18F4520 从传感器收集数据。伺服旋转 180 度，以 9 度的增量进行传感器测量。如果它发现了障碍物，就会记录下距离和方向。反馈显示在一个 20 LED 条形图显示器上，该显示器显示一个移动的 LED 来跟踪传感器的方向，只要发现物体，LED 就保持点亮。目前，障碍物数据是通过与 PC 的串行连接推送的，但可以很容易地注入机器人的导航逻辑，以便对障碍物周围的路径进行三角测量。休息之后你可以看到芮的项目在运作。

几年前，我们用不同的显示技术研究了同样的概念。该黑客使用了 Arduino 和处理功能来用传统的绿色扫描显示器绘制传感器数据。

[https://www.youtube.com/embed/KeNF3fzqa_I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KeNF3fzqa_I?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢大羚羊]
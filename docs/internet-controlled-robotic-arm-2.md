# 互联网控制的机器人手臂

> 原文：<https://hackaday.com/2011/11/24/internet-controlled-robotic-arm-2/>

![](img/000692e12a7ec4fe61a8f01bcea35a87.png "arm")

锈迹斑斑的钉子车间的伙计们已经安装了一个[网络控制的机械臂](http://www.rustynailworkshop.com/Robotic_Arm.html)供你娱乐。当你在等待火鸡烤好(或者，你知道，工作)的时候，试着用遥控机械臂移动一些乐高积木。

[构建日志](http://www.rustynailworkshop.com/Projects/Entries/2011/11/19_Internet_Controlled_Robotic_Arm.html)遍历构建所需的部分。手臂本身是一个 [Lynxmotion AL-5D](http://www.lynxmotion.com/c-130-al5d.aspx) ，一个重型设备，比我们的旧 [Armatron](http://en.wikipedia.org/wiki/Armatron) 更有能力，看起来也更好。

手臂由 Arduino Uno 控制。Arduino 连接到手臂的伺服控制器。以太网屏蔽接收运动命令，并将其转换为伺服命令。整个建筑独立于计算机运行，就像这个项目的灵感一样，Orbduino。

当然，你可以想象如果多人同时试图控制机器人，会造成多大的混乱。该项目网站上的一点代码可以确保在任何给定时间只有一个人可以控制机器人。看看别人用 Waldo 用乐高积木在建什么。如果你幸运的话，你将能完成那项工作。
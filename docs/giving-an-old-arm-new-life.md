# 赋予一只旧胳膊新的生命

> 原文：<https://hackaday.com/2009/12/18/giving-an-old-arm-new-life/>

![](img/5b3398452508546913caac861ee465a5.png "robotic-arm-driver-circuit")

[Jarek]发现一个不起作用的机械臂闲置着，[想让它再次工作](http://www.soniktech.com/arm.php)。通过在 Arduino 上添加一些定制板，他成功做到了这一点。

该臂由六个步进电机驱动，每个电机有四根控制线。为了处理所有这些问题，[Jarek]使用 TIP120 晶体管来保护控制器。这仍然留下了 24 条控制线要连接的问题。通过使用几个 74HC4514 多路分解芯片，他将数量减少到只有 8 个 Arduino 控制引脚。他通过将原始的 Playstation 控制器作为输入设备来完成这个项目。

该项目的源代码[可以下载](http://www.soniktech.com/arm/arm.txt)，但我们没有看到他的设置示意图。这不应该是一个问题，因为器件数量少意味着晶体管和解复用器的数据手册是您真正需要的。
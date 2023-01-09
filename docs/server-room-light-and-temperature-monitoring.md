# 服务器机房照明和温度监控

> 原文：<https://hackaday.com/2011/04/27/server-room-light-and-temperature-monitoring/>

![environ_monitoring](img/76768e403325e07c6afec8d354cc2193.png "environ_monitoring")

[Jaren]偶尔会健忘，经常怀疑自己是否忘了关服务器机房的灯。不知道灯是否还亮着让他抓狂，直到他第二天早上回去工作，所以他决定他必须做点什么。他认为制造一个小传感器来监控头顶上的灯的状态很容易，但是他不想因为执行一个简单的任务而浪费他的微控制器的能力。相反，他计划添加一系列其他传感器，使他能够监控房间的温度、声音水平以及服务器的电流消耗。

现在这个项目还处于开始阶段，但是他已经建立了部分传感器网络。他将一个基于 TMP421 的温度模块和一个 TEMT6000 环境光传感器连接到他的 Arduino 上，Arduino 将数据显示在他购买的一个小 LCD 屏幕上。更多的传感器正在订购中，所以我们应该期待在未来几周内看到更多的进展。

希望当一切都完成后，我们将看到一套完整的原理图和代码，这样任何人都可以根据自己的设计构建自己的服务器机房监控网络。
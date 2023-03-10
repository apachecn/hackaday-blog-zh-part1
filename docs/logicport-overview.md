# 逻辑端口概述

> 原文：<https://hackaday.com/2008/06/24/logicport-overview/>

![](img/d6e6972402e4c9cdaffd901e49a4ff60.png)
正如之前承诺的，不久的将来实验室已经公布了[逻辑端口逻辑分析仪](http://www.nearfuturelaboratory.com/2008/06/21/logicport-overview/)的概述。他们用[的 Playstation 2 分析](http://www.nearfuturelaboratory.com/2008/06/19/playstation2-logic-analysis/)作为例子。逻辑端口使用“解释器”来定义协议。它具有 I2C/TWI、SPI、RS232 和 CAN 2.0A/2.0B，但您可以基于这些构建自己的解释器。您可以指定数据的位顺序和格式。从解释器可以用于特定的任务:在 PS2 中，它们只显示第五个字节，也就是实际的按钮按压。

“触发器”用于发出特定活动的信号。在 PS2 上，一个连接到从选择线上的下降信号。该事件意味着主机将要开始发送数据。

最后一个值得探索的领域是“测量”。这些可以是事件之间的频率或任意时间间隔。逻辑端口有多个接地连接，以消除信号中的噪声，你必须调整采样率和逻辑电平，以使事情顺利运行。很高兴看到从一个刚刚开始使用这个工具的人的角度来写操作方法。

*   [永久链接](http://www.nearfuturelaboratory.com/2008/06/21/logicport-overview/)
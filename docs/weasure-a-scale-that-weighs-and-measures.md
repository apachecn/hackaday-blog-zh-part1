# Weasure，一种用于称重和测量的秤

> 原文：<https://hackaday.com/2008/11/09/weasure-a-scale-that-weighs-and-measures/>

![weasure](img/531cb304656594df8aa8413f6b84ce16.png "weasure")

[John Peterson]为瑞萨设计竞赛设计了这款邮政秤设备。Weasure 不仅计算[包装的总重量，还计算尺寸](http://www.circuitcellar.com/renesas2005m16c/winners/1727.htm "Renesas M16C Design Contest 2005")。他使用一个 SKP16C62P 评估板来构建它，该评估板有一个 LCD、按钮和 led 指示灯。最初的 DigiWeigh 包裹秤经过改进，可提供 PWM 输出和皮重控制。他在每个轴的每一英寸都嵌入了光敏电阻。它们稍微向上倾斜，周围被涂成黑色以减少反射。Weasure 通过串行连接输出所有内容，因此它可以与运输软件一起使用来生成邮资。
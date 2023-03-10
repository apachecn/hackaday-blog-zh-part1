# 变色杯垫有内置的饮料探测器

> 原文：<https://hackaday.com/2012/03/15/color-changing-coaster-has-a-built-in-drink-detector/>

![](img/86a6ae52c4e03b41c35a49e41823363d.png "color-changing-coasters")

[罗伯特]组装了他自己的发光杯垫，这些杯垫知道它们什么时候可以盛酒。由于专业生产的 PCB 和分层的激光切割丙烯酸外壳，它们看起来非常棒。它们很像给餐馆里等待就餐的人的寻呼机，但这个版本更花哨(不包括振动/寻呼功能)。

RGB-LED 板是之前的项目的[,该项目是使用圆形板周围的八个表面贴装 RGB LED 模块开发的。它使用 ATmega168 搭配 MBI5168 恒流 LED 吸收驱动器。过山车的外壳给他留出了更多的空间来放置一些物品，比如一对 AA 电池，它与一个升压转换器一起为设备供电。它还装有一个红外反射传感器，用于检测杯垫上是否有饮料。这很重要，因为如果没有玻璃来分散发光二极管的强度，有人乘坐的杯垫看起来会非常明亮。](http://blog.spitzenpfeil.org/wordpress/2012/01/11/rgb-led-ring-v2-sequels-dont-have-to-be-bad/)

他提到白炽灯泡会干扰红外反射传感器。但是一定有某种方法可以用代码来解释环境条件，对吗？
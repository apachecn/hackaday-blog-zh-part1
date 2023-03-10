# 燃烧的人:海盗船运动 Arduino 动力火焰帆

> 原文：<https://hackaday.com/2011/08/25/burning-man-pirate-ship-sports-arduino-powered-flame-sails/>

![](img/a395be2078e018b313dec7d4006fb267.png "Pirateship")

2011 年火人节几天后就要开始了，我们有了一个优秀的突变车辆配件，任何疯狂的沙漠居民都不应该没有。一个 Arduino 驱动的[消防炮序列器](http://www.dorkbotpdx.org/blog/paul/pirate_ship_fire_sequencer)！Lostmachine 的[Andy]要求[Paul]为他们的[私人飞船](http://www.lostmachine.com/blog/)变异飞行器增加火焰效果，并提供一个看起来很酷的代表船帆的火焰表演。

[Paul]将一只装满拱廊按钮、开关和液晶显示器的手扔在一起，控制八个 12V 电磁阀，这些电磁阀的任务是打开各种调节丙烷源，产生一些看起来很残酷的火焰效果。该控制器将 Teensy 2.0 与包含八个 P 沟道 MOSFET 电路的定制板相结合。来自线圈的回扫通过齐纳二极管处理，IRFR5305s 的尺寸远远超过 12v 螺线管所需的尺寸。由于沙漠的炎热、灰尘和混乱，人们越小心越好。[Paul]甚至扔在 RC 缓冲电路只是为了防止事情变得太失控。在十二个街机按钮中，八个用于手动控制，其余四个街机按钮、旋钮、开关和 LCD 显示器都连接到 Teensy 以处理序列。遗憾的是，[保罗]将不能去火人节解决音序器的问题，这是整个版本中的一个问题。

碰巧我这周五要去火人节，我有一个 18 英寸乘 18 英寸的二维码来标记我的区域，看看你能不能在那里找到我！还可以看看一段视频，视频中的定序器在跳跃后控制着一个 6 英尺长的火焰棒。

[https://www.youtube.com/embed/t2C4wwPY2to?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/t2C4wwPY2to?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
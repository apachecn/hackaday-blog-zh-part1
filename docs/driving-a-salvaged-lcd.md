# 驾驶回收的液晶显示器

> 原文：<https://hackaday.com/2011/02/10/driving-a-salvaged-lcd/>

![](img/4f61c545332920370c463a5ae2c9103e.png "010")

[bill2009]想要重复使用一些常见的七段液晶显示器，但问题是如何驱动它们。凭借来自[Microchip]和[Atmel]的几份应用笔记、一台示波器和一台 Arduino，他制作了[概念验证](http://arduino.cc/forum/index.php/topic,51464.0.html),表明驱动许多设备都有的小型反射式液晶显示器并不太难。

首先发现这些东西确实是多路复用的，他接着研究驱动它们所需要的东西，它与背板的电压差约为+-2 伏，接下来是找到一个施主，他很容易在 Staples 找到这个施主，它的形式是一个“clocky”型的逃跑闹钟。

在四处查看了信号对 LCD 上不同部分的影响后，他迅速设计了一个小电路来控制 Arduino 的显示。通过使用一组下拉电阻和切换微控制器上的引脚模式，可以实现各段所需的正负电压。

这些小型分段液晶显示器无处不在，能够使用它们是一个很大的奖励。
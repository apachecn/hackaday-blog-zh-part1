# 替换速度计

> 原文：<https://hackaday.com/2010/06/17/replacement-speedometer/>

![](img/480034ddc0e91edd1d9b66d6a019b577.png "replacement-speedometer")

在原来的速度表电缆坏了之后，霍华德为他的卡车制造了自己的替换速度表。他使用表面贴装元件，并制作了一个相当不错的两板设计。当他向我们通风报信时，他提到这是 Arduino 驱动的，使用霍尔效应传感器。在他的文章中没有谈到这一点，但我们推断他只是使用 AVR 芯片上的引导程序，霍尔效应传感器测量其中一个轮子的旋转。当车辆不移动时，板在最大速度和行程距离之间交替。一旦他开始滚动，它就会显示当前速度。
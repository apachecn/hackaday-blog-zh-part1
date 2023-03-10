# 空间化的伞

> 原文：<https://hackaday.com/2009/04/12/spatialized-umbrella/>

![umbrella-1](img/4c5246ec896bf43335c65b64d2e3fbe6.png "umbrella-1")

读者乔·萨维德拉发来了他的最新项目:空间化的雨伞。每个伞骨的底部都有一个 LED、扬声器和距离传感器。这些连接到运行 Arduino 环境的 ATMega168 微控制器。红外传感器根据接近程度触发雨滴声。更短的距离意味着更多的水滴被打出。声音是使用查找表和数字引脚产生的。你可以看到下面嵌入的演示视频。

使用没有关联板的 Arduino 环境是[Joe]正在研究的另一个想法的一部分。 [MapDuino 项目](http://hackduino.org/mapblog/ "MapDuino Project")使用标准 Arduino 硬件进行编程，但随后将芯片转移到目标项目中更为准系统的电路。他们最初的工作基于 [ITP 试验板 Arduino](http://itp.nyu.edu/physcomp/Tutorials/ArduinoBreadboard "Physical Computing at ITP | Tutorials / Setting up an Arduino on a breadboard") 。

[https://player.vimeo.com/video/4073522](https://player.vimeo.com/video/4073522)
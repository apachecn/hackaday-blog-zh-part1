# Ego Box 监控网络点击率

> 原文：<https://hackaday.com/2011/01/29/ego-box-monitors-web-hits/>

![](img/097f285c1169a7b5cc4b8c4f1b1ba42c.png "ego-box")

[波格丹一世]的最新项目是一个显示所选网站点击率的盒子。他称之为“自我盒子”,因为根据交通状况，它要么膨胀要么摧毁你的自我。这提供了与[我们的巨魔嗅探鼠](http://hackaday.com/2010/12/19/hackaday-unleashes-a-troll-sniffing-rat/)相似的功能，但最大的不同是这是一个独立的以太网设备。这要归功于管理堆栈的 ENC28J60 以太网控制器芯片，该芯片在 DIY 电子项目中非常受欢迎。为了监控你的点击率，[波格丹一世]编写了一些代码添加到你的索引页面的标题。每次加载页面时，它都会增加计数器文件，而 Ego Box 只是监视该文件，在 8 位 7 段显示器上显示流量。

[途径 [Adafruit](http://www.adafruit.com/blog/2011/01/28/the-ego-box/)
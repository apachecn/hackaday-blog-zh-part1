# 汽车电流监控器

> 原文：<https://hackaday.com/2009/12/16/automotive-current-monitor/>

![](img/d1ae223455b1ce25ccdb6283676fbb52.png "automotive-current-monitoring")

如果你曾经有过一辆电气系统有问题的车，你就会知道找出你的问题的根源有多难。这里有一个黑客解决方案，使用一个 diy [PCB 来监控从交流发电机流出的](http://www.imsolidstate.com/archives/9)电流。检测由 Allegro ACS758 集成电路提供。该芯片测量高达 150A 的电流，并输出可由微控制器测量的模拟信号。在这种情况下，AVR ATmega8 测量信号，并通过串行端口将信息传回 PC。该数据可以用图表表示，以帮助确定电池何时消耗过多电流而无法保持充电。

看看那块数控铣削的 PCB，多漂亮啊！

[Thanks Joshua via [Elektronika](http://www.elektronika.ba/726/how-much-electric-current-does-your-vehicle-use/) ]
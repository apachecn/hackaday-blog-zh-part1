# 改装成太阳能充电站的野营灯

> 原文：<https://hackaday.com/2011/11/04/camping-light-retrofitted-as-a-solar-recharging-station/>

[![](img/d8053dcdf460e1c615c5bbd184d5eafb.png "camping-light-retrofit")](http://hackaday.com/wp-content/uploads/2011/11/camping-light-retrofit.jpg)

有了在音乐节上逗留几天的宏伟计划，[Josh]需要一种方法为他的便携式设备充电。过去他总是随身携带 12V 电池，但今年他想让事情变得更简单。他结束了改装野营灯的工作，在夏日阳光的帮助下完成这项工作。

该项目的第一步是寻找一些充电电池。他考虑过锂离子电池的想法，但最终选择了镍氢电池，因为它的充电更宽容，而且价格也很便宜。由于工作电压较低(1.2V 对碱性的 1.5V)，他需要在灯壳里多装两个。在这里你可以看到，他只是设法让他们适合在电线运行区的情况下。

接下来是充电电路。他的设计基于 ATmega44，使用分压器和 ADC 来检测电池何时充满。白天，它与外部太阳能电池板相连，当他晚上回来时，它可以为他的手机充电。
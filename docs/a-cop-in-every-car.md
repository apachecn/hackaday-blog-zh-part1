# 每辆车里都有警察

> 原文：<https://hackaday.com/2010/04/06/a-cop-in-every-car/>

![](img/ad3c7d585deff490dcebfccf9712dbce.png "arduino-speed-enforcer")

[迈克尔]设计这个显示板是为了模仿警车把你拦下来的样子。当[控制板测量车速](http://nootropicdesign.com/projectlab/2010/04/05/speed-trap/)时，它位于他汽车的后窗(面向前方)。Arduino 从 GPS 模块获取 NMEA 数据，并将其与限速表进行比较。如果你在超速行驶，根据你当前的位置，红色和蓝色会闪烁，就好像你要靠边停车一样。对于我们来说，因为领先一步而被抓的刺激听起来并不有趣，但对于每个人来说都是如此。

顺便说一句，[迈克尔]使用的是 EM406 GPS 模块，与令人沮丧的浪漫盒子使用的是同一个模块。
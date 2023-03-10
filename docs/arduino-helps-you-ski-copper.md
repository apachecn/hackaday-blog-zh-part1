# Arduino 帮助你滑铜

> 原文：<https://hackaday.com/2010/02/11/arduino-helps-you-ski-copper/>

![](img/80c9750d49711300d996b83d5702810a.png "arduino-powered-copper-mountain")

[Dwight 的]一直在做一个长期项目，为铜山滑雪场的滑雪道添加一个状态板。该板将为每次跑步配备一个 8×8 的 LED 模块，显示绿色 O 代表开放步道，绿色 G 代表整洁步道，红色 X 代表封闭步道。他还有一个状态板，led 嵌在一个轨迹地图上。

系统的每个 LED 模块都依赖 SPI。Arduino Mega 使用 Xbee 模块无线下载 XML 数据，并将其显示在这块板上。由于[跟踪报告已经可以在网上获得](http://www.coppercolorado.com/winter/the_mountain/dom/trails.html)，这只是一个以一种有用的方式解析数据的问题。

他还没有完全完成整件事，但是如果你打算在铜山滑雪的话，请留意一下。

[via [汤姆指南](http://www.tomsguide.com/us/pictures-story/146-5-sparkfun-makers-inventions.html)
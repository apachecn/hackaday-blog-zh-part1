# 使用视差 Ping 传感器监控水位

> 原文：<https://hackaday.com/2011/08/30/monitoring-water-levels-with-a-parallax-ping-sensor/>

![arduino_parallax_ping_water_level_sensor](img/994f85e66882a2cf350284c5e9a5dd40.png "arduino_parallax_ping_water_level_sensor")

当你需要一种机制来检测容器或水箱中的水位时，你有几种不同的选择。大多数人选择一个简单的浮子或探针，位于水中，[，而其他人则使用光学](http://hackaday.com/2011/04/15/aquarium-overflow-sensor-saves-your-fish-and-your-floors/)来感知何时水位达到不希望的水平。

由[Danilo Abbasciano]制造的这个设备使用了视差 Ping 传感器。如果将传感器放置在井、水箱或其他水容器的顶部，它可以精确计算内部流体的高度和体积。这是通过使用 Ping 的读数结合用户已知的几个值，即容器的尺寸来完成的。

在他的实施中，读数被传递到一个简单的 LCD 面板上以便于查看，一个小型压电扬声器被用来在水位达到预定阈值时发出警报。在接触式传感器易受化学物质和腐蚀影响的情况下，或者存在污染问题的情况下，这种测量设备非常有用。
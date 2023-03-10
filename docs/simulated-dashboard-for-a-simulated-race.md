# 模拟赛车的模拟仪表板

> 原文：<https://hackaday.com/2012/01/29/simulated-dashboard-for-a-simulated-race/>

对于许多游戏玩家来说，模拟器可能已经失去了他们的酷，但是[Fergo]正在试图东山再起。他为赛车模拟器制作了一个电子仪表板。

[Fergo]大部分时间都花在 MMO 赛车模拟器 iRacing 上。可能是受[一级方程式方向盘](http://www.formula1.com/inside_f1/understanding_the_sport/5287.html)的一点点影响，他想在他的仪表盘上添加微软赛车方向盘。仪表板包括 RPM 灯、档位指示器、五个通用按钮、旋转编码器、坑限制器、转速限制器和低燃油指示器。

该版本由一个 VB.NET 应用程序提供支持，该应用程序将 iRacing API 连接到一个 Arduino。为了让所有这些按钮和 led 与 Arduino 对话，[Fergo]使用了一个通过 I2C 总线通信的 [IO 扩展器](http://www.nxp.com/products/interface_and_connectivity/i2c/i2c_general_purpose_i_o/PCF8574.html)。这是一个令人惊讶的简单设计，如果[Fergo]决定扩大他的驾驶舱，它应该可以很好地扩展。我们不确定它是否能处理[控制一架 737](http://hackaday.com/2012/01/06/737-cockpit-will-satisfy-even-the-most-discriminating-simulator-afficiandos/) ，但对于一架塞斯纳 172 或水星太空舱来说，这已经足够了。

休息之后，看看[Fergo]用他的按钮盒仪表板在赛道上跑来跑去。

[https://www.youtube.com/embed/HZp3mMatO1w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HZp3mMatO1w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# 读取二极管以创建热成像系统

> 原文：<https://hackaday.com/2012/02/01/reading-diodes-to-create-a-thermal-imaging-system/>

![](img/fb6235ba6bb28b08c1dadb8f901b247c.png "thermal-imaging-using-diodes")

[Udo Klein]正在研究一些 1N4148 晶体管，他对这些晶体管在不同温度下的性能规格很感兴趣。正向电压实际上随温度变化很大，不知道能否可靠地测量。他为 Arduino [破解了自己的 LED 防护罩，用作 1×20 热成像系统](http://blog.blinkenlight.net/experiments/measurements/thermal-imaging/)。

上面的截图是从一排二极管映射电压测量值(见休息后的视频，以获得完整的图片)。他拿着一个冰袋放在一排二极管上，观察变化。从 Arduino 中提取数据的 Python 脚本有助于屏幕显示。由于没有足够的模拟输入来分别读取所有 20 个二极管，它们被多路复用。四个 I/O 引脚分别使能五个二极管，在进入下一组之前，读取五个模拟输入。

这能用来做什么？这完全是个错误的问题…有时候你必须去你的好奇心带你去的地方。[https://www.youtube.com/embed/lHH-MTriwh8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lHH-MTriwh8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
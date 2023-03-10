# 指尖心率监测器

> 原文：<https://hackaday.com/2011/02/17/fingertip-heart-rate-monitor/>

![](img/51c0d35eba6bf1eb6da6ae542e539923.png "HeartRateMeasurementBoard")

[嵌入式实验室]有一个很好的[教程，教你如何构建自己的心率监测器](http://embedded-lab.com/blog/?p=1671)。该监视器的工作原理是将红外光照射到指尖，并观察心跳引起的反射红外信号的变化。红外探测器产生非常小的交流信号，因此使用两个运算放大器对信号进行滤波和放大。然后，PIC16F628A 读入滤波电路的输出，对节拍进行计数，并在七段显示器上显示出来。如果你已经放下了你的微控制器，并且想学习一些模拟电子学，这可能是一个不错的尝试。最后需要注意的是，构建这样一个电路的两个主要问题是串扰和调整滤波器。红外二极管和接收器应该彼此靠近，以实现最大反射，但你也需要确保不要让发射器直接照射到检测器上，因为反射光会被明亮的发射器淹没。

[通过[使](http://blog.makezine.com/archive/2011/02/how-to-fingertip-heart-rate-monitor.html)
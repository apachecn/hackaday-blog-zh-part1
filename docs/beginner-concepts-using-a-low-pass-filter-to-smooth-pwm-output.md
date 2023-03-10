# 初学者概念:使用低通滤波器平滑 PWM 输出

> 原文：<https://hackaday.com/2011/06/16/beginner-concepts-using-a-low-pass-filter-to-smooth-pwm-output/>

微控制器本质上是数字设备。它们可以做一些奇特的事情，比如把模拟信号转换成数字值，但是反过来就有点困难了。脉宽调制用于近似模拟输出，但实际上是非常快速地开启和关闭工作电压，以达到两者之间的平均值。这是调暗 LED 最常用的方法。但是以这种方式产生平滑的电压只需要多几个部件。

[Scott Daniels]花了一些时间讨论使用低通滤波器平滑 PWM 输出的过程[。这是数字和模拟电路的汇编，可以产生比 PWM 本身更平滑的信号。如上所示，低通滤波器由一个电阻和一个电容组成。这一理论不难理解，在[Scott]的帮助下，你会更容易为自己的滤波器选择元件值。他的例子集中在使用 analogWrite()函数的 Arduino 上，但是这些技术可以普遍应用。](http://provideyourown.com/2011/analogwrite-convert-pwm-to-voltage/)
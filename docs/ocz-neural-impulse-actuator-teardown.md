# 神经脉冲致动器拆卸

> 原文：<https://hackaday.com/2008/09/18/ocz-neural-impulse-actuator-teardown/>

![](img/066ebc7411102368e10c5cd35e6f7e49.png "ocz_neuro")

[m8ta fun](http://m8ta.com/index.pl) 对 OCZ 的神经脉冲致动器(NIA) 做了一次广泛的[拆解。OCZ 的计算机/思维界面实际上是一个相当直接的设计。一个模拟前端用几个](http://m8ta.com/index.pl?pid=600)[运算放大器](http://en.wikipedia.org/wiki/Operational_amplifier)净化并放大“神经”信号，然后将其馈送到 24 位[模数转换器](http://en.wikipedia.org/wiki/Analog-to-digital_converter) (ADC)。一个支持 USB 的 PIC 微控制器通过一个[通用 7400 系列](http://en.wikipedia.org/wiki/7400_series)并行到串行适配器 IC 读取 24 位并行 ADC 输出。该设备有一个 [ICSP 编程头](http://www.instructables.com/id/Understanding-ICSP-for-PIC-Microcontrollers/)(右上)，尽管尚不清楚 PIC 是否可以读写。

[谢谢，joeyo]
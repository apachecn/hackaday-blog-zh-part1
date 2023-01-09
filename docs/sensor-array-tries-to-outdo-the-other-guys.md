# 传感器阵列试图超越其他人

> 原文：<https://hackaday.com/2012/01/17/sensor-array-tries-to-outdo-the-other-guys/>

![](img/f9843dad5c840341d7670fb8585ea9d1.png "sensor-array-goes-for-broke")

路易斯维尔黑客空间 LVL1 的团队在收集环境数据方面也不甘示弱。他们把传感器板这个科学怪人放在一起，让你收集大量数据，显示周围发生了什么。

在中间偏左的位置，一个小的 Arduino 克隆体负责收集数据。他们的文章中没有提到数据存储，但如果是 ATmega328 芯片，你应该能够找到一种简单的方法在 1k 的内部 EEPROM 上存储数据。如果这还不够，板上还有一条 I2C 总线，可以方便地添加兼容的 EEPROM。

左下角的传感器应该看起来很熟悉。这是一个 DHT11 温度和湿度传感器，我们已经看到最近在项目中出现的。但是等等，还有一个 TMP102 温度传感器；但这还不是结束。BMP085 压力传感器还包括第三种温度传感选项。想看看房间里的灯什么时候亮？为此有一个 CdS 传感器和一个 TSL230R Lux 传感器。运算放大器电路可以通过 Arduino 的一个 ADC 引脚测量房间内的音量。最后，使用 RTC 板对数据进行时间标记。

显然，这是矫枉过正，我们确信这是作为各种传感器的测试平台。所有这些都已经安装在原型板上，并使用点对点焊接方法进行布线。
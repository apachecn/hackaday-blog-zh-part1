# AccelR8，一个自制的重力计

> 原文：<https://hackaday.com/2006/02/08/accelr8-a-homemade-g-meter/>

![g-meter](img/80fd7fa13b9e9354a37f3691187690e2.png)

Jesper 用少量的 IC 创造了一个汽车性能测量仪。关键芯片是 ADI 公司的 ADXL202。它测量加速度，而 AVR 8515 跟踪时间并进行所有计算。你只需要输入车辆的重量，计价器就会计算出你的 0-60 英里/小时时间，60-0 刹车距离和最大马力。Jesper 的网站上有一个完整的原理图，但代码仍然需要解决一些问题。这个项目本质上是第一代 [G-TECH/Pro 米](http://www.gtechpro.com/)的再现(邦尼有一张[原板](http://www.bunniestudios.com/wordpress/?p=74)的图片)。新一代 G-TECH 仪表玩起来很有趣，可以做一些有趣的事情，如通过测量电气系统中的噪声来确定发动机的转速。

*   [永久链接](http://www.myplace.nu/avr/accelr8/index.htm)
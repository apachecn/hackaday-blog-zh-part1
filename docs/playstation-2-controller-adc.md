# Playstation 2 控制器 ADC

> 原文：<https://hackaday.com/2005/12/18/playstation-2-controller-adc/>

![ps2](img/5dae976a4acf94f4d3615d8c4cc739c5.png)

[Paul Skinner]发来了一个他正在做的有趣的项目。目标是使用生物反馈(心率、皮肤温度)进行声音控制。Playstation 控制器提供多个模拟输入，因此 Paul 决定修改其中一个，将其用作模数转换器。在拆除控制器之前，他将控制器连接到 Max/MSP，以确保他可以读取输入。该项目的大部分时间都花在了为皮肤温度和其他传感器构建放大器上。放大器电路构建完成后，Paul 构建了几个 Max/MSP 补丁来使用这些数据。

*   [永久链接](http://blog.pixelcrypt.com/sound/)
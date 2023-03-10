# at tiny Hacks:Serial couple–带串行输出的独立热电偶 ADC 板

> 原文：<https://hackaday.com/2011/09/23/attiny-hacks-serialcouple-a-standalone-thermocouple-adc-board-with-serial-out/>

![ATtiny Hacks Theme Banner](img/5f674cf2d4b94faba5f6b413d805f657.png "ATtiny Hacks Theme Banner")

![serialcouple_thermocouple_adc_board](img/db71d2ae7b1153a72138f6925657d818.png "serialcouple_thermocouple_adc_board")

由于我们正在展示各种各样的 ATtiny hacks，因此[Kenneth]写了一篇文章来分享他在过去几个月中开发的一个项目,[serial couple。](http://kennethfinnegan.blogspot.com/2011/06/serialcouple-thermocouple-adc.html)

几乎所有开发平台都能够充当模数转换器，但当您只需要计算机的串行输出时，您并不总是需要全功能板。[Kenneth]利用他的 SerialCouple 板，试图通过构建一个独立的热电偶 ADC 板来降低过程的复杂性。SerialCouple 设计用于从热电偶获取模拟读数，将其转换为数字值，然后通过串行连接发送给任何设备。这项繁重的工作由 Maxim MAX31855 芯片完成，它将热电偶的模拟数据转换为数字温度读数。然后，板载 ATtiny2313 检索温度的数字表示，并通过串行端口发送数据。

如果您一直在寻找独立的热电偶 ADC 板，请务必访问他的网站，看看他的代码和原理图。

继续阅读，观看解释串行耦合如何工作的简短视频演示。

[https://www.youtube.com/embed/_y5MDVV93To?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_y5MDVV93To?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# 逆向工程无线气象站

> 原文：<https://hackaday.com/2011/06/13/reverse-engineering-wireless-weather-stations/>

![lacrosse_wireless_temp_sensor](img/d52711ae695dfebe82e1b461918b1b74.png "lacrosse_wireless_temp_sensor")

[Fred]收到了一个 La Crosse 无线气象站作为礼物，他认为 LCD 显示屏很棒，但他感到沮丧的是，无法提取温度数据供计算机使用。他认为，如果他能得到数据的话，这个系统的模块化设计会使它非常适合用于他的家庭自动化项目。

他冲进基站，开始四处寻找容易获得他正在寻找的数据的地方。他考虑接入控制 LCD 的总线，希望找到一个容易解码的信号，但气象站使用了一个集成 LCD 控制器的专有芯片，这几乎是不可能的。相反，他开始嗅探通过无线链接传来的数据，虽然他还不知道他看到了什么，但这是一个开始。

他使用 Audacity 嗅探信号，最终发现基站从每个传感器接收 40 位数据突发。他进一步挖掘，在网上找到的一些数据的帮助下，他能够解码数据包。他遇到的最后一个障碍是弄清楚系统的 CRC 编码是如何工作的。这需要一点努力，但他最终得到了它，现在可以记录数据包，知道数据是完整无缺的。

到目前为止，看起来他的温度监测系统工作得很好，尽管他计划在不久的将来进行几项改进。如果您有一个类似的单元，并且对扩展其功能感兴趣，[Fred]已经在他的网站上发布了大量代码。
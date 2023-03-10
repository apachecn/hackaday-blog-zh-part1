# 让开关模式电源为您服务

> 原文：<https://hackaday.com/2010/08/29/make-switched-mode-power-supplies-do-your-bidding/>

[Ken]需要提供 3.3 伏的稳压电源。他开始使用一个线性电压调节器，但是经过一些计算后，他发现他输入的 72%都被热损耗了。这个问题的解决方案是开关模式电源。SMPS 不是通过分压器消耗能量，而是非常快速地开关电源以达到所需的电压。

一个汽车充电器类型的 USB 调节器被选为[肯的]捐赠设备。他认为[调整内部电阻会影响输出电压](http://egeekrambling.blogspot.com/2010/08/building-blocks-switch-mode-power.html)，他是对的。他调整了分压器，最终稳定在 3.295 伏。

我们请他分享他在研究电路板时整理的原理图，他通过了。广告之后，请查看 DC-DC 转换器数据手册的链接。

[![](img/15679f9a38c7203c387904c41207d03b.png "smps-schematic")](http://hackaday.com/wp-content/uploads/2010/08/smps-schematic.jpg)

以上是[Ken 的]手绘示意图。在与他谈论这个项目后，他拿起一个珠宝商的放大镜，能够识别电路中的 DC-DC 转换器。这是一款 MC34063，其[数据手册可在此处找到(PDF)](http://www.st.com/stonline/products/literature/ds/5257/mc34063ab.pdf) 。
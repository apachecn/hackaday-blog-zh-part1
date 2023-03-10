# 构建您自己的可编程逻辑控制器

> 原文：<https://hackaday.com/2011/05/04/build-your-own-programmable-logic-controller/>

![](img/917d5c0ed6a979aa9b6b24419ecda8c4.png "building-your-own-PLC")

[Q]是一名在工业环境中工作的电气工程师。他经常在工作中使用可编程逻辑控制器，但自己从未制造过。他决定在家里承担这个项目，并设法[建造了一个输出 120 伏交流电或 12 伏 DC 并具有光隔离输入的 PLC](http://sites.google.com/site/qeewiki/projects/plc)。

在电路板上，你会发现一个 ATmega8 和一个 EEPROM 的额外数据存储。六路输出由继电器控制，因为它们能够输出交流电或直流电。有 8 路输入使用光隔离器作为缓冲器来保护微控制器。

那他最后用这个做什么？这是他去年圣诞灯饰的一部分。上图显示了一个防水电气盒中的 PLC，延长线连接到他希望控制的每个设备。示例代码是他在 X-mas 设置中使用的代码，但它应该足以指导您对任何应用程序进行编程。
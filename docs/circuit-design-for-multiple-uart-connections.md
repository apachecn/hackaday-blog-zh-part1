# 多 UART 连接的电路设计

> 原文：<https://hackaday.com/2011/06/28/circuit-design-for-multiple-uart-connections/>

![](img/845fa2f85f3445bcec02336c3b614b33.png "multiple-uart-connections")

[比尔·波特]有一个技巧，可以让[设计出与单个微控制器 UART](http://www.billporter.info/how-to-add-multiple-uart-connections/) 有多个连接的电路。这源于对一个朋友的电路设计的审查，该设计在项目中使用了 UART，但也要求使用 FTDI 芯片，以便通过 USB 和 bootloader 进行重新编程。与上面的原理图不同，该电路要求直接连接，无需任何电阻。在这种设计下，如果两台设备同时连接并试图通信，就会发生冲突。

修复很容易。[Bill]讨论了如何通过添加上面看到的一对限流电阻来确定连接的优先级。这有助于确保不会发生损坏，并且 FTDI 芯片将优先使用。现在，外部硬件将不会阻止 FTDI 芯片通过引导装载程序进行访问和编程。本教程面向那些从基于 Arduino 的原型中开发自己的电路板的人，但它也适用于任何需要多条连接到一组 UART 引脚的情况。
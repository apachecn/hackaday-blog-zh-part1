# 蓝牙温度模块

> 原文：<https://hackaday.com/2010/12/10/bluetooth-temperature-module/>

![](img/97b56cbf37d64cefce0a23369b61e299.png "bluetooth-thermometer")

想要知道外面的温度，[Jamie Maloway]建造了自己的[温度传感器，可以通过蓝牙设备](https://sites.google.com/site/jamiemaloway//projects/bluetooth-thermometer)读取。让我们从右到左浏览一下上面的硬件。有一个线性稳压器，带有两个过滤帽和一个接线板，可以连接 9V 电池或其他电源。接下来是一个 8 MHz 晶振及其电容，顶部是一个编程接头，底部是一个我们都很熟悉的单线温度 IC ds18b 20。这两个都连接到驱动系统的 8 引脚 PIC 12F675，并使用 Sure Electronics 的蓝牙模块进行传输。因为这是使用串行协议和传输 ASCII 数据，所以可以使用自动脚本或简单地使用终端程序来读取。

现在，谁将是第一个摆脱电池并通过电感切断电源的人？
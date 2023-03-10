# 学习使用 IAR 调试 Msp430 芯片

> 原文：<https://hackaday.com/2011/02/15/learn-to-debug-msp430-chips-using-iar/>

![](img/fc0a8752c922702fc276a51186382d51.png "msp430-debugging")

如果你还没有调试过微控制器程序，[Kphlight]贴出了一个调试 MSP 430 芯片的后续指南。您可以在上面看到，他正在使用 TI Launchpad，并选择了免费(但代码有限)的 IAR Embedded Workbench，这是 TI 为该套件提供的 IDE 之一。这个例子用五个发光二极管和一个电阻构建了一个番茄定时器。您将把代码闪存到芯片中，逐步执行固件的每一行，并学习如何在代码执行期间操作寄存器数据。

对于门外汉来说，这是一本很好的入门书，我们希望看到像 DDD 和 GDB 那样使用开源工具的人。如果你真的写了一个，别忘了[给我们发一个关于它的提示](http://hackaday.com/contact-hack-a-day/)。如果你想用这个硬件[试试开源，看看我们自己的教程](http://hackaday.com/2010/08/11/how-to-launchpad-programming-with-linux/)。
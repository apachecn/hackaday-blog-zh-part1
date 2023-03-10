# 为在线调试工具做准备

> 原文：<https://hackaday.com/2011/08/01/making-the-case-for-in-circuit-debugging-tools/>

![in_circuit_debugging_of_pic_microcontrollers](img/b99c0df7daec39847937de0cf26b8077.png "in_circuit_debugging_of_pic_microcontrollers")

如果你在市场上寻找 PIC 微控制器编程器，你可能会考虑带在线调试器(ICD)的型号。[Rajendra]整理了一个很棒的关于调试 PIC 固件时使用 ICD 的教程，这为拥有一个很有说服力的理由。

在他的教程中，他碰巧使用了 MikroElektronika PICflash2，但他说，如果你对这种特殊型号不感兴趣，还有很多其他的 ICD。PICflash2 不仅可以作为 ICD，而且顾名思义，它还可以作为 ICSP。

[Rajendra]使用一些简单的代码带领我们完成了一个简短的调试会话，这些代码从 LM34DZ 温度传感器读取数据，并在 LCD 屏幕上显示结果。虽然他实际上不是在寻找 bug，但他确实展示了一次一条语句地遍历 PIC 代码是多么容易，在这个过程中评估变量和寄存器。

[Rajendra]确实指出，在运行时使用 ICD 确实会占用一些 I/O 引脚，从而稍微限制了您的资源。我们认为，如果您不一定需要每一个可用的引脚，那么能够在代码运行时进行调试是一个非常合理的权衡。
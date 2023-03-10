# AVR8 软处理器的 VHDL 仿真

> 原文：<https://hackaday.com/2011/04/07/simulating-vhdl-of-an-avr8-soft-processor/>

![](img/24aca00fc76b1ff9755132b1e408ed01.png "papilio-soft-processor-mapping")

好了，现在我们开始觉得有点像[爱丽丝]。本教程向你展示如何模拟 VHDL 代码。该代码旨在 FPGA 上运行，包括 AVR 8 位微控制器内核的纯软件版本。本质上，您将模拟模拟 AVR 硬件的 VHDL 代码。把你的思想放在那上面！

该代码旨在运行在 [Papilio 现场可编程门阵列开发板](http://papilio.cc/)上。大约一年前，我们看到了运行 AVR8 内核的[早期版本的主板](http://hackaday.com/2010/04/08/arduino-implemented-on-an-fpga/)。但是，您不需要任何硬件来跟随并自己重新创建这个模拟。这可能是在购买第一个硬件之前尝试 FPGA 编程的好方法。五个不同的截屏带您了解获取 AVR8 代码的过程，使用经过修改的 Arduino IDE，设置 Xilinx ISE 的免费版本来运行仿真，然后释放它并解释仿真器在另一端输出的数据。
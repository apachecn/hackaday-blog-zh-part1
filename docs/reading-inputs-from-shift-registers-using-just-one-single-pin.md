# 仅使用一个引脚从移位寄存器读取输入

> 原文：<https://hackaday.com/2011/11/23/reading-inputs-from-shift-registers-using-just-one-single-pin/>

![](img/e9dce634cfff30d9856774b12b3f2e3c.png "single-pin-shift-register-input")

这里有一篇关于[使用少于三个引脚](http://www.openmusiclabs.com/learning/digital/input-matrix-scanning/hacks/)从移位寄存器读取数据的有趣文章。74HC165 移位寄存器是向微控制器添加输入的常用选择。它们有一个并行输入寄存器，可以使用锁存器读取，然后通过数据和时钟引脚移入微控制器。对于那些计数，这是三个引脚通常与驱动这些设备。

这个黑客首先去掉了插销。添加一个精心调整的 RC 电路(电容由时钟引脚充电，然后电阻让电容缓慢放电)意味着器件不会锁存，直到时钟停止切换。这种技术将控制降至仅两个引脚(数据和时钟)。通过这种方法，您仍然可以使用硬件 SPI 来读取数据。除了微控制器读取数据而不是写入数据之外，它与使用 SPI 驱动 595 个移位寄存器的[相同。](http://hackaday.com/2011/11/05/controlling-shift-registers-via-spi/)

但是等等，还有呢！上图实际上显示了仅用一个引脚读取该移位寄存器的方法。请注意，时钟和数据引脚现在只连接到一个微控制器引脚。数据引脚增加了一个电阻，使电流足够低，不会与来自微控制器的时钟信号竞争。在时钟脉冲之间，微控制器在每个周期从输出切换到输入，以读取数据引脚。试试看，这是一个有趣的实验！
# Lxardoscope 是一个 Linux+Arduino 示波器

> 原文：<https://hackaday.com/2011/09/20/lxardoscope-is-a-linuxarduino-oscilloscope/>

![](img/a44428edc853277788a3f1cd939806f7.png "arduino-oscilloscope")

[Privatier]来信让我们了解 lxardoscope，他的项目可以让你使用 Arduino 作为基于 Linux 的示波器显示的硬件输入。这种实现提供了两个通道，每个通道每秒大约 3000 个样本。他推销了一些 GUI 选项，比如每个分区 2mV 到 10V 之间的垂直分辨率。这部分有点难住我们了，因为我们不知道如何利用随附的原理图测量 10V(或更高)的电压。但是你的理解能力可能超过我们，所以你自己看看吧。

他使用 Arduino Uno 进行测试。但是为了解决他在其他基于 USB 的解决方案中遇到的一些问题，他实现了一个串行端口连接。你需要在将代码刷新到 Arduino 板上之后，从 Arduino 板上移除 ATmega 芯片，然后围绕它建立一个电路，其中包括一个电源，其中-2.5V 是地，2.5V 是 VCC。总而言之，你需要一个 16 Mhz 晶振、HEF4069 hex 反相器、ATmega8 系列微控制器和一些无源元件来在试验板上实现这一功能。
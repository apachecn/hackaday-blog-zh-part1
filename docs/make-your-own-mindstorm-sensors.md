# 制作你自己的思维风暴传感器

> 原文：<https://hackaday.com/2010/08/06/make-your-own-mindstorm-sensors/>

大约一个月前，斯图尔特·艾伦获得了一个思维风暴工具包，他已经为它建造了自己的传感器。他想要一个比股票传感器测量范围更窄、更精确的测距仪。Mindstorm 可以选择通过 I2C 总线与传感器通信。[Stewart]设置 ATtiny45 作为总线上的从机，通过使用查找表方便距离电压的模拟测量，并通过 NXT 模块处理数据传输。他的测试设置如上图所示，一个 AVR Dragon 用于编写 tiny45，一个 Bus Pirate 用于在开发过程中嗅探 I2C 数据。该传感器在他订购的专业制作的 PCB 上看起来很棒，但需要一个简单的驱动程序，该驱动程序是[Stewart]精心设计的，用于 leJOS，即我们之前见过的的[替代](http://hackaday.com/2010/08/02/android-controlling-mindstorms-nxt/) [Mindstorm](http://hackaday.com/2010/08/02/android-controlling-mindstorms-nxt/) [固件。](http://hackaday.com/2010/08/02/android-controlling-mindstorms-nxt/)
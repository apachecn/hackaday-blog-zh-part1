# Versaloon 移植到 STM8 和 STM32 发现板

> 原文：<https://hackaday.com/2011/02/06/versaloon-ported-to-stm8-and-stm32-discovery-boards/>

![](img/ac14d9916ee9d1c5f5e24685d1bb2c6b.png "versaloon-on-stm8")

[Bingo]做了一些工作[为 STM8 和 STM32 发现板](http://www.avrfreaks.net/index.php?name=PNphpBB2&file=viewtopic&t=101700&start=0&postdays=0&postorder=asc&highlight=)移植 Versaloon。Versaloon 是一个多架构程序员，我们几周前在见过[。它的中心是一个 STM32 微处理器，这大大简化了使用](http://hackaday.com/2010/12/25/versaloon-can-program-hardware-from-several-manufacturers/)[两个](http://hackaday.com/2010/10/12/arm-prototyping-on-the-cheap-with-stm32-discovery/) [发现板](http://hackaday.com/2009/11/23/stm8s-discovery-microcontrollers-reach-a-new-low/)的必要工作。向电路板刷新固件会破坏 ST-link 固件,[Bingo]不知道恢复的方法，所以要小心。这种黑客技术仍然非常新鲜，但迄今为止，看起来 vsprog 和 OpenOCD 在新硬件上工作得很好。
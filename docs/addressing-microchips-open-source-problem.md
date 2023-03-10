# 解决微芯片的开源问题

> 原文：<https://hackaday.com/2011/08/31/addressing-microchips-open-source-problem/>

![microchip_call_for_open_source](img/c9844a252959efb3d7cd7fec74054d02.png "microchip_call_for_open_source")

Hackaday 的校友和危险原型的所有者[Ian Lesnet] [最近写了一篇社论文章](http://dangerousprototypes.com/2011/08/30/editorial-our-friend-microchip-and-open-source/),指出 Microchip 对开源的一些不太友好的态度。

[Ian]和他的公司在他们的项目中广泛使用 PIC 微控制器，他们对他们的产品总体评价很高。他的抱怨(认为你也应该有)是关于微芯片的开源方法。

你看，Microchip 投资了 Arduino IDE，并发布了 chipKIT，一个 32 位 Arduino 兼容开发板，以及与开源社区“友好相处”的承诺。根据[Ian]的说法，问题在于尽管 Microchip 的编译器是基于 GCC 的，但它们“锁住了一些特殊的调料”，这意味着 chipKIT 工具链的某些部分是不开放的。社区中的许多人，包括[Ian]基于 Atmel 开源项目的成功对 chipKIT 寄予厚望，但许多东西仍然被封闭的许可证所锁定。

这种对开源不友好态度的一个例子可以在 Digilent 最近发布的 network shield 中看到。它支持 chipKIT MEGA 的以太网和 USB 功能，但 TCP/IP 和 USB 堆栈是完全封闭的源代码。Digilent 努力争取为主板发布开放驱动的能力，但这是一场他们最终输掉的战斗。这种行为给经验丰富的开源产品开发人员(如危险的原型)以及好奇的初学者设置了障碍，这就是为什么[Ian]强调这些问题的原因。

[Ian]敦促 Microchip 向他们正在开发的社区回馈一些有意义的东西，这一结果只能通过大声疾呼来实现。一定要看看他的社论，如果读完之后你有兴趣让别人听到你的声音，给 Microchip 写一行，让他们知道他们与开源社区的单向关系是你希望看到改变的。
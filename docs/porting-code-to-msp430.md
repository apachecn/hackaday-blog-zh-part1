# 将代码移植到 MSP430

> 原文：<https://hackaday.com/2010/08/13/porting-code-to-msp430/>

![](img/3f6336e632a3dab16aff929fff2ec811.png "porting-avr-to-msp430")

我花了一点时间研究为 AVR 编写的移植代码，以便在 MSP430 架构上运行它。这比你想象的要简单，大部分都是微小的差异，就像启用上拉电阻的额外步骤。但是，要从使用 EEPROM 过渡到使用 EEPROM，还有很多东西需要学习。

因为 TI 芯片没有 EEPROM，所以你需要使用 Info Flash，我在顶部链接的文章中详细介绍了这个主题。该闪存必须在写入前擦除，因为写入操作只能将高位变为低位，而不是相反。擦除操作会清除整个 64 kB 段，而不仅仅是您想要写入的字节。这是不同的，但可管理的。

哦，如果你想知道，我移植了我为[车库门编码入口项目](http://hackaday.com/2010/08/02/doorbell-combo-lock-can-open-your-garage-door/)写的代码。
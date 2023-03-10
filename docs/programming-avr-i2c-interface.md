# AVR I2C 接口编程

> 原文：<https://hackaday.com/2012/01/09/programming-avr-i2c-interface/>

正如你们许多人所知道的，I ² C 是许多外围设备与微控制器之间的简单串行接口，但对于不习惯它的人来说，它很快就会变得令人困惑。正因为如此，I ² C 教程总是受欢迎的，这个由【嵌入式】编写的新教程在[如何将 I](http://www.embedds.com/programming-avr-i2c-interface/) [² C 与 AVR](http://www.embedds.com/programming-avr-i2c-interface/) 和 24C16 字节 EEPROM 一起使用方面做得非常好。

教程的前半部分清楚地解释了 I ² C 是如何工作的，包括它的信号结构、寻址和数据包。然后它移动到 AVR 领域，展示如何在 AtMega 微控制器中设置 I ² C。作者使用了对我们大多数人来说相当标准的 Arduino，用 AVR C 编写的软件和一个漂亮的小 GUI 编程应用程序，它简化了直接处理 AVRDude 的麻烦。

从旋转寄存器到从 EEPROM 向 PC 上的串行终端读写位的完整应用程序，都有大量的代码样本。
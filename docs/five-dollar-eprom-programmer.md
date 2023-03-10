# 五美元 Eprom 编程器

> 原文：<https://hackaday.com/2006/11/08/five-dollar-eprom-programmer/>

几年前，我花了整整一周的时间给一个相当复杂的 EPROM 编程器接线，这样我就可以为我的吉普电喷系统烧一个 PROM。今天我偶然发现了[这个 5 美元的版本](http://www.miranda.org/~jkominek/hardware/eeprom/)。Jay Kominek 建造的他使用移位寄存器来处理寻址和 IO 线，所有这些都由并行端口直接驱动。没有办法避开必须连接的引脚数量，但是[原理图](http://www.miranda.org/~jkominek/hardware/eeprom/eepromprog.png)本身非常简单。
【顺便说一句，街机用品店是廉价 UV erase EPROMS 的绝佳来源。]

[更新:我忘记了写 UV EPROMS vs EEPROMS 所需的电压变化(如果我记得的话，是 3 vs 5)。稍加修改，您当然也可以将它用于 EPROMS。]

*   [永久链接](http://www.miranda.org/~jkominek/hardware/eeprom/)
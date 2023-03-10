# “计数盒”也可以让小孩子不用计算器

> 原文：<https://hackaday.com/2011/08/25/counting-box-also-saves-calculators-from-small-children/>

![](img/71f0e89ff03d84917287e2c493922f88.png "box")

[Nathan]的儿子非常喜欢数字和计数，他最喜欢做的事情之一就是一遍又一遍地在计算器上加 1。作为一个令人敬畏的父亲，[内森]为他的儿子[做了一个计数盒](http://www.hahabird.com/2011/08/the-counting-box/)，里面有一个 10 位数的旋转开关和两个用于加减的街机按钮。

该项目的一个目标是让计数盒在断电时保留显示器的记忆。最简单的方法是将显示数据写入 ATmega 的 EEPROM。这种 EEPROM 只额定 100，000 个写周期(尽管实际上[要高得多](http://hackaday.com/2011/05/16/destroying-an-arduinos-eeprom/))，所以【Nathan】在过度设计的小痉挛中包括了一个 24LC256。所有的电子设备都布置在 perf 板上，箱子由[波诺科](http://www.ponoko.com/)激光切割的竹子制成。表壳本身的质量相当出色——我们对其光洁度和磁性电池检修门印象深刻。

根据经验，我们知道玩 HP-15C 最终会导致计算器坏掉，我们的任天堂被拿走。我们真的为(内森)的儿子感到高兴，希望我们在他这个年龄也有自己的计数箱。
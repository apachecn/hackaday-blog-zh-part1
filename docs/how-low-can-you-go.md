# 你能走多低？

> 原文：<https://hackaday.com/2011/04/09/how-low-can-you-go/>

![](img/e5f638121b3c47866c9379156b63d15d.png "msp430 clock(Custom)")

这正是[Kenneth Finnegan]在他对基于 MSP430 的低功耗电路的最初调查中发现的。他能够让一个价值 20F 的电容器运行 10 周以上。尽管其本身的优点令人印象深刻，但许多人发表评论，质疑类似的结果是否会出现在功能比 LCD 上简单增加一位数更高级的电路中。好了，伙计们，[Kenneth]通过这款[超低功耗液晶时钟](http://kennethfinnegan.blogspot.com/2011/02/low-power-lcd-clock.html)再次提高了它的性能。

创建这个时钟的最大挑战是找到一种有效的方法来驱动 MSP430G2231 芯片上有限数量的引脚中的 28 个 LCD 段，同时仍然有用于按钮输入的开放引脚。ICM7211 LCD 驱动器绝对适合这项任务(通过一些巧妙的修改来驱动辅助字符，如中间的冒号)，但需要 8 个引脚来驱动它。一个标准的 74HC595 锁存移位寄存器将这个数字降低到一个更易于管理的 3 引脚总数。

完成后，总电流消耗约为 12μA——对于所用的 3V 200mAh CR2032 纽扣电池大约两年半的运行时间来说，这已经足够低了。如果这是真的，一组标准的 AA 碱性电池串联起来，就像在许多时钟中发现的那样，可以运行这个小电路几十年。

休息后留下来观看一个短视频，并确保查看[原始博客条目](http://kennethfinnegan.blogspot.com/2011/02/low-power-lcd-clock.html)中的原理图和完整源代码！

[https://www.youtube.com/embed/dV1LWnB6J4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dV1LWnB6J4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# 省电的 MSP430 迷你闹钟

> 原文：<https://hackaday.com/2011/04/04/power-sipping-msp430-mini-alarm-clock/>

![msp430_alarmclock](img/385cc4c7675e280d402f13674f129e7b.png "msp430_alarmclock")

[Markus]有一台 TI MSP430，放在他不久前购买的 LaunchPad 套件中。他不知道该拿它做什么，但最终决定用它来做一个很棒的微型闹钟。

他添加了一个移位寄存器来驱动他的 7 段 LCD 显示器，在这个过程中使用了 MSP430 的两个输出引脚。另外四个引脚连接到显示器的阴极，而其余两个引脚连接到记录用户输入的按钮。

他把时钟的逻辑和闹钟的曲调塞进了芯片不足 2KB 的存储空间，几乎占据了所有的空间，直到最后一个可用的字节。这个时钟相当省电，待机状态下仅用 2 A。根据[Markus']的计算，这应该能够让时钟使用一组电池超过 10 年。

虽然这不是我们见过的第一个 MSP430 时钟，但它肯定是最小和最简单的。留下来看看他的时钟运行的快速视频。

[https://www.youtube.com/embed/a6q4vUfasKw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/a6q4vUfasKw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
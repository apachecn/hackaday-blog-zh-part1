# 完全用汇编编写的 64 位操作系统

> 原文：<https://hackaday.com/2011/05/27/64-bit-os-written-entirely-in-assembly/>

![](img/86572c5360b597f07027568d0f576985.png "baremetal")

Return Infinity 的工作人员刚刚发布了他们的新版本裸机操作系统，这是一个完全用汇编语言编写的 64 位操作系统。

BareMetal 项目的目标包括一个[精简引导加载程序](http://www.returninfinity.com/pure64.html)和一个[集群计算平台](http://www.returninfinity.com/baremetalnode.html)，目的是摆脱由 C/C++和 Java 等高级语言生成的低效混乱的机器代码。通过汇编编写操作系统，运行速度提高了，而且每个时钟周期的开销都很小。

Return Infinity 表示，理想的应用是高性能和嵌入式计算。我们可以看到为什么这对真正快速的嵌入式计算非常好——有对网络、声音、磁盘访问和项目可能需要的其他一切的系统调用。还有非常小的系统需求——整个操作系统只有 16384 字节——适合非常小、非常强大的计算机。

对于计算密集型项目，我们认为这可能是不足的 AVR、PIC 或 Propeller 与成熟的 linux 发行版之间的一座桥梁。只有一些关于实施的问题——我们感觉就像刚刚得到了一个工具，我们甚至不知道何时使用。任何黑客读者都知道如何使用一个“裸机”操作系统吗？确切地说，什么需要 64 位，它将在什么硬件上运行？

查看 Return Infinity 团队在跳跃之后在他们的裸机节点操作系统上计算质数的情况。

[https://www.youtube.com/embed/ccLef8GLl6g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ccLef8GLl6g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
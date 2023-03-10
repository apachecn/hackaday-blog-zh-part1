# 微控制器虚拟机让你在 AVR 芯片上运行 Python

> 原文：<https://hackaday.com/2011/08/31/virtual-machine-for-microcontrollers-lets-you-run-python-on-avr-chips/>

![](img/0320be435016bfd0228862b0b7c1845b.png "avr-vm-code")

[Clifford Wolf]来信让我们了解他最近完成的一个名为 EmbedVM 的项目。这是 AVR 微控制器的虚拟机。这个包的开销相对较小，大约占用 3kB 的程序内存。VM 每秒可以执行 74，000 条指令，并且与微控制器异步运行。正如[Clifford]在休息后的视频中演示的那样，这可以方便地预加载命令，以防止在 VM 处理器负载繁重时速度变慢。

上图中的片段是一个用类似 C 语言的 VM 代码编写的示例程序，它将在扬声器上播放一些[里克·阿斯特利]的音乐。该代码可以从 RAM、EEPROM 甚至 SD 卡等外部存储器中运行。最近有一个补充的编译器项目，它甚至将 Python 代码编译成 VM 字节码。对于那些有一点 Python 经验的人来说，这是一个非常好的抽象工具，可以使廉价的基于微控制器的设计易于编程。

如果你不认识这个名字，【Clifford Wolf】也是 OpenSCAD 的作者，这是一个[相当受 3D 打印](http://hackaday.com/2011/06/03/onshoulderstv-knows-how-to-use-openscad/)欢迎的工具。

[https://www.youtube.com/embed/CVUh5eVN8gU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CVUh5eVN8gU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[https://www.youtube.com/embed/CaRRwuWSbMs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CaRRwuWSbMs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
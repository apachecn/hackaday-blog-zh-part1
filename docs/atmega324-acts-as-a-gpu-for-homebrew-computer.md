# ATmega324 充当自制计算机的 GPU

> 原文：<https://hackaday.com/2012/03/20/atmega324-acts-as-a-gpu-for-homebrew-computer/>

![](img/6e02152f1767cdb630200755d32b0a91.png "atmega324-vga-gpu")

[奎因·邓基的]自制计算机项目正在向另一个进化梯级前进。她需要一个更加通用的用户界面，这从数据输出开始。到目前为止，一组 7 段数字已被用作显示寄存器值的方式。但她目前的工作是针对[给系统](http://quinndunki.com/blondihacks/?p=955)增加 VGA 输出。

她从证明协议选择的合理性开始写报告。虽然复合视频更容易启动和运行(我们在许多 AVR 项目中看到它)【Quinn】没有显示复合视频的屏幕。但是也有很多关于 VGA 信号产生的信息。她深入研究了细节，甚至在 Lucid Science 找到了[一个很好的基于 AVR 的例子。](http://www.lucidscience.com/pro-vga%20video%20generator-1.aspx)

上面看到的版本使用的是 40 针 ATmega324。对于她所举的例子来说，这比需要的要大得多，但是将来她计划添加视频内存，并且很高兴拥有所有这些额外的 I/O 引脚。说到视频同步，时间就是一切。她用汇编语言编写了驱动显示器的代码。通过这种方式，她能够查找每个命令使用的周期，以确保循环以近乎完美的时序运行。
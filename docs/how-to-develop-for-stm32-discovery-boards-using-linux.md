# 如何使用 Linux 开发 STM32 发现板

> 原文：<https://hackaday.com/2011/10/17/how-to-develop-for-stm32-discovery-boards-using-linux/>

一些艰苦的工作使得使用 Linux 系统为 STM32 开发板开发成为可能。该板拥有一个 ARM Cortex-M3 处理器，可以通过侧面的迷你 USB 端口进行编程。但是该公司只支持通过他们的 IDE 进行开发，这些 IDE 不能在 Linux 上运行。stlink 项目旨在解决这一问题，提供一个工具链，并使通过 USB 连接刷新微控制器成为可能。

上面链接的 github 项目还包括[一个帮助你入门的教程](https://github.com/texane/stlink/blob/master/doc/tutorial/tutorial.pdf?raw=true) (pdf)。除了编译软件包的演练之外，它还包括一个简单的 blink 程序，您可以用它来测试您的硬件。 [GDB](http://www.gnu.org/s/gdb/) ，大家熟悉的开源调试器，用来闪存芯片。这是一个基本的教程，所以如果你最终发布了你在探索板[上使用这个工具链的经历，我们很乐意听到它](http://hackaday.com/contact-hack-a-day/)。

[谢谢德州人]
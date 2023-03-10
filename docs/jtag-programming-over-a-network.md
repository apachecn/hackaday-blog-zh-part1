# 网络上的 JTAG 编程

> 原文：<https://hackaday.com/2010/06/01/jtag-programming-over-a-network/>

![](img/eb18d35186d3642f9e4e9dd8a19b9cb3.png "router-jtag-programmer")

[Matt Evans]遇到了由于并行端口消失而导致的常见编程问题。多年来，他在处理 FPGAs 时一直使用 JTAG 并行电缆，但最近意识到他不再拥有任何具有该接口的机器。他没有花 50 美元买一个 USB 编程器，而是用一个旧路由器的编程接口。他正在做的事情是[使用 Linux 开发](http://hackaday.com/2009/09/22/introduction-to-ftdi-bitbang-mode/)。在这种情况下，它是一个运行 Linux 版本的路由器，这使得他的设置对互联网友好，但这可以在任何具有足够可用 I/O 连接到您正在编程的设备的 Linux 设备上以相同的基本方式完成。
# MCP2200 USB 转串行芯片被黑为您服务

> 原文：<https://hackaday.com/2011/01/18/mcp2200-usb-to-serial-chip-hacked-to-do-your-bidding/>

![](img/498ba1e542c4c548ec1aa48af4f38bcf.png "mcp2200-hacking")

Mircrochip 有一个新的 USB 到串行转换器，称为 MCP2200。[Sjaak]怀疑它可能是由现有的 20 引脚 PIC 制成的，并发现用 PICKIT3 读取设备签名显示该芯片是 18F14K50。最有可能的是，这是运行微芯片的 USB 堆栈，但很难说，因为芯片是代码保护，读回全零。所以[他开始写一些替换固件](http://dangerousprototypes.com/2011/01/18/hack-open-source-usb-stack-on-mcp2200/)，它将提供相同的功能，并让你访问芯片的其余功能。

一路上有一些减速带。第一个是微芯片的 USB 堆栈许可不允许你开源你的固件。没关系，似乎已经有一个 USB 堆栈可以移植，没有这个限制。该计划的第二个问题是，Sjaak 的代码没有像 V-USB 那样为 AVR 芯片提供 VID/PID 对。但这并没有减少通过回显接收到的字符使设备工作的成就。替换固件将提供全面的 USB 转串行支持。

[谢谢克里斯]
# AVR Gameboy 转储器

> 原文：<https://hackaday.com/2011/05/09/avr-gameboy-dumper/>

![](img/6f812504086f65d8f6d6ebd7a4020088.png "DSC03314")

[凯旺]一直在努力工作，latley 开发了一个 [Gameboy cart dumper](http://www.rival-corp.com/2011/05/08/usb-gameboy-cartridge-dumper/) ，虽然还有一些细节需要处理，但这个设备运行良好，可以建立他的收藏。运行 AVR (mega 16？)和一个用于 usb 连接的 FTDI 芯片，该设备可以读取游戏的 ROM 和 SRAM，如果你想将保存的游戏加载到真正的购物车上，还可以写入 SRAM。

在电脑方面，该设备使用通用的 HID 协议进行通信，速度可以从 16Kbps(目前)到 64Kbps 左右(很快)。python 脚本目前处理数据流，但对于我们其他人来说，有一个 GUI 版本正在为*x 和 windows 工作。

还在工程中的是一个重新设计的 PCB。有几个问题，你可以看到跳线，虽然我们认为它增加了一点特色，这将是一个很好的解决未来。
# 零件:拆箱总线盗版

> 原文：<https://hackaday.com/2009/07/20/parts-unboxing-the-bus-pirate/>

![bp-unbox-3](img/fb36934c7869e199de5f9a3e3d6d9c86.png "bp-unbox-3")

几个月来，我们一直使用我们的[总线盗版通用串行接口工具](http://www.buspirate.com)来演示[电子零件](http://hackaday.com/category/parts/)，所以总线盗版获得它自己的零件帖子是唯一合适的。我们最近有一个[巴士海盗预购](http://hackaday.com/2009/06/25/bus-pirate-preorders-open/)，今天我们收到了来自 [Seeed 工作室](http://www.seeedstudio.com/depot/)的预生产巴士海盗原型。这个原型是在 [preorder 1 开始发货](http://hackaday.com/2009/07/16/bus-pirate-preorder-1-ships/)的前几天寄出的，所以那些包裹应该随时会到达。

跟随我们打开原型 Bus Pirate 的包装，并将其连接到调试器，以确定该主板附带的 [PIC24FJ64GA002-I/SO](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en026374) 版本。用这个帖子分享一下自己的公交盗版拆箱经历。休息后的图片和讨论。

![bp-unbox-1](img/86732bcf2f9b0ecd1f942964aefef3e3.png "bp-unbox-1")

大多数总线盗版者会将[装在一个填充的信封里](http://hackaday.com/wp-content/uploads/2009/07/ready-envelope-470.jpg?w=470&h=312) (JPG)，但我们的是装在一个盒子里，里面有一些用于未来项目的 PCB 和一个 AVR 编程器。

![bp-unbox-2](img/60d62b97a1c9f0a7e44f5d4553ab22fe.png "bp-unbox-2")

在盒子内部，总线盗版由一个静电耗散袋保护。总线盗版引脚头粘在泡沫中，以保护包装。

![bp-unbox-5](img/7d0ad82ed4b6776bd115eee90f795cde.png "bp-unbox-5")

我们进行了一系列功能测试，包括 USB、用户终端、协议库、电源和上拉电阻。一切都通过了我们的测试。

接下来，我们使用了一个微芯片 ICD2 调试器/编程器，在使用引导加载程序进行升级/降级测试之前，对固件进行了备份。

> 连接到 MPLAB ICD 2
> …已连接
> 设置 Vdd 源到目标
> **找到目标设备 PIC24FJ64GA002，revision = Rev 0x 3042**
> …读取 ICD 产品 ID
> 运行 ICD 自检
> …通过
> MPLAB ICD 2 准备下一步操作

我们以前的所有总线盗版版本都是使用 PIC 24FJ64GA002 的版本 0x3003 (A3)构建的。版本 A3 有一些问题，被称为[勘误表](http://ww1.microchip.com/downloads/en/DeviceDoc/80470a.pdf) (PDF)，其中之一是[片状硬件 I2C 模块](http://www.google.com/codesearch/url?ct=ext&url=http://forum.microchip.com/tm.aspx%3Fm%3D271183%26mpage%3D1&usg=AFQjCNFvedVtagkyXzTS-vmSKIk3OE0eiw)。这些芯片没有“缺陷”，它们只是像任何复杂的集成电路一样有一些怪癖。总线盗版固件使用软件技术来解决这些问题。大多数台式计算机处理器都经历类似的步进过程。

我们的总线盗版似乎有一个 B4 修订版图片(0x3042)，纠正了一些，但不是全部，从 A3 的勘误表。这并不能保证每个巴士盗版将有一个 B4 的图片，预订 1 和 2 都来自多个国际供应商。此外，拥有 B4 芯片不会带来立竿见影的好处，有人将不得不编写利用硬件优势的软件。下一次固件更新将在用户终端中打印 PIC 版本，如果您担心，请检查[夜间编译](http://code.google.com/p/the-bus-pirate/source/browse/#svn/trunk/firmware/v0h-nightly)。

PIC 勘误表中提到了版本 B5。其中一些可能会进入预购 2 板。

![bp-unbox-0](img/b6ed3daecf541cf00b6a21a4a782c002.png "bp-unbox-0")

现在你有了你的巴士海盗，你会怎么处理它？我们提供了一系列[零件演示](http://hackaday.com/the-bus-pirate-universal-serial-interface/)来帮助您入门。

请留下您拆箱体验的评论，以及您计划连接的设备。
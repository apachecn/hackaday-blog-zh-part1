# 总线盗版固件更新(v.0c)，JTAG 和更多

> 原文：<https://hackaday.com/2008/12/01/bus-pirate-firmware-update-v0c-jtag-and-more/>

![stat](img/6f6c4a3b756b6219238b534a4242e35b.png "stat")

**下载:** [buspirate.v0c.zip](http://blog.mahalo.com/hackaday/howto/buspirate.v0c.zip)

几周前，我们写了关于我们的[总线盗版通用串行接口工具](http://hackaday.com/2008/11/19/how-to-the-bus-pirate-universal-serial-interface/)。我们利用最近的假期增加了一些新功能，比如 JTAG 编程器、宏、频率测量等等。一个主要的代码重组使一切更容易阅读和更新。

请查看下面的新功能演示。我们正在编制路线图和愿望清单，请在评论中分享您的想法。你也可以看到我们如何使用总线盗版[读取智能卡](http://hackaday.com/2008/11/25/how-to-read-a-fedex-kinkos-smart-card-sle4442/)和[试驾 I2C 晶体振荡器](http://hackaday.com/2008/11/28/parts-133mhz-162khz-programmable-oscillator-ds1077/)。

**新协议** 

> I2C > m**<–设置模式**
> 1。HiZ**<–高阻抗引脚(安全模式)**
> 2。单线**<–未准备好发布**
> 3。UART
> 4。I2C
> 5。SPI
> 6。JTAG**<–接口和编程器**
> 7。拉线 2 线
> 8。拉线
> 模式> 1
> 900 模式设定
> HiZ >

这个固件版本列出了三个新协议。

Hi-Z 使所有引脚[高阻抗](http://en.wikipedia.org/wiki/High_impedance)/输入，这是一种不会损坏附属电路的安全状态。为了安全起见，巴士海盗现在以这种模式启动。

1-Wire 已列出，但我们无法将其包括在此版本中，因为我们仍然没有任何器件可以用我们的库进行测试。目前这只是一个占位符，但一旦我们得到要测试的单线器件，就会添加它。

我们编写了一个简化的 JTAG 接口，包括一个 XSVF 播放器，用于编程 JTAG 设备链。

* *我们包括了一个硬件 I2C 库，但是根据设备勘误表[，在 24FJ64GA002 rev3 I2C 模块](http://forum.microchip.com/tm.aspx?m=271183&mpage=1)中有一个 bug。这将适用于不同的芯片(例如 28 针 dsPIC33)。

*连接表*

| **销** | **单线** | **【I2C *】** | *** *** | **RS232** | **JTAG** |
| **B9** | 国家药品监督管理局 | SDA | MOSI | – | trandport driver interface 传输驱动程序接口 |
| **B8** | – | SCL | CLK | – | TCK |
| **B7** | – | – | 味噌 | RX | TDO |
| **B6** | – | – | CS | TX | （同 terms）合同或协议书的条件 |
| **B5** | 去吧 | au | au | au | 去吧 |
| **地面** | GND | GND | GND | GND | GND |

*也是原始的 2 线。* *也是原始的 3 线。

新模式连接到总线盗版，如下表所示。

**新功能和设置**

*频率测量*

> HiZ > F**<–做个频率计数**
> 9xx FREQ 计数上 AUX:22199552hz(22 MHz)
> HiZ>

正如在 [DS1077 演示](http://hackaday.com/2008/11/28/parts-133mhz-162khz-programmable-oscillator-ds1077/)中看到的，我们给总线盗版的 AUX 引脚添加了一个频率计数器。f '测量频率，最大值约为 50 兆赫。

*分配腋窝控制*

> hiz > c**<–菜单 c**
> 到针脚
> 1。au(默认)
> 2 .CS/TMS
> 模式>**<—设置为控制模式**
> 9xx AUX:默认设置(AUX PIN)
> HiZ >

有时我们需要手动控制片选(CS) /JTAG 状态机(TMS)引脚。c '在辅助引脚和片选引脚之间切换引脚控制。

*设定终端速度*

> HiZ > b**<–菜单 b**
> 设置串口速度:(bps)
> 1。300
> …
> 9。115200
> 速度> 9

 **' b '调整 PC 端串口速度。

**宏**

新增加的语法“(#)”触发协议相关的宏。

> JTAG >(0)**<–宏 0**
> 0。宏菜单
> 1。复位链条
> 2。探针链
> 3。XSVF 播放器
> JTAG >

在任何模式下，使用宏(0)显示可用宏的菜单。

*I2C 地址搜索*

> I2C >(1)**<–扫描 I2C 地址宏**
> xxx 搜索 7bit I2C 地址空间。
> 发现设备在:
> 0xb 0 0x B1**–ds 1077 响应读写地址**I2C>

I2C 图书馆包括一个宏，自动搜索设备的 I2C 地址范围。当你用一个未知的芯片工作时很有帮助。

*Raw2wire 智能卡 ISO 7813-3 ATR*

> raw 2 wire >(1)**<–ATR 和解码宏**
> ISO 7813-3 ATR
> 950 AUX 低电平
> 951 AUX 高电平
> 4xx RAW2WIRE 0x01 时钟滴答
> 950 AUX 低电平
> ISO 7813-3 回复:0x a2 0x 13 0x 10 0x 91**<–ATR 字节**
> 协议:2 线**<–解码 ATR 数据**
> 读取类型:to end

 **宏 1 重置并识别智能卡。关于 ISO7813-3 ATR 的更多信息，请看我们如何使用总线盗版读取智能卡。

**JTAG**

[JTAG](http://www.fpga4fun.com/JTAG.html) 是各种电子设备的调试和编程接口。原始硬件接口可以通过 Bus Pirate 的 raw 3 wire 库来访问，但我们添加了一些功能来使它变得更加容易。

**![jtagstate](img/0fd90e4677af96ccaa3057a090b69a9a.png "jtagstate")**

JTAG 有不同的模式，数据输入做不同的事情。用 JTAG TMS 信号导航模式；有一堆 JTAG 模式叫做状态。巴士海盗的 JTAG 图书馆只是原始的 3 线图书馆，增强以帮助 JTAG 州的变化。

我们只实现了从 JTAG 设备链中获取数据所需的 JTAG 状态:复位、空闲、数据寄存器和指令寄存器。宏(1)发出 JTAG 链复位，并将链初始化为空闲状态。{将 JTAG 链置于数据寄存器模式。[将链置于指令寄存器模式。]或}将链返回到空闲状态。总线盗版有一个内部状态机跟踪器，它足够智能，可以管理链，而无需显式地将链返回到空闲状态；换句话说，你不必关闭你的标签。状态机跟踪器报告每个状态变化，以帮助调试问题。

> JTAG >[0 xfe { rrrr }**<–同[0xfe]{rrrr}**
> xxx JTAGSM:已空闲
> xxx JTAGSM:空闲- >指令寄存器(TMS 延迟一位)
> 610 JTAG 准备写 IR**<–JTAG 链指令寄存器**
> 620 JTAG 写:0 xfe**<–请求 ID**
> xxx JTAGSM:(已写延迟位) IR- >空闲**<–返回空闲**
> xxx JTAGSM: IDLE- >数据寄存器**<–空闲到数据寄存器**
> 611 JTAG 准备读/写 DR
> 630 JTAG 读:0x 93**<–设备 ID**
> 630 JTAG 读:0x40
> 630 JTAG 读:0x60
> 630 JTAG

下面是和一个 [Xilinx XC9572 CPLD](http://www.xilinx.com/products/xc9500xl/index.htm) 的简短互动。我们转到指令寄存器([)，发送设备 ID 请求命令(0xfe)。然后，我们进入数据寄存器({)，读取四个字节(rrrr，或 r:4 简写)，然后返回 idle ( })。

*什么是延迟位写入？*

JTAG 要求在状态改变的同时输入写入指令寄存器的最后一个数据位。由于总线盗版无法预测我们何时会真正改变状态，它会延迟每个字节写入的最后一位，直到发生以下三种情况之一:

*   使用}、]或{命令退出指令寄存器
*   写入另一个字节值
*   读取命令

未决位不是通过按位运算清除的(比如！或者^).在写入最后一个字节之前做这些，或者修改代码。我们还没有实现对数据寄存器的挂起写入，但这可能是需要的。如果你正在写数据寄存器，而不是像我们一样只是读，你可能需要实现这个。

*JTAG 宏*

> JTAG >(1)**<–巨集 1】**
> 【XXX jtgsm:复位
> 【XXX jtgsm:复位】>闲置【JTAG】>

JTAG 宏(1)重置 JTAG 链，然后将其推进到空闲状态。

> JTAG >(2)**<–宏 2**
> xxx JTAG 初始化链
> XXX JTAG sm:RESET
> XXX JTAG sm:RESET->IDLE
> XXX JTAG sm:IDLE->指令寄存器(TMS 延迟一位)
> XXX JTA GSM:IR->IDLE
> XXX JTA GSM:IDLE->数据寄存器
> XXX JTA GSM:DR->IDLE
> XXX JTA GSM:RESET
> XXX JTA GSM:RESET->IDLE
> XXX JTA GSM:IDLE->数据寄存器
> xxx JTAG 链报告:**<–报告开始**
> 0x01 设备【T16

宏(2)重置链，计数设备，并报告所有设备 id。

![xsfv](img/7d4b76836f8a98affc7a7223fefa43d9.png "xsfv")

> JTAG >(3)**<–宏 3**
> 6xx JTAG XSVF 播放器
> xxx XON/XOFF 流控必选**<–必选！**
> xxx 按 z 继续**<–按 z**
> xxx 开始 XSVF 上传**<–上传文件**
> 6×0 XSVF OK**<–结果或错误**
> 您的 PC 在 XOFF 后运球最大 0x05 字节(没问题)
> 6xx 按 z 5 次继续**<–继续**
> JTAG >

Macro 3 是一个 XSVF 播放器/程序员，使用 Xilinx 的代码。XSVF 是 Xilinx (pdf)描述的字节格式 [SVF](http://www.asset-intertech.com/support/svf.html) 、[。XSVF 文件可以用正确的](http://www.xilinx.com/support/documentation/application_notes/xapp058.pdf)[通用 JTAG 定义文件](http://www.xilinx.com/products/design_resources/config_sol/isp_standards_specs.htm)为任何链编译，甚至是非 Xilinx 设备。我们成功地使用了 [Hercules](http://www.hw-group.com/products/hercules/index_en.html) 和 [Tera Term](http://www.ayera.com/teraterm/) 中的*二进制*传输特性向程序员发送 XSVF 文件。

JTAG 有时暂停的时间比 PC 传输一个字节数据的时间还要长，所以我们为 XSVF 播放器实现了 [XON/XOFF 软件流控制](http://en.wikipedia.org/wiki/XON)。在上传 XSVF 文件之前，您的终端必须处于 XON/XOFF 流控制模式，否则编程器将会失败。即使有了软件流控制，现代 PC 在接收到流控制信号之前，已经通过操作系统层发送了几个字节。我们通过在继续之前捕获这些字节来处理这个问题，这被报告为“滴下”的最大字节数。

如果上传有错误，PC 可能会继续向总线盗版者吐字节。为了保持错误消息可见，并防止终端中出现垃圾，XSVF 播放器在返回到提示符之前会等待五个小写的 z。我们选择这个序列是因为它永远不会出现在 XSVF 文件中。

*请注意，XSVF 播放器不支持 JTAG Hi-Z 引脚设置。即使成功了，也失败了。在没有缓冲器的情况下混合电压时要小心。

**更好的代码结构**

0b 版和 0c 版固件最大的区别是代码结构的巨大改进。在我们为第一篇文章打包之前，巴士海盗已经存在了很多次。v.0c 协调了代码库，使添加新协议变得更加容易。

*如何添加自定义协议*

总线盗版代码处理用户界面，并将两个变量传递给活动协议库。第一个变量是命令，例如 CMD_READ、CMD_READBULK 或 CMD_WRITE。整个命令集在 base.h 中定义。第二个变量是可选值。简单的 CMD_READ 命令不传递值，批量读取命令传递要读取的字节数，写入命令传递要写入总线的值，等等。至少，自定义协议需要一个函数来接收这些变量，并将它们转换成总线动作。

我们使用三种不同的技术将命令链接到总线动作。简单代码可以直接放在一个巨大的 switch 语句中，如 SPI.c。外部库使用单一链接函数，如 I2C.c 和 m_i2c_1.c。更复杂的协议使用 switch 语句来调用库中包含的函数(raw2wire.c、raw3wire.c、jtag.c UART.c)。base.h/c 中包含了对终端 IO 有用的功能

由于大量的代码改进，现在向总线盗版者注册一个新协议只是稍微有点混乱:

*base . h*–创建协议的定义。最后一个条目当前是“#define RAW3WIRE 7”，因此下一个条目可能是“#define MYCUSTOMWIRE 8”。

**bus pirate . c**–包含一个头文件，用于访问处理函数。在 *char* mode[] =* 变量列表中添加一个菜单项。菜单项*必须*位于列表中与 base.h 定义中分配的编号相同的位置。如果 MYCUSTOMWIRE 是数字 8，那么它必须是模式变量中的第八个条目。最后，向 bpProcess()函数添加一个额外的开关，当模式设置为“MYCUSTOMWIRE”时，该开关调用定制库处理例程。

**更进一步:一天一个愿望清单**

我们将得到的反馈整理成三个愿望清单:协议、特性和宏。

*协议*

*   [1 线](http://en.wikipedia.org/wiki/1-Wire)，带枚举(*一旦我们有零件测试它就准备好)
*   [OBD-II](http://www.elmelectronics.com/obdic.html) (感谢[ [沙迪曼](http://hackaday.com/2008/11/19/how-to-the-bus-pirate-universal-serial-interface/#comment-51551))
*   [能](http://en.wikipedia.org/wiki/Controller-area_network)
*   [迷笛](http://www.ucapps.de/) ( [维基](http://en.wikipedia.org/wiki/General_MIDI))
*   [DMX512-A](http://en.wikipedia.org/wiki/DMX512-A)
*   [IRDA](http://en.wikipedia.org/wiki/Irda) 、 [RC5x](http://hackaday.com/2008/10/30/how-to-usb-remote-control-receiver/) 等。

有些协议需要外部收发器。

*特性*

*   脉宽调制器、频率发生器
*   “等到中断”命令
*   将频率测量转换为输入捕获外设
*   允许对任何引脚进行频率测量
*   显示当前配置设置和引脚状态的报告。
*   批量读取、时钟滴答、延迟等的整数重复值。
*   CRC 生成器

*宏*

*   透明 UART 桥
*   SD 卡初始化、元数据提取和转储
*   EEPROM 编程/转储(I2C/SPI)
*   诺基亚 6100 液晶显示器初始化，控制
*   NMEA 全球定位系统数据解码器

你还有什么要补充的吗？

固件下载: [buspirate.v0c.zip](http://blog.mahalo.com/hackaday/howto/buspirate.v0c.zip)****
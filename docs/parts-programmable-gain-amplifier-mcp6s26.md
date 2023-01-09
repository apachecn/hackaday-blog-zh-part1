# 器件:可编程增益放大器(MCP6S26)

> 原文：<https://hackaday.com/2009/03/30/parts-programmable-gain-amplifier-mcp6s26/>

![mcp6s26](img/83ca176b046c77679df1ebc71e0f36d4.png "mcp6s26")

微芯片的 [MCP6S21/2/6/8](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en010485) 是可编程增益放大器，可将输入电压放大 1、2、4、5、8、10、16 和 32 倍。MCP6S22/6/8 还具有可选的输入通道，可用于不同的信号源。乘法因子和输入通道通过 [SPI](http://en.wikipedia.org/wiki/Serial_Peripheral_Interface_Bus) 接口进行配置。该芯片可用于放大小输入信号，并在多个模拟输入源中进行选择。下面我们演示六通道 MCP6S26。 

![mcp6s26](img/b6d805b2783fbe1f99c1e7dfa414dfa2.png "mcp6s26")

**[MCP6S26](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en010485) 可编程增益放大器([鼠标搜索](http://www.mouser.com/Search/Refine.aspx?Keyword=MCP6S26)、[八分搜索](http://octopart.com/search?q=MCP6S26)、$2.56) [数据表](http://ww1.microchip.com/downloads/en/DeviceDoc/21117a.pdf) (PDF)。**

我们用 3.3 伏电源测试了上面所示电路中的芯片。电阻分压器(R1-4)在通道 0、2 和 4 上输出一小部分电源。我们使用 5K 电阻，但电阻值并不重要。分压器在通道 0 上输出 2.4 伏，在通道 2 上输出 1.6 伏，在通道 4 上输出 0.8 伏。

| **公交海盗** | **DS1801 (pin #)** |
| 物理输出核心 | VOUT (1) |
| GND | VREF (8) |
| GND | VSS (9) |
| 特许测量员 | 政务司司长(10) |
| MOSI | 硅(11) |
| 军事情报部门组织(Military Intelligence Service Organization) | 所以(12) |
| 时钟 | SCK (13) |
| +3.3V | VDD (13) |

我们使用我们的[总线盗版通用串行接口](http://www.buspirate.com)来演示该芯片，但是对于任何微控制器实现来说，事务序列都是相同的。如上表所示，我们将 Bus Pirate 连接到 MCP6S26。我们为 raw3wire 模式(M，8)设置了具有正常输出的总线 Pirate，并启用了板载电源(大写“W”)。

> RAW3WIRE>[0b01000001 0] d
> CS 使能**<–开始 SPI 处理**
> 写:0x 41**<–更改输入通道命令**
> 写:0x 00**<–更改通道 0**
> CS 禁用**<–结束 SPI 处理**
> 电压探针:2.4 伏**<–Vout 电压测量**

写入 0b01000001 (0x41)后跟一个通道号会改变有效的 MCP6S26 输入。['拉低片选线以启动 SPI 处理。我们发送更改通道命令(0x41)，后跟 0，以选择输入 0。]'拉高芯片选择线以结束 SPI 处理。d '进行电压测量，显示增益为 0 的输入 0 为 2.4 伏

我们无法放大电源以外的输入电压(2.4 伏* 2 = 4.8，4.8 伏> 3.3 伏)，因此我们需要换到一个较低的通道来玩增益功能。

> RAW3WIRE>[0b01000001 4] d
> CS 使能
> 写:0x 41**<–更改输入通道命令**
> 写:0x 04**<–更改通道 4**
> CS 禁用
> 电压探针:0.8 伏**<–Vout 电压测量**
> RAW3WIRE >

通道 4 上的测量显示输出仅为 0.8 伏，有足够的空间来测试芯片的增益特性。

> raw 3 wire >[0b 01000000 0b 00000001]d
> CS 使能
> 写:0x 40**<–改变增益命令**
> 写:0x 01**<–增益设置(x2)**
> CS 禁用
> 电压探针:1.6 伏**<–Vout 现在是 0.8 伏* 2**
> RAW3WIRE >

一个双字节序列设置增益量。命令 0b01000000 (0x40)寻址增益寄存器，第二个字节设置乘法因子(0x01=增益为 2)。将增益设置为 2 会将输出电压乘以 2，0.8 伏* 2 = 1.6 伏

> raw 3 wire >[0b 01000000 0b 00000010]d
> CS 使能
> 写:0x 40**<–改变增益命令**
> 写:0x 02**<–增益设置(x4)**
> CS 禁用
> 电压探针:3.2 伏**<–Vout 现在是 0.8 伏* 4**
> RAW3WIRE >

这次我们设置增益为 4，0.8 伏* 4 = 3.2 伏

> raw 3 wire >[0b 01000000 0b 00000011]d
> CS 使能
> 写:0x 40**<–改变增益命令**
> 写:0x 03**<–增益设置(x5)**
> CS 禁用
> 电压探针:3.3 伏**<–净空不足以达到 0.8 伏* 5**
> RAW3WIRE >

最大输出电压是芯片的电源电压。如果我们设置增益为 5，输出电压不能超过 3.3 伏的电源(0.8 伏* 5 = 4 伏，4 伏> 3.3 伏)。

> RAW3WIRE>[0b00100000 0] d
> CS 使能
> 写:0x 20**<–睡眠命令**
> 写:0x 00**<–无关字节**
> CS 禁用
> 电压探针:0.0 伏**<–输出禁用**
> RAW3WIRE >

MCP6S26 具有省电睡眠模式。使用命令 0x20，后跟任意字节值，关断芯片。通过发送任何有效命令来离开睡眠。

喜欢这个帖子？查看您可能错过的[部分帖子](http://hackaday.com/category/parts/)。想申请一个职位吗？请在评论中留下你的建议。
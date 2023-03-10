# 部件:4×20 VFD 字符显示器(NA204SD02)

> 原文：<https://hackaday.com/2009/07/13/parts-4x20-vfd-character-display-na204sd02/>

![futuba-serial](img/f9152532b706025378c71df390f44eb9.png "futuba-serial")

[双叶](http://www.futaba.com/products/display_modules/module_products/character/index.asp)制造[真空荧光字符显示器](http://en.wikipedia.org/wiki/Vacuum_fluorescent_display)，可作为普通字符[液晶显示器](http://en.wikipedia.org/wiki/Lcd)的替代产品。VFD 具有更宽的视角，并且通常看起来更酷。

Futaba 的字符显示器可以使用标准的 [8 位或 4 位并行 LCD 接口](http://ouwehand.net/~peter/lcd/lcd0.shtml)或简单的双线协议进行接口。协议类型由显示器背面的电阻设置，因此没有[热风返工站](http://hackaday.com/2009/02/20/tools-aoyue-968-3-in-1-soldering-and-rework-station/)不太容易更改。今天我们将使用 Bus Pirate 演示一个串行接口 VFD。

**[福图巴 VFD](http://www.futaba.com/products/display_modules/module_products/character/index.asp) 字符 LCD 更换( [NA204SD02](http://www.primelec.com/Electronic-Components/LCDs-Displays/Futaba-4X20-LCD-Emulator-p7144243.html)** **，$7.00)。[数据表](http://www.futaba.com/products/display_modules/lcd_emulator/products/index.asp) (PDF)。**

| **VFD(引脚号)** | **公交车海盗** |
| GND (1) | GND |
| +5 伏(2) | +5v，Vpullup |
| 数据(3) | MOSI |
| 闪光灯(4) | 特许测量员 |
| 不适用(5) | — |
| 时钟(6) | CLK |

我们使用我们的 [Bus Pirate 通用串行接口](http://buspirate.com)来演示 Futaba VFD，但是接口操作对于任何微控制器实现都是相同的。我们在 VFD 和 Bus Pirate 之间的连接如上表所示。

我们用[开漏输出](http://hackaday.com/2009/07/01/mixed-voltage-interfacing-with-the-bus-pirate/) (HiZ)为 raw2wire 模式(菜单 M，7)设置 Bus Pirate。开漏输出允许我们使用板载上拉电阻(菜单 P，2)连接来自 3.3 伏总线的 5 伏 VFD。最后，我们启用了板载电源(大写“W”)。

VFD 的 strobe 引脚连接到 Bus Pirate CS 引脚。辅助引脚没有自己的上拉电阻，但 CS 有。否则，CS 在 raw2wire 模式下不使用，因此我们将辅助命令重新分配给 CS 引脚(菜单 C，2)。

*接口*

*![vfd-serial](img/94c9a903c2c18400df809da3ef3b2635.png "vfd-serial")
*

双线接口使用直接 16 位(2 字节)协议(数据手册第 20 页)。LCD 控制位(R/W、RS)放在第一个字节，8 个数据位放在第二个字节。所有处理都以 strobe 低电平开始，以 strobe 高电平结束。读操作与写操作类似，只是 R/W 位被置位，第二个字节被读取。

![vfd-command.pg27.](img/bb498ff48b00ac1c75a906be9ee12d6b.png "vfd-command.pg27.")

Futaba VFD 接受所有标准 HD44780 LCD 命令(数据表第 27 页)，有关每个命令的详细描述，请参见这些表格。复位(上电)后，VFD 希望第一个命令是功能设置命令。

> raw 2 wire > @**<–启动选通高**
> AUX 高 IMP，READ:1**<–AUX 引脚(CS)现在输入，上拉电阻保持选通高**
> raw 2 wire>a 0b 11111000 0b 001111000 @**<–command**
> AUX 低**<–选通低**
> WRITE: 0xF8 **<**

功能集配置数据接口长度(位 4)、显示行(位 3)和亮度/发光度(位 1，0)。开始之前，我们将 strobe 引脚设置为高电平(@)，以防它当前为低电平。然后，我们通过拉低 strobe 引脚(a)来开始处理，并发送第一个字节的读/写和寄存器选择(RS)设置。

第二个字节是命令。我们将数据接口长度设置为 8 位(位 4 = 1)，但在串行模式下，这可能会被忽略。我们的显示器有多条线(位 3 = 1)，我们将亮度设置为最大(位 1，0 = 0)。当 strobe 引脚返回高电平(@)时，序列结束。

> raw 2 wire > a 0b 11111000 0b 00001111 @
> AUX 低电平**<–选通低电平**
> 写:0x F8**<–起始字节(R/W=0，RS=0)**
> 写:0x0F**<–指令字节(显示开/关控制)**
> AUX 高电平 IMP，读:1**<–选通高电平**
> RAW2WIRE

显示开/关命令启用显示(位 3)，切换光标(位 1)，并闪烁光标(位 0)。我们启用了闪烁光标(位 1，0 = 1)的显示器(位 3 = 1 ),因此很明显显示器正在工作。

> raw 2 wire > a 0b 11111000 0b 100000000 @
> AUX 低电平**<–选通低电平**
> 写:0x F8**<–起始字节(R/W=0，RS=0)**
> 写:0x 80**<–指令字节(DDRAM 地址设置)**
> AUX 高电平 IMP，读:1**<–选通高电平**
> RAW2WIRE

在将字符写入显示器之前，我们需要通过发送与所需光标位置相加的 DDRAM 地址设置命令(0b10000000)来定位光标。我们将光标置于第 1 行的第一个字符。

第 1 行的第二个字符位于 0x01。要设置这个地址，我们需要发送 0b 10000001(0b 10000000+0b 00000001)。

字符显示内存不是线性的，第一行从 0x00 开始，第二行从位置 0x40 开始，第三行从 0x14 开始，最后一行从位置 0x54 开始。大多数显示器都有类似的配置，这里有一些[表，用于确定不同字符显示器](http://ouwehand.net/~peter/lcd/lcd0.shtml#visible_ddram)的布局。

> raw 2 wire > a 0b 11111010 0x 48 0x 61 0x 63 0x6b 0x 20 0x 61 0x 20 0x 44 0x 61 0x 79 @
> AUX 低电平**<–选通低电平**
> 写:0x fa**<–起始字节(R/W=0，RS=1)**
> 写:0x 48**<–ASCII 字母‘H’**
> …
> 写:0x 77

最后，我们可以在前面命令设置的位置输入一些字符。字符作为其 [ASCII 等效值](http://web.cs.mun.ca/~michael/c/ascii-table.html)输入。我们展示了大写的“Hack a Day”。

可以一次输入多个字符，但是因为内存空间不是连续的，所以需要手动将光标定位在每一新行的开头。在写入第 1 行的最后一个位置后，光标将前进到第 3 行的第一个字符。使用另一个位置命令 0b10010100，将光标设置到第 2 行的开头(0b10000000 + 0x14 = 0b10010100)。

喜欢这个帖子？查看您可能错过的[部分帖子](http://hackaday.com/category/parts/)。想申请一个职位吗？请在评论中留下你的建议。

**Hack a Day review disclosure:我们在易贝购买了这里演示的串行 VFD，Futaba 还向我们发送了一个带有并行接口的样品，我们将在稍后进行演示([此处显示的是](http://hackaday.com/2009/07/02/how-to-bus-pirate-probe-cable/))。**

**![futuba-serial.ii](img/e8116d9addee536324fe1e16dc593d30.png "futuba-serial.ii")
**
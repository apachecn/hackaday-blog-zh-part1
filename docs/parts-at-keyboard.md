# 零件:在键盘上

> 原文：<https://hackaday.com/2009/01/26/parts-at-keyboard/>

![atkeyboard](img/6d048de5f0b614f280fbfb1e0ce1d358.png "atkeyboard")

上周我们介绍了[总线盗版通用串行接口工具](http://hackaday.com/the-bus-pirate-universal-serial-interface/)的新版本。最近一次固件更新包括一个适用于两个硬件版本的 AT 键盘解码器库。

有一大堆旧键盘正被运往垃圾填埋场。我们将向你展示如何回收一个作为你下一个项目的输入设备。

**连接**

| **公交车海盗** | **电脑键盘(pin #)** |
| 国家药品监督管理局 | KBD 数据(3) |
| SCL | KBD 时钟(1) |
| +5 伏 | VDD (5) |
| GND | GND (2) |

AT 键盘通过双向双线接口进行通信。总线是[集电极开路](http://en.wikipedia.org/wiki/Open_collector)，但是键盘已经有内部[上拉电阻](http://en.wikipedia.org/wiki/Pull-up_resistor)。PC AT 键盘协议在这里描述[。我们使用我们的总线盗版工具来演示键盘协议，但是相同的基本原理适用于任何微控制器。](http://www.beyondlogic.org/keyboard/keybrd.htm)

我们将总线盗版连接到键盘，如表中所示。我们认为[这个](http://www.mouser.com/Search/ProductDetail.aspx?R=161-2306virtualkey11180000virtualkey161-2306)是键盘插孔的通孔母孔，但是我们没有测试过。你知道新插座的来源吗？

**协议**

键盘为*所有*数据传输提供时钟信号；PC 端类似于一个从设备。现有的总线盗版接口库都不支持外部时钟，因此我们编写了一个简单的 AT 键盘解码器库。该库依赖于键盘的时钟信号，如果键盘出现故障或没有连接，它就会挂起。如果您在自己的项目中使用我们的库，请考虑在 readbit()和 writebit()函数中添加超时延迟。

*PC 到键盘的命令代码*

| **代码** | **命令** |
| 0xed | 设置状态指示灯 |
| 0xee | 回声 0xee |
| 0xf0 | 设置扫描代码类型 |
| 0xf3 | 设置重复率 |
| 0xf4 | 键盘启用 |
| 0xf5 | 键盘禁用 |
| 0xfe | 重新发送最后一个字节 |
| 0xff | 重置键盘 |

PC 使用这些命令来控制 AT 键盘的各种功能。键盘用一个应答字节(oxfa)来响应命令。根据我们的经验，如果在命令发送后没有立即读取响应字节，键盘将会复位。

*键盘到 PC 的响应代码*

| **代码** | **响应** |
| 0xfa | 承认 |
| 0xaa | 自检通过 |
| 0xee | 回声响应 |
| 0xfe | 重新发送最后一个字节 |
| 0x00 或 0xff | 错误或缓冲区溢出 |

键盘有许多单字节响应代码。大多数 PC 命令用 0xfa 应答。键盘复位后发送 0xaa。

**设置公交海盗**

> HiZ>m
> 1。HiZ
> ……
> 9。PC 在键盘
> 模式>9**–设置模式**
> 900 模式设置
> X02 PC 在 KB 解码器就绪
> PC 在键盘>

首先，我们将总线盗版设置为键盘模式，选项 9。

> PC AT 键盘> p**<–电源设置**
> W/w 切换 3.3 伏电源？
> 1。没有
> 2。是
> 模式>1**<–无 3.3 伏电源**
> W/w 切换 5 伏电源？
> 1。否
> 2。是
> 模式>2**<–使用配置的 5V 电源**
> 9xx 电源，使用 W/w 切换
> 9xx 电压监视器:5V:0.0 | 3.3V:0.0 | VPULLUP:0.0 |
> PC 在键盘上>W**<–大写“W”，打开**
> 9xx 5V 电源在
> PC 上>

接下来，我们配置总线盗版的电源为 AT 键盘提供 5 伏电压。

> PC AT KEYBOARD > r**<–从键盘读取字节**
> x30 PCATKB READ:NONE**<–无数据可用**
> PC AT KEYBOARD >

AT 键盘库遵循标准的总线盗版语法。数值以字节的形式发送到键盘，“r”从键盘读取一个字节。该协议由键盘计时，因此逐位操作被禁用。如果没有可用数据，读取将返回“无”。

**设置键盘** 

> PC AT KEYBOARD > 0xee r**<–发送 0xee，读取一个字节**
> X20 PCATKB 写入:0xEE 得到 ACK**<–写入 0xEE，得到 ACK 位**
> x30 PCATKB 读取:0x ee**<–读取 0x ee，echo 成功**
> PC AT KEYBOARD >

我们可以使用 echo 命令 0xee 测试与 AT 键盘的连接。如果我们的连接是正确的，键盘将响应 0xee。

键盘用协议级的 ACK 位和 ACK 字节来响应命令。我们发现，如果发送命令后没有立即读取 ACK 字节，我们的测试键盘会自动重置。

> PC AT KEYBOARD > 0x ee**<–echo 命令**
> X20 pcat kb WRITE:0x ee get ACK**<–WRITE echo，get ACK**
> PC AT KEYBOARD>r**<–READ one byte**
> x30 pcat kb READ:0x aa**<–READ 0x aa，reset indicator**
> PC AT KEYBOARD>

这里，我们尝试发送 echo 命令，然后在稍后读取回复。键盘自动复位并回复 0xaa，自检通过。

> PC AT KEYBOARD > 0x ff r r**<–reset 命令，读取两个字节**
> X20 pcat kb WRITE:0x ff get ACK**<–写入 reset 命令，get ACK**
> x30 pcat kb READ:0x fa**<–命令 ACK 字节**
> x30 pcat kb READ:NONE**<–再次读取以复位 PC AT KEYBOARD >**

通过写入命令 0xff 并读取两个字节来复位键盘。键盘不会重置，直到第二个字节被读取。

> PC AT KEYBOARD > r**<–读取一个字节**
> x30 PCATKB READ:0x aa**<–复位成功**
> PC AT KEYBOARD >

复位后的短时间内，我们可以读取开机自检(POST)结果，0xaa 表示 POST 成功。

> PC AT KEYBOARD > 0x F5 r**<–禁用键盘**
> X20 pcat kb WRITE:0x F5 get ACK**<–写入命令**
> x30 pcat kb READ:0x fa**<–读取 ACK 字节**
> PC AT KEYBOARD>0x F4 r**<–启用键盘**
> X20 pcat kb WRITE:0x F4 get ACK**<–写入命令**

0xf5 禁用键盘输入。0xf4 使能键盘并清除缓冲器。

> PC AT KEYBOARD > 0xed r 0b 111 r**<–设置指示灯 LED**
> X20 pcat kb 写入:0x ed 获得 ACK**<–设置 LED 命令**
> x30 PCATKB 读取:0x fa**<–命令确认**
> X20 PCATKB 写入:0x07 获得 ACK**<–发送 LED 值
> x30 PCATKB 读取:0x fa**<–值确认<****

num、caps 和 scroll lock LEDs 由 0xed 命令控制。第二个字节(ob111)的最后三位表示哪些 led 要点亮。在键盘超时时间内完成所有四字节操作非常重要，否则键盘会复位。

> PC AT KEYBOARD > 0xee r**<–echo 测试命令**
> X20 PCATKB 写入:0x ee 获得 ACK
> x30 PCATKB 读取:0x ee
> PC AT KEYBOARD>0xfe r**<–重复最后一个字节命令**
> X20 PCATKB 写入:0x Fe 获得 ACK**<–写入重复命令**
> x30 PCATKB 读取:0x ee**<–重复前一个字节<**

最后一个有趣的键盘命令是重复字节命令。0xfe 使键盘再次发送最后一个字节。如果在之前的传输中有错误，这是一个有用的命令。

**按下
阅读键**

按键被键盘缓冲，直到我们阅读它们。

> PC AT KEYBOARD > r**<–READ byte**
> x30 pcat kb READ:0x 29**<–space scancode**
> PC AT KEYBOARD>r**<–READ byte**
> x30 pcat kb READ:0xf 0**<–key release scancode**
> PC AT KEYBOARD>r**<–READ byte**
> x30 pcat kb READ:

按键发送[扫描码](http://www.barcodeman.com/altek/mule/scandoc.php)，代表按键的多字节序列。在本例中，我们按下了扫描代码为 0x29 的 space。当释放一个键时，键盘发送 0xf0 和该键的扫描码(0x29)。每次按键都会产生类似的三部分序列。

> PC AT 键盘> r:4**<–读取 4 字节**
> x31 PCATKB 批量读取，0x04 字节:
> 0x29 0xF0 0x29 无**<–空间扫描码**
> PC AT 键盘>

这只是上一个例子的简化版本。我们没有单独读取三个字节，而是使用了批量读取命令。同样，我们得到了空间扫描码序列。我们读取不存在的第四个字节的尝试失败。
# 器件:单线温度传感器(DS1822)

> 原文：<https://hackaday.com/2008/12/10/parts-1-wire-temperature-sensor-ds1822/>

![1wire](img/2566deb383ed61e8f4dc7dbd2302d1e8.png "1wire")

**下载:** [buspirate.v0d.zip](http://blog.mahalo.com/hackaday/howto/buspirate.v0d.zip)

达拉斯/马克西姆的单线协议是[总线盗版](http://hackaday.com/2008/11/19/how-to-the-bus-pirate-universal-serial-interface/)中最受欢迎的。我们终于得到了一些单线器件，今天我们将演示 [DS1822 单线数字温度计](http://www.maxim-ic.com/quick_view2.cfm?qv_pk=2795)。获取[数据表](http://datasheets.maxim-ic.com/en/ds/DS1822.pdf) (PDF)并跟随。

这篇文章附有硬件版本 0 的总线盗版固件的 v.0d 版本。这包括新的 1 线协议库、更多配置选项和其他改进。

**[DS1822](http://www.maxim-ic.com/quick_view2.cfm?qv_pk=2795) 经济型数字温度计(Digikey # [DS1822+-ND](http://search.digikey.com/scripts/DkSearch/dksus.dll?Detail?name=DS1822%2B-ND) ，$3.87)** 我们在 [Cadsoft 下载页面](http://www.cadsoft.de/cgi-bin/download.pl?page=/home/cadsoft/html_public/download.htm.en&dir=pub/userfiles/libraries)上找到了 [Eagle](http://www.cadsoft.de/freeware.htm) 在 1-wire 库中的足迹。

单线协议使用单线进行数据传输，有时也用于供电。数据在[时间敏感的“时隙”](http://en.wikipedia.org/wiki/1-Wire#Example_communication_with_a_device)中传输，因为没有单独的时钟来描述位周期。

![ds1822cct](img/bdb45ae6a512e338a41c8b144a769e1e.png "ds1822cct")

| **巴士海盗** | **DS1822** |
| **SDA** | 冰雪皇后(Dairy Queen) |
| **+5v** | Vdd |
| **地面** | GND |

表中显示了 DS1822 的连接。我们使用 Bus Pirate 的 5 伏电源为 DS1822 供电，但它也可以在 3.3 伏下工作。一个电阻器(R1，~5K)使总线保持高电平。

所有单线命令都以复位程序开始，然后是五个 ROM 命令之一。

| **命令** | **描述** |
| 0x33 | 读取 ROM。读取单个设备地址。 |
| 0x55 | 匹配 ROM。匹配设备地址，后跟 64 位地址。 |
| 0xCC | 跳过 ROM。一起寻址所有设备。 |
| 0xEC | 报警搜索。搜索报警条件。 |
| 0xF0 | 搜索 ROM。地址枚举过程的一部分。 |

数据手册第 10 页描述了 ROM 命令。所有 ROM 命令在 Bus Pirate 1-Wire 库中作为宏提供，参见(0)菜单。ROM 命令宏*包括单线总线复位程序*。

**单个设备**

**![singli-4501](img/d5f9612f4759b90cf69d22489be75d1e.png "singli-4501")
**

所有单线器件都有一个唯一的 64 位(8 字节)地址，有些单线器件专门用于给电子设备一个唯一的跟踪号。当单个器件连接到单总线时，READ ROM 命令将提取其地址。

> 单线> { 0x 33 r:8**<–命令**
> xxx 单线总线复位正常
> xxx 单线写入:0x 33**<–读取 ROM**
> xxx 单线批量读取，0x08 字节:
> 0x 22 0x 47 0x 45 0x 22 0x 00 0x 00 0x 00 0x 29**<–ID #**
> 单线>

该命令发送总线复位({)、读取 ROM 命令(0x33)，并读取 64 位地址(r:8，8 字节* 8 位/字节= 64 位)。

第一个字节(0x22)将其标识为 DS1822 温度计。接下来的 6 个字节是该器件独有的，最后一个字节是前 7 个字节的一个 [CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check) 。

现在，我们可以用 MATCH ROM 命令对设备进行寻址，并向其发送进一步的指令。

> 1 线> { 0x 55 0x 22 0x 47 0x 45 0x 22 0x 00 0x 00 0x 29 0x 44
> XXX 1 线总线复位正常
> XXX 1 线写入:0x 55**<–匹配 ROM 命令**
> XXX 1 线写入:0x 22**<–起始地址**
> XXX 1 线写入:0x 47
> XXX 1 线写入:0x 45
> XXX 1 线写入:0x22
> xxx

首先，我们发送匹配 ROM 命令(0x55)和器件地址(8 字节)。接下来是启动温度转换的 CONVERT T 命令(0x44，数据手册第 11 页)。

第二个命令序列从 DS1822 获取温度读数。

> 1 线> { 0x 55 0x 22 0x 47 0x 45 0x 22 0x00 0x 00 0x 29 0x be r:9
> XXX 1 线总线复位正常
> XXX 1 线写入:0x 55
> XXX 1 线写入:0x 22
> *…长 1 线地址…*
> XXX 1 线写入:0x 29
> XXX 1 线写入:0x be**<–读取暂存命令**
> XXX 1 线批量读取，0x 0

读取暂存命令(0xBE，数据手册第 11 页)返回 9 个字节。我们只关心前两个字节，其余的可以根据数据手册第 7 页的表格进行解码。温度根据数据手册第 4 页计算得出:0x0171 HEX=369 DEC，369*0.0625=23C (74F)。

**多个设备**

![multi-450](img/f81d22bef9cbeb3eee5b43e3ea9be294.png "multi-450")

当多个单总线器件共享一条总线时，确定所有地址会更加困难。查找连接设备的最快方法是使用搜索 ROM 命令(0xF0)和二进制分支程序。总线盗版者用宏(240)自动完成这一操作。

> 1-WIRE >(240)**<–Macro 240**
> XXX 1-WIRE ROM 命令:SEARCH (0xF0)
> 在:
> Macro 1-WIRE 地址
> 1.0×22 0x 50 0x 28 0x 22 0x 00 0x 00 0x 00 0x 0a**<–地址**
> * ds 1822 Econ Dig Therm**<–根据系列代码**
> 2.0×20
> 宏可以使用前 10 个设备 id，参见(0)。
> 单线>

SEARCH ROM 命令显示它找到的设备，以及根据系列代码的类型。

我们认为输入 8 字节的单线地址非常繁琐，所以前 10 个器件地址存储在内存中，可以用宏(1)…(10)访问。编译时，可在单线库中定义最多 50 个器件地址的缓冲器。理想情况下，这些数据将存储在一个全局暂存缓冲区中，在未来的固件更新中由所有模块共享。

> 1-WIRE >(0)**<–显示宏列表**
> 0。宏菜单
> 宏单线地址**<–枚举器件地址**
> 1.0×22 0x 50 0x 28 0x 22 0x 00 0x 00 0x 00 0x 0a
> * ds 1822 Econ Dig Therm
> 2.0×22 0x d0 0x C7 0x 1a 0x 00 0x 00 0x 00 0x 01
> * ds 1822 Econ Dig Therm
> 3.0×22 0x 47 0x 45 0x 22 0x 00 0x 00 读取单个设备总线
> 85 的 ROM(0x 33)*。匹配 ROM(0x 55)*，后跟 64 位地址
> 204。跳过 ROM(0x cc)*，后跟命令
> 236。报警搜索(0xEC)
> 240。搜索 ROM (0xF0)
> 单线>

宏菜单(0)还将包括存储在名册中的设备地址。现在我们可以通过宏来寻址设备，而不是每次都输入完整的 64 位地址。

> 单线>(85)(1)0x 44**<–开始转换**
> xxx 单线总线复位正常
> xxx 单线写 ROM 命令:MATCH(0x 55)*跟随 64 位地址
> xxx 单线地址宏 1:0x 22 0x 50 0x 28 0x 22 0x 00 0x 00 0x 00 0x 00 a
> XXX 单线写:0x44
> 单线>(85)(1)0x be r:9**<–读取读数 *随后是 64 位地址
> XXX 1 线地址宏 1:0x 22 0x 50 0x 28 0x 22 0x 00 0x 00 0x 00 0x0A
> XXX 1 线写入:0x be
> XXX 1 线批量读取，0x09 字节:
> 0x 81 0x 01 0x 4b 0x 46 0x 7f 0x ff 0x 0f 0x 10 0x 71
> 1 线>**

(85)是总线复位和匹配 ROM 命令的快捷方式。(1)是器件地址宏，0x44 是开始温度转换的命令。获取读数涉及相同的宏，但是替换了读取设备的命令(0xBE)并获取了 9 个字节(r:9)。电脑风扇旁边的温度为 0x0181 或 24C。

**更进一步**

我们使用 Bus Pirate 对 1-Wire 协议进行了可视化演示，但真正的挑战是将其集成到您自己的设计中。Maxim 提供了[示例代码](http://www.maxim-ic.com/products/ibutton/software/1wire/wirekit.cfm)，Microchip 有一个 [app 备注](http://ww1.microchip.com/downloads/en/AppNotes/01199a.pdf) (PDF)，大家可以查看一下我们用的[示例代码](http://www.microchipc.com/sourcecode/#heater)。

**固件下载:** [buspirate.vod.zip](http://blog.mahalo.com/hackaday/howto/buspirate.v0d.zip)
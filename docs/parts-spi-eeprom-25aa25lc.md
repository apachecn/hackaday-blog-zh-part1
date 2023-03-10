# 器件:SPI EEPROM (25AA/25LC)

> 原文：<https://hackaday.com/2009/06/30/parts-spi-eeprom-25aa25lc/>

![3EEPROM-SPI](img/39016ae131f0832d5711ecfeab148766.png "3EEPROM-SPI")

微芯片的[25AA/25LC](http://www.microchip.com/stellent/idcplg?IdcService=SS_GET_PAGE&nodeId=2697)[EEPROM](http://en.wikipedia.org/wiki/EEPROM)是带有简单三线接口的数据存储芯片。25AA/LC 是普通 [24AA/LC I2C EEPROM](http://hackaday.com/2008/11/19/how-to-the-bus-pirate-universal-serial-interface/#EEPROM) 的 [SPI](http://en.wikipedia.org/wiki/Serial_Peripheral_Interface_Bus) 版本。它的容量从 128 字节到 128 千字节不等。我们看了最小的，128 字节的 [25AA010A](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en025533) 。

大多数类型的串行 EEPROMs 都有总线盗版演示。查看我们以前的 1 线( [DS2431](http://hackaday.com/2008/12/24/parts-1k-1-wire-eeprom-ds2431/) )和 I2C ( [24LC1025](http://hackaday.com/2008/11/19/how-to-the-bus-pirate-universal-serial-interface/#EEPROM) ) EEPROM 帖子。

下面继续查看我们的测试电路和 25AA010 EEPROM 演示。我们用[总线盗版](http://www.buspirate.com/)从我们的 PC 上玩这个芯片。在有限的时间内，你可以[得到你自己的巴士海盗](http://hackaday.com/2009/06/25/bus-pirate-preorders-open/)，完全组装并运往世界各地，只需 30 美元。

 

**[25AA010A](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en025533) SPI EEPROM 存储器，128 字节([八分搜索](http://octopart.com/parts/search?q=25AA010A)，0.70 美元)。[数据表](http://ww1.microchip.com/downloads/en/DeviceDoc/21832E.pdf) (PDF)。**

上面的原理图显示了一个简单的测试电路，可以与任何 25AA/25LC SPI EEPROM 一起工作。在真实电路的电源引脚上使用 0.1uF 去耦电容(C1)是个好主意，但我们在演示中没有使用。我们还将写保护(WP)和保持(hold)引脚连接到电源电压(V+)以禁用这些功能。

| **公交车海盗** | **25AA/LC (pin #)** |
| 特许测量员 | 政务司司长 |
| 军事情报部门组织(Military Intelligence Service Organization) | 所以(2) |
| MOSI | 硅(5) |
| CLK | SCK (6) |
| V+ | WP (3) |
| V+ | 保持(7) |
| v+(3.3 伏) | VCC (8) |
| GND | GND (4) |
| Vpullup | VCC (8) |

我们使用我们的[总线盗版通用串行接口](http://wwww.buspirate.com)来演示这个芯片，但是命令序列对于任何设置都是相同的。如上表所示，我们将 Bus Pirate 连接到 25AA010。我们为 SPI 模式(M，5)设置了正常输出的总线盗版，并启用了板载电源(大写“W”)。

25AA 零件的工作电压为 1.8 伏至 5.5 伏，25LC 零件的最低工作电压为 2.5 伏。我们使用 3.3 伏电源为芯片供电，并使用 Bus Pirate 的正常 3.3 伏引脚输出进行接口。

你也可以用总线盗版的 5 伏电源给芯片供电。在模式配置期间，通过选择开漏引脚类型(HiZ)以 5v 电压连接芯片，然后用连接到 5v 电压的上拉电阻保持总线高电平。

*接口*

数据手册的第 7 页有完整的接口命令列表。本演示展示了写入和检索数据所需的最少操作。

> SPI >[0b 110]**<–总线盗版命令语法**
> CS 使能**<–片选使能(0 伏)**
> 写:0x 06**<–写使能命令**
> CS 禁用**<–片选禁用(V+)**
> SPI >

将数据保存到 EEPROM 之前，需要有效的写使能命令。使能片选信号以唤醒芯片([)，发送写使能命令(0b110 二进制或 0x06 十六进制)，然后禁用片选(])。

> SPI >[0b 10 0 1 2 3 4 5]**<–总线盗版命令语法** CS 使能**<–片选使能(0 伏)**
> 写:0x 02**<–写数据命令**
> 写:0x 00**<–写地址(*有时 2 字节)**
> 写:0x 01**<–要写的数据(5 字节)**
> 写:写

通过发送写命令(0x02)、开始写入的地址(0x00)和要写入的字节(值 1 至 5)，将数据存储在 EEPROM 中。

单次操作最多可写入 16 个字节。所有写入必须在存储器的同一页，详情参见数据手册第 6 页。大于 256 字节的 EEPROMs 使用 16 位(2 字节)地址。

> SPI >[0b 11 0 r:5]**<–总线海盗命令语法**
> CS 使能**<–片选使能(0v)**
> 写:0x 03**<–读数据命令**
> 写:0x 00**<–读地址(*有时 2 字节)**
> 批量读 0x05 字节:
> 0x 01 0x 02 0x 03 0x 04**<–数据 we**

回读这些值以验证写操作。发送读取命令(0x03)和从(0x00)开始读取的地址，然后从芯片读取 5 个字节(r:5)。输出应该与我们之前写的值相匹配。

*大于 256 字节的 EEPROMs 使用 16 位(2 字节)地址。如果您使用这些 EEPROMs 中的一个，请输入一个双字节地址，如“0 0”。

喜欢这个帖子？查看你可能错过的[部分帖子](http://hackaday.com/category/parts/)。想申请一个职位吗？请在评论中留下你的建议。
# 如何:总线盗版，通用串行接口

> 原文：<https://hackaday.com/2008/11/19/how-to-the-bus-pirate-universal-serial-interface/>

**更新:** [与 JTAG 的新固件还有更多](http://hackaday.com/2008/12/01/bus-pirate-firmware-update-v0c-jtag-and-more/)

我们总是很兴奋能得到一个新的芯片或 SIM 卡接口，但我们的热情往往被原型制作过程所挫伤。连接任何芯片通常意味着试验电路，编写代码，并拖出编程器；甚至可能是原型 PCB。

几年前，我们制造了第一个“总线海盗”，这是一个通用总线接口，可以从 PC 串行终端与大多数芯片通信。3.3-5 伏支持多种标准串行协议，包括 [I2C](http://en.wikipedia.org/wiki/I%C2%B2C) 、 [SPI](http://en.wikipedia.org/wiki/Serial_Peripheral_Interface_Bus) 和[异步串行](http://en.wikipedia.org/wiki/Asynchronous_start-stop)。额外的“原始”2 线和 3 线库几乎可以连接任何专有串行协议。因为这对我们来说是一个非常有用的工具，我们清理了代码，记录了设计，并在这里发布了规格、原理图和源代码。

**概念概述**

**![overview-diagram-new](img/e1af8d5193aeb17ffbae972998752f50.png "overview-diagram-new")
**

 ****

总线盗版是一个串行终端桥多个集成电路接口协议。我们在计算机的串行终端上输入命令。命令通过 PC 串行端口发送到总线盗版。总线盗版者以适当的协议与微芯片对话，并将结果返回给 PC。

所有引脚输出 3.3 伏电压，但允许 5 伏电压。板载 3.3 伏和 5 伏电源可为连接的芯片供电。软件可配置 I2C [上拉电阻](http://en.wikipedia.org/wiki/Pull-up_resistor)完成封装。

![terminal-450](img/a14e18bdce5cfc5fd26f046623f32536.png "terminal-450")

串行终端接口适用于任何系统:PC、Mac、Linux、Palm Pilots、WinCE 设备等；不需要任何垃圾。我们考虑过 USB 设备，但 USB 与大量具有串行端口的手持设备不兼容。我们还想要一个 3.3 伏的设备，具有 5 伏容许输入，但最受欢迎的通孔 USB 微控制器是 5 伏器件(例如 [PIC18Fx550](http://www.microchip.com/ParamChartSearch/chart.aspx?branchID=111&mid=10&lang=en&pageId=74) )。

Bus Pirate 目前“说”三种用于高速接口的硬件协议，并有两个软件协议库用于简单的总线操作。每种协议的理论和规范都超出了我们在这里所能涵盖的范围，但是请查看其中的一些教程:

*I2C*

一条慢速双线总线。维基百科是了解 I2C 背景的好地方。I2C-Bus.org、[机器人电子学](http://www.robot-electronics.co.uk/htm/using_the_i2c_bus.htm)、[嵌入式系统学院](http://www.esacademy.com/faq/i2c/)、[Embedded.com](http://www.embedded.com/story/OEG20010718S0073)都有像样的 I2C 教程。

*SPI*

简单的三线总线。维基百科有[背景](http://en.wikipedia.org/wiki/Serial_Peripheral_Interface_Bus)；Embedded.com 有一个伟大的[教程和 I2C](http://www.embedded.com/columns/beginerscorner/9900483) 比较。

*通用异步收发器(UART 或串行)*

一种时钟和时序相关的串行协议，以其作为 PC 串行端口协议而闻名。维基百科有关于[异步串行协议](http://en.wikipedia.org/wiki/Asynchronous_start-stop)的背景。

*原始 2 线*

这是一个通用的双线协议库，类似于 I2C，但没有 ACK 位。利用这种模式下可用的总线操作，可以形成 I2C 和许多专有的 2 线协议。使用该库来处理非 I2C 双线设备，如[智能卡](http://www.smartcardsupply.com/Content/Cards/SLE4442.htm)或 [Sensirion SHT11](http://www.sensirion.com/en/01_humidity_sensors/02_humidity_sensor_sht11.htm) 温度/湿度传感器。

*原始 3 线*

这是一个通用三线式协议库，类似于 SPI，但没有硬件模块的限制。使用这个库与使用非 8 位兼容三线协议的设备一起工作，如 [Sparkfun 诺基亚 6100 LCD 山寨](http://www.sparkfun.com/commerce/product_info.php?products_id=569)。利用这种模式下可用的总线操作，可以形成许多三线式协议。

**硬件**

![brd-450](img/d2a7f48b2d9890b4dbf5b5d3c6951566.png "brd-450")

[点击查看全尺寸 PCB 布局图](http://hackaday.com/files/2008/11/brd.png) (PNG)。螺丝端子连接到电源。一排七个引脚接头连接到 IO 引脚。尽管有标签，但只需要 7v DC。

| **销** | **SPI** | **I2C** | **RS232** |
| **B9** | MOSI | SDA | – |
| **B8** | CLK | SCL | – |
| **B7** | 味噌 | – | RX |
| **B6** | CS | – | TX |
| **B5** | au | au | au |
| **地面** | GND | GND | GND |

下表显示了每种总线模式的引脚连接。原始双线模式使用与 I2C 相同的引脚配置。原始三线模式使用与 SPI 相同的引脚配置。

![cct-450](img/99aed936933dbd706d69e2ca794c34fa.png "cct-450")

[点击查看全尺寸电路图像](http://hackaday.com/files/2008/11/cct.png) (PNG)。电路和 PCB 使用免费版的 [Cadsoft Eagle](http://www.cadsoft.de) 设计。下载[项目档案](http://blog.mahalo.com/hackaday/howto/buspirate.v0b.zip) (ZIP)。

*PIC 24FJ64GA002*

我们在总线盗版中使用了一个 [PIC24FJ64GA002](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en026374) 微控制器；这是我们在[迷你服务器项目](http://hackaday.com/2008/09/25/web-server-on-a-business-card-part-2/)中使用的同一芯片。它的速度足以完成我们想要的一切(16MIPS)，外设引脚选择特性允许硬件 SPI、UART 和 I2C 模块共享输出引脚。每个电源引脚需要一个去耦电容(C12，13)，MCLR 功能需要引脚 1 和 3.3 伏之间的一个电阻(R7)。PIC 有一个内部稳压器，需要一个 10uF 钽电容(C3)，尽管我们使用普通电解电容没有问题。在我们的 [PIC24F 教程](http://hackaday.com/2008/09/18/web-server-on-a-business-card-part-1/)中阅读关于编程和使用该芯片的内容。如果你没有 PIC 调试器，一些读者推荐易贝上不到 40 美元的 ICD2 克隆版。

PIC 在 3.3 伏下运行，但数字专用引脚可承受 5 伏电压，用于连接 5 伏逻辑。引脚 14、15、16、17、18、21 和 22 仅是数字引脚，我们通过查阅数据手册并排除任何模拟连接类型的引脚来确定(第 11-16 页，表 1-2)。根据数据表，I2C 引脚也能承受 5 伏电压。网上有很多相互矛盾的信息，但数据手册第 230 页的参数 DI28 明确指出，24FJ64GA002 I2C 引脚在没有模拟电路的情况下的最大输入为 5.5 伏

引脚 21 和 22 (RB10/11)可以通过电阻 R4 和 R5 上拉 SDA/SCL。

*MAX3223CPP*

该芯片将 3.3 伏串行输出转换为兼容 PC 串行端口的+/-10 伏 RS232 信号。MAX3223CPP 是 MAX202 的 3-5v 版本，具有额外的节能功能。MAX RS232 收发器需要四个 0.1uF 电容用于电荷泵(C4，5，7，8)和一个去耦电容(C17)。我们对所有东西都使用相同的电容器。

我们用了一个 MAX3223CPP，好像已经没有了。MAX3223EEPP+ 是一个引脚兼容的新版本，在 Digikey 上售价 7 美元。哎哟！没有使用 3223 的节能功能，所以如果可能的话，应该用更便宜、更简单的 3.3 伏 RS232 收发器代替。

*电源*

大多数芯片可以由总线盗版的板载 3.3 伏和 5 伏电源供电。5v 电压由一个普通的 7805 稳压器(VR2)和两个去耦电容(C9，10)提供。使用两个电阻(R2，3)将 LM317 可调稳压器(VR1)设置为 3.3 伏，并需要两个去耦电容(C6，7)。该电路需要 7-10 伏 DC 电源(J1)。

*零件清单*

| **部分** | **值** |
| IC1 | [PIC24FJ64GA002-DIP](http://search.digikey.com/scripts/DkSearch/dksus.dll?Detail?name=PIC24FJ64GA002-I/SP-ND) |
| IC2 | MAX3223CPP(试用 [MAX3223EEPP+](http://search.digikey.com/scripts/DkSearch/dksus.dll?Detail?name=MAX3223EEPP%2B-ND) ) |
| C3 | [10uF 电容器](http://www.mouser.com/Search/ProductDetail.aspx?qs=M%252b5JCWh%252b1ty3RFguvdcdsg%3d%3d)(最好是钽) |
| C4-13，17 | [0.1uF 电容](http://www.mouser.com/Search/ProductDetail.aspx?qs=9AX3phJxokWIpR5WRGtIJw%3d%3d) |
| R1 | [330 欧姆电阻](http://www.mouser.com/Search/ProductDetail.aspx?qs=ULgY8XwKjTmmv2gtdH4CoQ%3d%3d) |
| R2 | [240 欧姆电阻](http://www.mouser.com/Search/ProductDetail.aspx?qs=4eNa8160l8VHA9lUHkRdvw%3d%3d) |
| R3 | [390 欧姆电阻](http://www.mouser.com/Search/ProductDetail.aspx?qs=X3IDIfI%252bJAVuAq1Yim8fmg%3d%3d) |
| R4，5，7 | [2K2 欧姆电阻](http://www.mouser.com/Search/ProductDetail.aspx?qs=8tsW7z%2fc78pkoLNVKn1xoQ%3d%3d) |
| VR1 | [LM317](http://www.mouser.com/Search/ProductDetail.aspx?qs=swDD%252bF%252bps7c8uLyY%252b3mJJw%3d%3d) |
| VR2 | [LM7805](http://www.mouser.com/Search/ProductDetail.aspx?qs=cnIeywgme7bzmZ37%2fiFT9w%3d%3d) |
| X1 | [螺丝夹(3 个端子)](http://www.mouser.com/Search/ProductDetail.aspx?qs=wjes1ZhMGKfGv3iS94oZ%252bQ%3d%3d)*未经测试 |
| X2 | [DB9 母连接器(串口)](http://www.mouser.com/Search/ProductDetail.aspx?qs=nAEW9fCjKd%2fyLNwP2ItddQ%3d%3d)*未测试 |
| ICSP，SV3 | [.1″引脚接头，直角](http://www.mouser.com/Search/ProductDetail.aspx?R=4-103329-0virtualkey57100000virtualkey571-41033290) |
| J1 | [电源插孔，2.1 毫米插脚](http://www.mouser.com/Search/ProductDetail.aspx?qs=8xMK%252bwDsXhcfMNb%2fYnnwLQ%3d%3d) |
| LED1 | 3 毫米 LED(可选) |

**固件**

固件使用免费演示版的 [PIC C30 编译器](http://www.microchip.com/stellent/idcplg?IdcService=SS_GET_PAGE&nodeId=1406&dDocName=en010065)用 C 编写。在我们对 PIC 24F 系列的[介绍中了解所有关于使用这张 PIC 的信息。下载](http://hackaday.com/2008/09/18/web-server-on-a-business-card-part-1/)[项目档案](http://blog.mahalo.com/hackaday/howto/buspirate.v0b.zip) (ZIP)。

main . c–处理用户终端界面。

c——抽象例程，将语法转换成适当总线上的动作。

UARTs IO . c–两个硬件 UART 的 IO 例程。

m _ i2c _ 1 . c–软件 I2C 例程，作者为[ [Michael Pearce](http://www.microchipc.com/sourcecode/#i2c) 。我们不能让 PIC 硬件 I2C 工作，所以我们使用这个有用的库。该软件没有考虑 I2C 速度设置，似乎工作在大约 5 千赫。

SPI . c–驱动硬件 SPI 模块的例程。

raw 2 wire . c–软件双线接口库。

raw 3 wire . c–软件三线式(SPI)接口库。

用户输入保存在一个 4000 字节的缓冲区中，直到检测到换行符(enter)。如果输入的第一个字符是一个菜单选项(见下文)，则显示菜单对话框，否则对字符串进行解析，以获取要通过总线发送的数据(见语法)。代码由令人尴尬的大量 switch 语句和意大利面条式代码组成。

**终端接口**

我们没有编写一个垃圾软件来控制设备，而是给了它一个串行命令行接口，可以在任何 ASCII 终端上工作。总线盗版者用三个数字的结果代码和一条短消息来响应命令。代码的设计考虑到了 PC 自动化。我们在[项目档案](http://blog.mahalo.com/hackaday/howto/buspirate.v0b.zip) (zip)中包含了一个结果代码表。

*菜单选项*

菜单选项是不涉及数据传输的单字符命令。输入字符，然后按`<enter>`，进入菜单。

**？**–显示带有命令和语法的帮助菜单。

**M**–设置总线模式(SPI、I2C、UART、原始 2 线、原始 3 线)。紧接着是速度、极性和输出状态的提示(取决于模式)。

*   总线速度:SPI:30、125、250、1000KHz。I2C:100，400，1000 千赫。UART: 300，1200，2400，4800，9600，19200，38400，57600，115200bps。原始模式:1、10、50 千赫。
*   反向时钟设置设置与正常相反的空闲状态(正常 SPI:空闲低电平；正常 UART:idle 高):SPI:idle 高；UART:空闲低电平。
*   有些模式具有可选的高 z 输出模式，与上拉电阻配合使用(低电平=接地，高电平=输入)。

**L–**切换位发送/接收顺序:最高/最低有效位优先。

**P**–SDA/SCL 引脚上拉电阻切换(3.3 伏)。仅在 I2C 和原始 2 线模式下有效。

**O**–设定数字输出显示格式。终端可以将数字显示为十进制、十六进制和二进制 ASCII 值。第四种格式发送原始的、未处理的字节，用于读取 ASCII 格式的文本。

*语法*

一种简单的语法用于通过总线与芯片通信。语法命令具有一般适用于所有总线类型的通用功能。

**A/A/@**–切换辅助销。大写字母“A”设置为高，小写字母“A”设置为低。@将 aux 设置为输入(高阻抗模式)并读取引脚值。

**[**–开始数据写入。SPI/raw 3 线:片选使能。I2C/raw 2 线:开始条件。RS232:打开 UART，丢弃接收的字节。

**{**–开始数据写入和读取。与[，除了:SPI/raw 3 线:显示每次写入的读取字节。RS232:显示异步到达的数据。

**]或}**–结束数据写入。SPI/raw 3 线:片选禁用。I2C/raw 2 线:停止条件。RS232:关闭 UART。

**R/R**–读取字节。SPI/raw 3 线:发送虚拟字节，返回读取。I2C:用 ACK 读取字节。原始 2 线:读取 8 位。RS232:检查 UART 的字节并返回，如果为空则失败。使用 0r1…255 进行最多 255 字节的批量读取。

**0b**–写入该二进制值。一个字节的格式是 0b00000000，但部分字节也可以:0b1001。

**0h 或 0x**–写入该十六进制值。格式为 0h01 或 0x01。部分字节也可以:0xA。A-F 可以是小写或大写字母。

**0-255**–写入该十进制值。任何前面没有 0x、0h 或 0b 的数字都被解释为十进制值。

**或空格**--值分隔符。使用逗号或空格来分隔数字。任何组合都可以，非数字值之间不需要分隔符:{0xa6，0，0 16 5 0b111 0haF}。

*原始 2 线模式和原始 3 线模式的直接总线操作命令。*
**^**–发送一个时钟滴答声。将 0^1…255 用于多个时钟刻度。

**/和\**–切换时钟电平高(/)和低(\)。包括时钟延迟(100 微秒)。

**-/_**–切换数据状态高(-)和低(_)。包括数据建立延迟(20uS)。

**！**–用时钟读取一位。

**。**–读取数据引脚状态(无时钟)。

**&**–延时 1uS。多次延迟使用 0 & 1…255。

**使用它**

**![buspirate-24fv0a](img/0a751fd8d7c721207c7361875a0b1e94.png "buspirate-24fv0a")
**

这里有两个例子，展示了巴士海盗的行动。终端应设置为 ASCII 模式并带有本地回送，我们使用的是 Windows 串行终端。PC 端串行连接是 115200bps，8N1。总线盗版应该响应任何单线馈送类型(0x0a、0x0d)或两者(Windows 风格)。

*T1。I2C/SPI–闪存 24LC1025 EEPROM*

微芯片的电可擦可编程只读存储器(EEPROMS)是流行的永久性存储芯片， [24LC1025](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en024636) 有 128 千字节的存储空间，带有 I2C 接口。我们可以测试这种芯片，而不需要对大电路进行电路板测试或编写代码。

![i2ceeprom](img/8373a837005bded2b9f6ef7c417f8c84.png "i2ceeprom")

图为一个 24LC1025 连接到总线盗版。EEPROM 的工作电压范围为 2.7 至 5 伏，因此我们使用总线盗版的 3.3 伏电源为电路供电。片上 SDA/SCL 上拉电阻保持 I2C 总线为高电平，无需外部电阻。一个 0.1uF 电容将 EEPROM 与电源去耦。

设置 I2C 模式

首先，我们将总线盗版设置为 I2C 模式，并使能上拉电阻。由于总线盗版目前使用软件 I2C 库，速度设置并没有真正的影响。

> SPI > m**<–输入 m 为模式选择**
> 1。SPI
> 2。I2C
> 3。UART
> 4。生 2 丝
> 5。生 3 丝
> 模式>2**–输入 2 为 I2C**900 模式设定
> 设定速度:
> 1。100KHz(标准)
> 2。400KHz(快速模式)
> 3。1MHz(高速)
> 速度>1**<–速度实际上没有任何作用…**
> 901 速度设置
> 202 I2C 就绪，P/p 为上拉
> I2C>P**<–使能 I2C 上拉电阻**
> 205 I2C 上拉
> I2C >

写入 EEPROM (I2C)

所有的 I2C 操作都以开始条件{或]开始，以停止条件{或}结束。写操作从寻址器件(1 字节)并寻找确认位(ACK)开始。如果 EEPROM 响应，我们可以发送数据位置写入(2 字节)和数据有效载荷(n 字节)。总线盗版器会在每次写入结束时自动检查 ACK，并在每次读取时检查 ACK。

24LC1025 的基址是 1010xxy，其中 xx 由引脚 2 和 3 的状态决定，y 是读(1)或写(0)模式。我们将引脚 2 和 3 连接为高电平，使完整的写地址**为 1010110** 。我们将从第一个数据位置( *0 0* )开始写入设备，并使用混合数据输入格式( 1…13 )写入 1 到 13。

> I2C > {**0b 10100110***0 0*1 2 3 4 5 6 7 8 9 10 0xb 0xc 13} **<–I2C 命令**
> 210 I2C 启动条件**<–总线启动**
> 220 I2C 写:0xA6 得到 ACK:是**<–地址发送和 ACK 接收**
> 220 I2C 写:0x00 得到 ACK:是**<–写地址**
> 220 I2C 写:0x00 得到 ACK:是**<–写地址**

从 EEPROM 读取(I2C)

读取 24LC1025 需要两步。首先，没有数据的写命令设置地址指针。第二，read 命令从步骤 1 中设置的位置开始输出数据。

第一个命令是写命令，我们使用写地址的十六进制等效值(0b10100110 = 0xa6 ),以节省一点打字时间。地址指针被设置到我们写入数据的位置(0 0)。

> I2C > { 0xa6 0 0 }**<–设置写指针命令**
> 210 I2C 开始条件
> 220 I2C 写:0x a6 得到 ACK:是
> 220 I2C 写:0x00 得到 ACK:是
> 220 I2C 写:0x00 得到 ACK:是
> 240 I2C 停止条件

设置好指针后，我们就可以开始读取数据了。读取地址是器件地址，最后一位设为 1 ( 0b10100111 或 0xa7)。我们使用了 13 个 r 命令来读取数据，但是我们也可以使用简写版本:0r13。

> I2C > { 0b 10100111 rrrrrrrrrrrrrr }**<–读命令**
> 210 I2C 起始条件
> 220 I2C 写:0xA7 得到 ACK:是**<–芯片 ACK 读地址**
> 230 I2C 读:0x 01**<–数据字节 1**
> 230 I2C 读:0x 02**<–数据字节 2**
> …
> …

我们知道操作是成功的，因为输出与我们之前写的数据相匹配。

*UART–em 406 surf iii GPS*

![gps](img/298309100c5092c112946b8ad95bb647.png "gps")

EM406 是一个微小的 5 伏 GPS 模块，可以跟踪多达 20 颗卫星。默认情况下，它以 4800bps，8N1 的速度从串行端口输出 NMEA 格式的数据。输出格式是标准串行，但在 2.8 伏时，它与 PC 串行端口不兼容。总线盗版者可以连接这个 GPS，而不需要单独的 RS232 收发器或 5v 电源。

设置 UART

首先，我们设置总线盗版 UART 以 4800bps 的速率接收串行数据。

> I2C > m**<–设置模式**
> 1。SPI
> 2。I2C
> 3。UART
> 4。生 2 丝
> 5。RAW 3 线
> 模式>3**<–UART**
> 900 模式设定
> 设定速度:
> (bps)
> 1。300
> 2。1200
> 3。2400
> 4。4800
> …
> 9。115200
> 速度>4**4800 bps**901 速度设定
> 302 UART 就绪
> UART >

启用 UART 和数据读取

关于 UARTs，需要记住的一件重要事情是，数据是异步到达的。与数据传输由主机控制的 SPI 和 I2C 不同，串行数据可以随时到达 UART。GPS 就是一个很好的例子，因为它可以连续不断地输出位置数据，无需用户干预。

我们开发了两种读取模式来处理异步数据。{当所有传入数据到达时，对其进行回声。新数据将取代和混淆数据输入，但所有输入仍正常接受。[在仅发送模式下打开 UART，丢弃输入的字节。}或]关闭 UART，不考虑模式。

> UART > {**<–打开异步读取的 UART**
> 310 UART 打开，}关闭
> 330 UART 读取:0x 80**<–GPS 数据**
> 330 UART 读取:0x78

写入 UART

输入数值以发送 UART。即使输入被输入数据打断，它也会在`<enter>`被处理。我们发送了 *0x40* 作为示例，但这对 GPS 模块没有特别的意义。

> 330 UART 读:0x 80*0x 40***<–随机字节写**
> 320 UART 写:0x 40**<–字节写**

关闭 UART

" } "后跟`<enter>`关闭 UART。

> 330 UART 读取:0x78
> 303 UART 读取:0x 60*}***<–关闭 UART 命令**
> 330 UART 读取:0xE6
> 340 UART 关闭
> UART >

不要以为你可以用这个 GPS 数据来跟踪我们，我们在妈妈的地下室里没有卫星信号。

**更进一步**

总线盗版是我们实验室的一个重要开发工具。我们在使用时会不断更新它，并且在添加协议和功能时会发布新的固件。期待在以后的文章中看到巴士海盗。

这些改进是我们的首要任务。有什么建议吗？

*   新协议:单线，CAN？？？
*   极性和其他设置的控制
*   可调指令延迟
*   让硬件 I2C 模块工作。
*   启用协议速度设置。
*   更便宜、更容易获得 RS232 收发器

项目档案 (ZIP)有你需要的一切来建造你自己的巴士海盗。
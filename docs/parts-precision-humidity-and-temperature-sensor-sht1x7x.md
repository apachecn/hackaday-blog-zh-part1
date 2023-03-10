# 零件:精密湿度和温度传感器(SHT1x/7x)

> 原文：<https://hackaday.com/2008/12/29/parts-precision-humidity-and-temperature-sensor-sht1x7x/>

![sht11](img/d1a4984d7964ea1a0d257a6a6469fd9a.png "sht11")

Sensirion 的 [SHTxx](http://www.sensirion.com/en/01_humidity_sensors/00_humidity_sensors.htm) 是一款数字接口湿度和温度传感器。精确的湿度测量通常需要精心的模拟设计，但 SHTxx 将所有复杂的东西都集成到一个芯片中。有通孔(SHT7x)和表面贴装(SHT1x)两种版本，我们使用表面贴装 SHT11，精度为+/-3%。下面我们将向您展示如何使用 SHTxx。

**Sensirion SHT1x/SHT7x 精密湿度和温度传感器( [Octopart 搜索](http://octopart.com/search?q=sht*)，25 美元起)。**

这不是一个便宜的传感器。Octopart 列出了[几个可以买到它的地方](http://octopart.com/search?q=sht*)。几家较小的业余爱好电子商店出售这种产品；Hobby Engineering 售价 29 美元( [H01509-01C](http://www.hobbyengineering.com/H1509.html) )。我们在 [Cadsoft 库下载页面](http://www.cadsoftusa.com/cgi-bin/download.pl?page=/home/cadsoft/html_public/download.htm.en&dir=eagle/userfiles/libraries)的 *sht10_11_15.lbr* 和 *sht11.lbr* 中找到了兼容的 PCB 尺寸。不同封装类型的引脚连接见数据手册: [SHT1x](http://www.sensirion.com/en/pdf/product_information/Datasheet-humidity-sensor-SHT1x.pdf) (PDF)， [SHT7x](http://www.sensirion.com/en/pdf/product_information/Datasheet-humidity-sensor-SHT7x.pdf) (PDF)。

![sht11](img/df55198cf613a59f8643c8981df19535.png "sht11")

SHTxx 有一个双线串行接口，需要上拉电阻(R1，2)，阻值在 2K 和 10K 之间。Sensirion 建议，只有当传感器通过一段电线供电时，才使用去耦电容(C1)，但我们认为包含一个去耦电容总是一个好主意。

我们将使用带 Hi-Z 输出的 raw2wire 模式中的[总线盗版通用串行接口](http://hackaday.com/2008/11/19/how-to-the-bus-pirate-universal-serial-interface/)演示 SHTxx。SHTxx 由 Bus Pirate 的 3.3 伏电源供电。总线海盗的板载上拉电阻保持总线高，消除了外部电阻 R1 和 R2 的需要。

**界面**

SHTxx 使用简单的串行协议通过两条线进行通信。该协议与 I2C 不兼容，但单个 SHTxx 可以存在于带有 I2C 外设的总线上。

| **命令** | **代码** |
| 测量温度 | *000* 00011 |
| 测量相对湿度 | *000* 00101 |
| 读取状态寄存器 | *000* 00111 |
| 写状态寄存器 | *000* 00110 |
| 软复位 | *000* 11110 |

五个命令控制 SHTxx，如下表所示。前 3 位是地址(始终为 000)，其余 5 位是唯一的命令代码。

**复位**

通过清除先前使用的任何部分命令或数据来启动事务。当数据为高电平时，至少需要 9 个时钟周期才能清除 SHTxx 接口。对于这一点，总线盗版的语法是*-^:9*；数据高(-)，9 个时钟周期(^:9).【T2

SHT11 的命令以唯一的起始条件开始。像 [I2C 起始条件](http://www.esacademy.com/faq/i2c/busevents/i2cstast.htm)一样，这是数据信号随时钟信号高电平变化的唯一时间。这种非法条件导致芯片准备新的命令。SHTxx 起始条件不同于 I2C，允许两种类型的器件存在于同一总线上。

生成 SHTxx 样式开始条件的总线盗版代码是*-/_ \/-\*；数据开始为高电平(-)，时钟上升(/)，数据变为低电平(_)，时钟为低电平(\)，时钟为高电平(/)，数据变为高电平(-)，最后一次时钟为低电平转换(\)结束序列。

软复位是一个好主意，因为它将芯片置于默认状态。在第一次温度或湿度转换之前，我们发送软复位命令。

> RAW2WIRE>-^:9 -/_\/-\ 0b00011110！**<–命令**
> 4xx RAW2WIRE 数据输出，1**<–清接口**4xx raw 2 wire 0x 09 时钟滴答
> 4xx RAW2WIRE 数据输出，1**<–起始条件**
> 4xx RAW2WIRE 时钟，1
> 4xx RAW2WIRE 数据输出，0
> 4xx RAW2WIRE 时钟，0
> 4xx RAW2WIRE 时钟，1
> 4xx raw 2

首先，我们清除接口(-^:9)，然后发送开始条件( *-/_\/-\)。*复位命令(0b00011110=0x1E)跟随其后。命令发送后，SHTxx 通过将数据线拉低一位来应答(ack)命令。我们读一位(！)以获得确认状态；0 表示成功，1 表示出错。

**温度**

现在我们可以读取温度**。**这分两步进行，温度转换有延迟。【T2

> RAW2WIRE>-^:9 -/_\/-\ 0b00000011！
> 4xx RAW2WIRE 数据输出，1**<–清零接口**
> 4xx RAW2WIRE 0x09 时钟滴答
> 4xx RAW2WIRE 数据输出，1**<–起始条件**
> …
> 4xx RAW2WIRE 时钟，0
> 420 RAW2WIRE 写:0x 03**<–起始温度转换**
> 4xx RAW2WIRE 读位:0**<–ack 位**

首先，我们发送一个起始条件和温度转换命令(00000011=0x03)。SHTxx 通过将数据线拉低一位(ack)来响应成功的命令。ack 位之后，数据线变为高电平，直到转换完成。

> RAW2WIRE >。
> 4xx RAW2WIRE 数据输入，状态:0**<–完成时数据低**
> RAW2WIRE >

当数据线变为低电平时，温度转换完成。'.'是在没有时钟滴答的情况下读取数据状态的总线盗版命令。现在我们可以抓取结果了。

> raw2wire>r_^ r_^ r_^
> 430 raw 2 wire 读取:0x 17**<–数据字节 1**
> 4xx RAW2WIRE 数据输出，0**<–数据低电平**
> 4xx RAW2WIRE 0x01 时钟滴答**<–发送 ack 位**
> 430 RAW2WIRE 读取:0x cc**<–数据字节 2**
> 4xx RAW2WIRE 数据输出，0
> 4xx RAW2WIRE 0x01

每个字节读取(r)都需要一个数据为低电平的 I2C 式应答位。我们用 _^序列来做这个。数据低电平(_)，一个时钟周期(^).

前两个字节是温度读数(0x17cc)，随后是 CRC (0x0c)。原始值(0x17cc=6092)通过数据手册第 9 页的公式和系数转换为摄氏度。默认情况下，温度读数为 14 位:

T = -39.7 + 0.01* *X*

21.22 c=-39.7+(0.01 **6092*

**湿度**

湿度转换从代码 00000101 (0x05 十六进制)开始。 ****

> RAW2WIRE>-^:9 -/_\/-\ 0b00000101！**<–命令**
> 4xx RAW2WIRE 数据输出，1**<–清零接口**
> 4xx RAW2WIRE 0x09 时钟滴答
> 4xx RAW2WIRE 数据输出，1**<–起始条件**
> …
> 4xx RAW2WIRE 时钟，0
> 420 RAW2WIRE 写:0x 05**<–开始湿度转换**
> 4xx RAW2WIRE 读位:

如前所述，如果 SHTxx 处理了命令，则第九个应答位为低电平。

> RAW2WIRE >。
> 4xx RAW2WIRE 数据输入，状态:0**<–完成时数据为低电平**

湿度转换完成后，数据线变为高电平，然后返回低电平。

> raw2wire>r_^ r_^ r_^
> 430 raw 2 wire 读取:0x 05**<–数据字节 1**
> 4xx RAW2WIRE 数据输出，0**<–数据低电平**
> 4xx RAW2WIRE 0x01 时钟滴答**<–ack 位**
> 430 RAW2WIRE 读取:0x 80**<–数据字节 2**
> 4xx RAW2WIRE 数据输出，0
> 4xx RAW2WIRE 0x01

完整的转换产生一个三字节响应。前两个字节是原始湿度读数(0x0580=1408)，最后一个字节是 CRC (0x46)，可用于验证数据完整性。

默认情况下，湿度读数具有 12 位分辨率，使用以下公式转换为湿度:

RH =-2.0468+0.0367(*x*)+(-0.0000015955 *(*x*^2))

46.46%相对湿度=-2.0468+0.0367(*1408*)+(-0.0000015955 *(*1408*^2))

**结论**

这不是一个廉价的传感器，但它不需要像霍尼韦尔 HIH 系列那样精心的模拟设计。你用过湿度传感器吗？

喜欢这个帖子？查看您可能错过的[部分帖子](http://hackaday.com/category/parts/)。
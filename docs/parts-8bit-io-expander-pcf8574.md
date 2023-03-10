# 器件:8 位 IO 扩展器(PCF8574)

> 原文：<https://hackaday.com/2008/12/27/parts-8bit-io-expander-pcf8574/>

![pcf8574](img/949f69a79351f490b6f5f7ff39842b37.png "pcf8574")

有时，一个项目的传感器、按钮或 led 比您的微控制器的引脚还多。 [PCF8574](http://focus.ti.com/docs/prod/folders/print/pcf8574.html) 是向微控制器添加 8 个低速输入或输出引脚的简单方法。可配置地址允许多个 PCF8574s 存在于同一总线上，因此两个微控制器引脚可以控制几十个 IO 引脚。下面我们将向你展示如何使用这个芯片。

![pcf8574](img/a57cea32d2a7dde858ab885beb543c12.png "pcf8574")

[TI PCF8574](http://focus.ti.com/docs/prod/folders/print/pcf8574.html) I2C 8bit IO 扩展器(mouer #[595-PCF 8574n](http://www.mouser.com/Search/ProductDetail.aspx?qs=L5CvrNUdZirGmsfmc3baKQ%3d%3d)，$1.86)

我们在 Cadsoft Eagle [库下载页面](http://www.cadsoft.de/cgi-bin/download.pl?page=/home/cadsoft/html_public/download.htm.en&dir=eagle/userfiles/libraries)的 *i2c.lbr* 和 *micro-phillips.lbr* 中找到了该芯片的 PCB 尺寸。PCF8574 由 2 线 [I2C 协议](http://en.wikipedia.org/wiki/I%C2%B2C)控制，所以我们用我们的[总线盗版通用串行接口](http://hackaday.com/2008/11/19/how-to-the-bus-pirate-universal-serial-interface/)来演示这个芯片。相同的基本操作将适用于任何微控制器。

原理图显示了我们针对 PCF8574 的简单测试电路，这里是[数据手册](http://www.ti.com/lit/gpn/pcf8574) (PDF)。我们为芯片提供 5v 电源，并在电源和接地引脚之间使用 0.1uF 去耦电容(C1)。R1 和 R2 将 I2C 时钟和数据总线保持在 5 伏。我们将使用 LED 来测试芯片的输出特性；P0 通过限流电阻 R3 (330+欧姆)连接到 LED1。P6 和 P7 与已知状态相关联，因此我们可以轻松测试芯片的输入能力。

PCF8574 的 I2C 地址为 0100xxxy，其中三位(x)由地址引脚 A2-0 的状态决定，最后一位(y)设置读(1)或写(0)模式。通过使用不同的地址引脚设置，许多 PFC8574s 可以共享一条 I2C 总线。由于我们将地址引脚接地，因此写地址为 01000000 (0x40)。

**输出**

P0 上的 LED 通过将 1(开)或 0(关)写入写地址后的字节的位 0 来控制。

> I2C > { 0x40 0b 000000001 }**<–命令**
> 210 I2C 开始条件
> 220 I2C 写:0x 40 得到 ACK:是**<–写地址**
> 220 I2C 写:0x01 得到 ACK:是**<–输出值**
> 240 I2C 停止条件
> I2C >

*{* 发出 I2C 起始条件，随后是写地址 0x40。输出值 0b00000001 将 P0 设为高电平，其余位设为低电平。}发送 I2C 汽车站条件，结束交易。当相应的位设为高电平时，LED 开启。

要关闭 LED，重复该序列，并将相应的输出位设为 0。

> I2C > { 0x40 0b 00000000 }**<–命令**
> 210 I2C 开始条件
> 220 I2C 写:0x 40 得到 ACK:是**<–写地址**
> 220 I2C 写:0x00 得到 ACK:是**<–输出值**
> 240 I2C 停止条件
> I2C >

P0 现在设为接地，LED 关闭。

**输入**

设置为输出高电平的引脚也可以用作输入(数据手册第 1 页)。在本例中，P6 保持高电平(+5 伏)，P7 保持低电平(地)，但这些也可以是按钮、传感器或其他数字逻辑。其他引脚悬空，不代表有效数据。

> I2C > { 0x40 0b 11000000 }**<–命令**
> 210 I2C 开始条件
> 220 I2C 写:0x 40 得到 ACK:是**<–写地址**
> 220 I2C 写:0xC0 得到 ACK:是**<–输出值**
> 240 I2C 停止条件
> I2C >

首先，我们将 1 写入输出值的相应位，将所需的输入引脚设置为高电平输出。位 6 和 7 将 P6 和 P7 设置为输出高电平。

现在，我们可以读取 pin。我们在将总线盗版的输出设置为二进制模式的情况下执行了此操作，因此引脚值立即变得明显。

> I2C > { 0x 41 r }**<–命令**
> 210 I2C 开始条件
> 220 I2C 写:0b01000001 得到 ACK:是**<–地址**
> 230 I2C 读:0b 01000000**<–引脚状态**
> 240 I2C 停止条件
> I2C >

{发出 I2C 起始条件，0x41 是读取地址，r 从器件读取一个字节。}发送 I2C 汽车站条件，结束交易。

回复 01000000 表示输入引脚的状态。最高有效位为 0，因为 P7 接地。下一位是 1，因为 P6 保持高电平，其他位(0)是垃圾数据。

这远远不是唯一的 IO 扩展器 IC。你用过另一个芯片吗？

不要忘记补上你可能错过的任何[部分帖子](http://hackaday.com/category/parts/)。
# 操作方法:数码相框，100% DIY

> 原文：<https://hackaday.com/2009/01/08/how-to-digital-picture-frame-100-diy/>

![frontii](img/19e2cd44f4462fd5d8d8d3269991b00f.png "frontii")

有大量的数码相框教程。大多数是老式笔记本电脑，巧妙的重新配置适合相框。

我们着手打造一个 100% DIY、零基础的数码相框。我们的框架有一个 12 位彩色液晶显示器，在普通的 FAT 格式的 microSD 卡上有千兆字节的存储空间，你可以在家里制作它。我们得到了下面的细节。

**概念概述**

![overview](img/32891b9a5ce70a9cb555e1ccb9c8ce6e.png "overview")

位图图像存储在普通的 PC 可读的 microSD 卡上。PIC 微控制器通过三线式 SPI 总线读取图像。PIC 处理图像数据，并通过单向 9 位 SPI 类总线将其写入彩色 LCD。SD 卡上的配置文件定义了图像之间的延迟。

**硬件**

**![cct450](img/02af64230ba9796495a73d141bd9604d.png "cct450")
**

[点击查看全尺寸示意图](http://hackaday.com/wp-content/uploads/2009/01/cct.png) (PNG)。电路和 PCB 使用免费版的 [Cadsoft Eagle](http://www.cadsoft.de/) 设计。这个项目的所有文件都包含在本文末尾链接的项目档案中。

![back](img/4996dc880c4c7b5954079afa6202e0fc.png "back")

*微控制器*

我们在这个项目中使用了一个微芯片[pic 24 FJ 64 ga 002](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en026374)28 引脚 SOIC 微控制器(IC1)。我们真的很喜欢这个芯片，因为外设引脚选择功能让我们把重要的功能放在我们想要的引脚上；这使得 PCB 更小、更简单、更紧凑。每个电源引脚都有一个 0.1uF 旁路电容接地(C1，2)。内部 2.5v 调节器需要一个 10uF 钽电容(C12)。该芯片通过一个五引脚接头 SV1 进行编程。R1 是引脚 1 上 MCLR 功能的上拉电阻。在我们的 [PIC24F 简介](http://hackaday.com/2008/09/18/web-server-on-a-business-card-part-1/)中阅读更多关于该芯片的信息。

一个 32.768kHz 晶体(Q1)和两个 27pF 电容(C10，11)为实时时钟日历(RTCC)提供振荡器。这些部分是可选的，初始固件不使用它们。RTCC 可以用作在屏幕上叠加当前时间的功能的一部分。连接到编程标题的按钮可用于设置时间。

*SD 卡*

[MicroSD](http://en.wikipedia.org/wiki/MicroSD) 卡与普通 SD 卡完全兼容，MicroSD 卡可以在带有适配器的 SD 卡读写器中使用。我们[测试了几个 microSD 卡持有者](http://hackaday.com/2008/10/06/parts-microsd-memory-card-holders/)，并选定了 SparkFun Electronics 的一个。microSD 卡要求在电源引脚和地之间有一个旁路电容(C3)。LED 指示 microSD 读取活动，但它对一般调试也很有用(LED1，R2)。

*彩色液晶 128×128 诺基亚仿制品*

这个项目是围绕 [SparkFun 的 20 美元彩色液晶面板](http://www.sparkfun.com/commerce/product_info.php?products_id=569)设计的。LCD 逻辑在 3.3 伏下运行，需要一个去耦电容(C4)。LED 背光需要单独的 7v 电源，并且似乎有内部限流器，因为示例设计不使用外部电阻。

LCD 有一个独立的 3.3 伏显示电源输入。如果电压不干净，许多人会报告显示器有噪音。我们使用铁氧体磁珠(L1)和 0.1uF 电容(C5)对电源进行滤波，没有遇到任何问题。这甚至在一个肮脏的家庭蚀刻的原型上工作。铁氧体磁珠类型并不重要，我们使用的是我们的[微型网络服务器项目](http://hackaday.com/2008/09/25/web-server-on-a-business-card-part-2)遗留下来的一种。

小连接器用阻焊膜很容易焊在专业板上，但是买几个作为保险。SparkFun 在其 [Eagle 零件库](http://www.opencircuits.com/SFE_Footprint_Library_Eagle)中有该零件的 PCB 足迹，但焊盘之间的间距小于 [Olimex](http://www.olimex.com/pcb/) 或 [BatchPCB](http://www.batchpcb.com/) 将制造的尺寸。我们通过减小焊盘尺寸来获得更多的空间。不要依靠连接器来固定液晶显示器，使用胶带将其固定。我们用粘性标签临时贴上了液晶显示器。

在发送最终设计用于生产之前，我们制作了 LCD 载板的原型。我们建议不要在没有阻焊膜的情况下在连接器下使用接地填料。

*电源*

由 LD1117S33 (IC2)提供的 3.3 伏电源为 PIC、microSD 卡、LCD 逻辑和 LCD 显示器供电。IC2 的电源端需要一个 0.1 微法旁路电容(C6)，输出端需要一个 10 微法电容(C13)。我们使用与 PIC 内部调节器相同的钽电容。

LCD 背光由 LM317 可调稳压器(IC3)供电，该稳压器通过 240 (R5)和 1100 (R6)欧姆电阻配置为 7 伏。C7 和 C8 是 LM317 的 0.1uF 旁路电容。

J1 是一个用于普通[2.1 毫米 DC 筒形插头](http://en.wikipedia.org/wiki/DC_connector)的 SMD 电源插孔。C11 是一个 10uF 电解电容，可以平滑电源电压的任何滞后。C11 的最大输入额定值为 16 伏，因此电源电压最好保持在 12 伏以下。9-12 伏可能是理想的供电范围。

**PCB**

**![board4501](img/40fea7cd2e8d65bc51a3e4fa7747fdd3.png "board4501")
**

[点击查看全尺寸摆放图](http://hackaday.com/wp-content/uploads/2009/01/board1.png) (PNG)。L1，C5 和液晶显示器在对面。我们无法在妈妈的地下室里制作双面板的原型，所以我们把这个设计发给了 [BatchPCB](http://www.batchpcb.com/) 。下周我们将向你展示我们是如何做到的。

*缔约方清单*

| **部分** | **描述** |
| IC1 | [PIC 24FJ64GA002](http://www.mouser.com/Search/ProductDetail.aspx?qs=V/yyTCAHA4D/h5r3CRQDtA==) (SOIC) |
| IC2 | [LD 1117s 33](https://www.mouser.com/Search/ProductDetail.aspx?R=LD1117S33CTRvirtualkey51120000virtualkey511-LD1117S33C)3.3 伏稳压器(SOT223) |
| IC3 | [LM317 可调调节器](http://www.mouser.com/Search/ProductDetail.aspx?R=LM317MDCYRvirtualkey59500000virtualkey595-LM317MDCYR) (SOT223) |
| 1 美元 | [彩色液晶 128×128 诺基亚山寨](http://www.sparkfun.com/commerce/product_info.php?products_id=569)  |
| – | [诺基亚山寨连接器](http://www.sparkfun.com/commerce/product_info.php?products_id=570)  |
| C1-8 | [0.1uF 电容器](https://www.mouser.com/Search/ProductDetail.aspx?R=C0805C104M5RACTUvirtualkey64600000virtualkey80-C0805C104M5R) (0805) |
| C10，11 | [27pF 电容器](http://www.mouser.com/Search/ProductDetail.aspx?qs=0ZUpllj3bsbA9A7Pajx4jA%3d%3d) (0805) |
| 12.13 | [10uF 钽电容器](http://www.mouser.com/Search/ProductDetail.aspx?R=293D106X96R3A2TE3virtualkey61320000virtualkey74-293D106X96R3A2TE3) (SMCA) |
| C14 | [10uF 电解电容](https://www.mouser.com/Search/ProductDetail.aspx?R=UWF1C100MCL1GBvirtualkey64700000virtualkey647-UWF1C100MCL1GB)(贴片) |
| 腰神经 2 | [铁氧体磁珠](https://www.mouser.com/Search/ProductDetail.aspx?R=BLM21BB600SN1Dvirtualkey64800000virtualkey81-BLM21BB600SN1D) (0805) |
| LED1 | [LED](http://www.mouser.com/Search/ProductDetail.aspx?qs=7JStj%2fjQ2SElGv%2fp7IzKlg%3d%3d) (0805) |
| 雌三醇环戊醚 | [32.768kHz 晶体](http://www.mouser.com/Search/ProductDetail.aspx?R=CM200S-32.768KDZF-UTvirtualkey69500000virtualkey695-CM200S-327KF-U) |
| R1 | [2000 欧姆电阻](http://www.mouser.com/Search/ProductDetail.aspx?qs=jBethxrBxZb5NLDetw123g%3d%3d) (0805) |
| R2 | [390 欧姆电阻](http://www.mouser.com/Search/ProductDetail.aspx?qs=2BMLUTrrT4P7Xm58YbKmPg==) (0805) |
| R5 | [240 欧姆电阻](http://www.mouser.com/Search/ProductDetail.aspx?qs=B6sMDe4C%252beDvUrZZzlhhcA%3d%3d) (0805) |
| R6 | [1100 欧姆电阻](http://www.mouser.com/Search/ProductDetail.aspx?qs=DZvKvnD5UYWyFJjgnPvJ4g%3d%3d) (0805) |
| SD1 | [microSD 卡座](http://www.sparkfun.com/commerce/product_info.php?products_id=127) |
| J1 | [2.1 毫米电源插孔](http://www.mouser.com/Search/ProductDetail.aspx?qs=b2tC%2fwvzm2TxaPjSsb%252bCzQ%3d%3d)(贴片) |
| SV1 | [0.1 英寸公插头，直角](http://www.mouser.com/Search/ProductDetail.aspx?R=4-103329-0virtualkey57100000virtualkey571-41033290) |

**固件**

固件使用免费演示版的 [PIC C30 编译器](http://www.microchip.com/stellent/idcplg?IdcService=SS_GET_PAGE&nodeId=1406&dDocName=en010065)用 C 编写。在我们对 PIC 24F 系列的[介绍中了解所有关于使用这张 PIC 的信息。固件包含在本文末尾的项目档案中。](http://hackaday.com/2008/09/18/web-server-on-a-business-card-part-1/)

*FAT12/16/32 磁盘库*

[Microchip 的 FAT 12/16/32 库](http://www.microchip.com/stellent/idcplg?IdcService=SS_GET_PAGE&nodeId=1824&appnote=en532040)让我们可以轻松访问存储在 SD 卡上的文件。我们在名片项目的 [web 服务器上给出了这个库的详细描述。如果你在图书馆读卡有问题，检查它是否在数码相机中格式化或者使用](http://hackaday.com/2008/09/25/web-server-on-a-business-card-part-2)[松下的 SD 卡格式化器](http://panasonic.jp/support/global/cs/sd/download/sd_formatter.html)。

*诺基亚 6100 液晶驱动*

SparkFun 为诺基亚 6100 提供了一个基本的 8 位颜色驱动程序。我们将其移植到 PIC，并更新为每像素 2 字节[12 位颜色模式](http://www.idcomm.com/personal/lorenblaney/sparkfun.html)。通过增加少量的复杂性，可以使用不同的 12 位模式轻松提高像素写入速率，该模式使用 3 个字节提供两个像素。

LCD 使用 9 位协议，比大多数 SPI 硬件能处理的多一位。第一位告诉 LCD 接下来的 8 位是数据还是命令。在 PIC 24F 上，不可能手动输入第一位，然后使用 SPI 外设发送剩余的 8 位。当硬件 SPI 使能时，我们失去了对引脚的直接控制。数据输入必须完全位碰撞，这大大降低了屏幕刷新率。

*读取位图*

有大量的[位图格式](http://en.wikipedia.org/wiki/Windows_bitmap)。Windows 兼容性让每个人都使用古老的 [Windows v3 格式](http://en.wikipedia.org/wiki/Windows_bitmap#Bitmap_information_.28DIB_header.29)。我们创建了两个 C 结构来读取 V3 位图数据。

| **偏移** | **字节** | **位图文件头** |
| Zero | Two | 总是 0x42 0x4D(十六进制表示 BM) |
| Two | four | 文件大小(字节) |
| six | Two | 保留，忽略 |
| eight | Two | 保留，忽略 |
| Ten | four | 第一个位图数据在文件中的位置 |

位图文件以 14 字节的文件头开始。前两个字节是字母“BM”，表示位图。如果前两个字节正确，固件将加载信息头。最后四个字节表示位图数据的开始，但是当前的固件只是假设它将在头的末尾开始。

| **偏移** | **字节** | **位图信息头** |
| Fourteen | four | 位图信息头的长度(Windows V3 位图为 40 字节) |
| Eighteen | four | 宽度(像素) |
| Twenty-two | four | 高度(像素) |
| Twenty-six | Two | 颜色平面，总是 1 |
| Twenty-eight | Two | 每像素颜色位数(1、4、8、16、24 和 32) |
| Thirty | four | 压缩方法，我们只读取未压缩的(类型 0) |
| Thirty-four | four | 图像数据长度 |
| Thirty-eight | four | 水平分辨率(每米像素) |
| forty-two | four | 垂直分辨率(每米像素) |
| Forty-six | four | 颜色数量，忽略。 |
| Fifty | four | 重要颜色的数量，忽略不计。 |

Windows V3 位图信息头的长度为 40 字节。固件验证报头长度(偏移量 14)为 40，表示 V3 位图。如果宽度(132)、高度(132)、颜色深度(24)和压缩(0)都检查通过，图像数据将被处理并输出到屏幕。

| **偏移** | **字节** | **24 位图像位图数据** |
| 54+(3 牛) | one | 像素 n 红色值 |
| 54+(3n+1) | one | 像素 n 绿色值 |
| 54+(3n+2) | one | 像素 n 蓝色值 |

位图图像具有以三个字节序列存储的像素数据的未压缩的 1:1 表示。数据从图像的右下角开始；首先是红色值，然后是绿色和蓝色。维基百科有一个[完整的位图遍历](http://en.wikipedia.org/wiki/Windows_bitmap#Example_of_a_2x2_Pixel.2C_24-Bit_Bitmap)。

如果位图图像的颜色深度(24 位)大于 LCD 可以显示的深度(12 位)，我们需要丢弃颜色数据的最低有效位。要从 24 位颜色转换到 12 位颜色，我们只需丢弃一半的颜色数据；将 8 位值 11110011 向右推 4 位，得到 1111。

*固件演练*

1.  初始化图片，标清，液晶显示器。
2.  读取 config.ini，如果它不存在，则创建它。
3.  使用 config.ini 的第一个字符来设置图像之间的延迟。
4.  寻找图像，打开下一个图像。
5.  阅读并检查位图文件头的格式是否正确。
6.  阅读并检查位图信息标题的版本、大小和颜色。
7.  读取并显示每个像素值。根据需要调整位深度。
8.  延迟，然后从 4 开始重复。

**准备图像**

**![newyear](img/571f94a97768cbb6b79977367eb41347.png "newyear") ![hackaday](img/c2fd7cc2d6bb7d3374a88cb109ef13f2.png "hackaday") ![tulips1](img/fd853a9f6f41834217f8ae78d6e450d4.png "tulips1")** 

为了简化演示，相框只显示最常见的位图格式。图像大小必须为 132 x132 像素，24 位颜色。

1.  用图像编辑程序打开图片。
2.  在您想要使用的图像部分上绘制一个方形选择框，通常使用 shift 和拖动。
3.  裁剪图像。
4.  将图像大小调整为 132 x132 像素。
5.  将图像保存为 windows 位图，24 位色深。

其他图像大小和格式可以通过固件升级(巴布亚新几内亚，JPG)来支持，特别是通过引脚兼容的微控制器升级到[巨型 dsPIC 33F](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en532302) 。

**使用它**

将图像放入 FAT 格式 SD 卡的根目录中。根据最后格式化卡的设备，可能需要使用数码相机或松下 SD 格式化程序进行格式化。

可选:使用文本编辑器生成 config.ini 文件。输入 0-9 之间的一个数字，设置画面间延迟。保存文件。如果您没有创建自己的 config.ini 文件，系统会延迟 1 秒为您创建一个。

将卡插入插座，然后插入数码相框。图像将以定义的延迟在屏幕上循环显示。

**更进一步**

我们在这个简单的数码相框中看到了很多潜力。许多功能可以通过固件升级来添加，其中一些是未来硬件的基础。 ****

*   显示其他图像格式，缩放图像
*   随机淡入淡出和擦除
*   在图像上显示时间和日期，用连接到编程引脚的按钮设置
*   扩展 config.ini 中的配置选项，以包括更长的延迟、渐变或擦除类型
*   使用图像子目录，因为 FAT 格式 SD 卡的根目录有一些文件限制。
*   为网络显示更新添加以太网连接。

~~**下载:** [dpf.v1.zip](http://blog.mahalo.com/hackaday/howto/dpf.v1.zip)~~ 它已经把[移到这里](http://www.whereisian.com/files/dpf.v1.zip)。

[https://www.youtube.com/embed/AKlQwLkeWdE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AKlQwLkeWdE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
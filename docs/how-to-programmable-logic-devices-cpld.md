# 操作指南:可编程逻辑器件(CPLD)

> 原文：<https://hackaday.com/2008/12/11/how-to-programmable-logic-devices-cpld/>

[复杂可编程逻辑器件](http://en.wikipedia.org/wiki/CPLD)(CPLD)包含数百个 [7400 系列逻辑 IC](http://en.wikipedia.org/wiki/7400_series)的构建模块。可以在 PC 上设计完整的电路，然后上传到 CPLD 上立即实施。连接到 CPLD 的微控制器就像一个配有可重编程电路板和库存充足的电子商店的微控制器。

起初，我们并不确定 CPLDs 在业余项目中的广泛吸引力和应用，但我们已经被说服了。一个定制的逻辑器件可以省去几天阅读数据手册、寻找[理想逻辑 ic 组合](http://en.wikipedia.org/wiki/7400_series#7400_series_subfamilies)，然后等待芯片到来的时间。使用 CPLDs 的电路板更简单，因为具有可编程引脚布局的单个芯片可以取代[100 个独立的逻辑 IC](http://en.wikipedia.org/wiki/List_of_7400_series_integrated_circuits)。电路错误可以通过上传新的设计来纠正，而不是蚀刻和填充新的电路板。CPLDs 速度很快，反应时间从 100MHz 开始。尽管功能极其多样，但 CPLDs 是一项成熟的技术，芯片起价 1 美元。

我们有一个家庭可蚀刻，自我编程开发板，让你开始。不要担心，这个板有一个串行端口接口与 CPLD 一起工作，不需要一个单独的(通常是并行端口)JTAG 编程器。

**CPLD 简介**

**![bitclone-24fv1final](img/59446921d202fd8516244779eadffb3c.png "bitclone-24fv1final")
**

*何时使用 CPLD*

当设计需要多个 7400 系列逻辑 ic 时，可以考虑使用 CPLD。CPLD 将会更便宜、更快，并且可以通过理想的引脚排列配置对更简单的 PCB 进行编程。

在可能需要多次迭代的复杂设计中使用 CPLD。在软件中设计新电路并上传到 CPLD 比设计、蚀刻和填充新电路板更容易。

要获得最高速度和即时响应，请选择 CPLD。速度上的差异是惊人的；CPLDs 以 100MHz 开始，而微控制器以几 MHz 响应中断。CPLD 设计形成对外部刺激作出反应的电路，反应几乎是瞬间发生的。微控制器执行代码对事件作出反应，即使中断例程也有相对较高的延迟。

*CPLD vs FPGA*

FPGA 比 CPLDs 更为人所知，但它们有许多共同的特征。这个类比并不完美，但我们喜欢它:FPGAs 是一个可重编程的处理器内核，CPLD 是一个可重编程的电路板或试验板。FPGAs 取代了微控制器、存储器和其他元件。CPLDs 吸收逻辑 ic，与微控制器配合工作良好。

*制造商*

最大的 CPLD 制造商 Altera 和 [Xilinx](http://www.xilinx.com/) 以其 FPGAs 而闻名。 [Lattice Semiconductor](http://www.latticesemi.com/) 是另一家大型 CPLD 制造商，社区追随者较少。Atmel 制造旧工业标准 CPLDs 的[引脚兼容版本](http://www.atmel.com/dyn/products/devices.asp?family_id=653)。

如果你计划在 5 伏电压下工作，你的选择是有限的。Xilinx XC9500 CPLDs 仍有新旧库存，但价格是新的 3.3 伏同等产品的四倍。Atmel 的 [ATF1502 系列](http://www.atmel.com/dyn/products/product_card.asp?part_id=2123)工作在 5v，但是他们不提供自由的开发环境。

在 3.3 伏下有更多的选择，但新的 CPLDs 越来越多地使用 2.5 伏、1.8 伏或更低的内核。Altera [MAXII](http://www.altera.com/products/devices/cpld/max2/mx2-index.jsp) 和 Xilinx [XC9500XL](http://www.xilinx.com/products/xc9500xl/index.htm) 系列可能是最受欢迎的 3.3 伏 CPLDs。Xilinx 还制造了 [CoolrunnerII](http://www.xilinx.com/products/coolrunner2/) CPLD，但它只采用 TQFP 封装，内核需要单独的 1.8 伏电源。

*套餐*

大多数制造商在业余爱好者友好的 [PLCC 44 封装](http://en.wikipedia.org/wiki/Plastic_leaded_chip_carrier)中提供一个或两个 CPLDs，尽管这种情况开始消失。PLCC 是一个 SOIC 大小的表面贴装芯片，四面都有引脚。PLCC44 插座通常有通孔和 SMD 两种版本。不幸的是，较新的 CPLD 系列开始取消 PLCC 封装，只提供 44 引脚和更大的 TQFP 芯片，如 Xilinx 的 CoolrunnerII。

*开发环境*

大多数制造商提供免费的开发环境，支持使用简单原理图的设计输入，以及 [Verilog](http://en.wikipedia.org/wiki/Verilog) 或 [VHDL](http://en.wikipedia.org/wiki/VHDL) 。许多人不支持免费版本中的最新 FPGAs，但我们只需要 CPLD 部分。Altera 有 [Quartus](https://www.altera.com/support/software/download/sof-download_center.html) ，Xilinx 有 [ISE](http://www.xilinx.com/products/design_resources/design_tool/index.htm) ，Lattice 有 [ispLever](http://www.latticesemi.com/dynamic/index.cfm?fuseaction=view_category&document_type=65&source=topnav) 。Atmel 为 ATF15xx 系列提供了 [ProChip Designer](http://www.atmel.com/dyn/products/tools_card.asp?tool_id=2756) ，但他们只提供 6 个月的试用许可——实际上他们不会给我们。

*程序员*

我们展示的开发板不需要单独的 JTAG 编程器，因为 PIC 微控制器已经对 CPLD 进行了编程。如果要外部编程器，最便宜的是并口编程器:Xilinx 的[Parallel Cable III](http://www.sparkfun.com/commerce/product_info.php?products_id=8460)和 Altera 的[bytle blaster](http://www.sparkfun.com/commerce/product_info.php?products_id=8705)。SparkFun 上有便宜的克隆体和原理图。 [OpenOCD](http://www.sparkfun.com/commerce/product_info.php?products_id=8278) 是一个通用的 USB JTAG 编程器，可以与许多 CPLDs、FPGAs 和 arm 一起工作。

*我们的选择*

我们最终选定了 Xilinx XC9500XL 系列，因为它有一个便宜的开发套件，我们可以在实施整个设计之前用它来测试我们的 JTAG 编程器。

来自 [Digilent](http://www.digilentinc.com/Products/Detail.cfm?Prod=XC2XL&Nav1=Products&Nav2=Programmable) 的 [DO-CPLD-DK](http://www.xilinx.com/products/devkits/DO-CPLD-DK-G.htm) 包括一个 XC9572XL、一个 CoolrunnerII 和并行端口编程器。Nu Horizons 有一些[的非 ROHS 老款，售价 40 美元](https://webapps.nuhorizons.com/storefront/PartSearch.do;jsessionid=916F131647DF384D1C7D5D21956D5A63?PostAction=GO&ItemsPerPage=25&PartNumberHolder=&Mode=initSearch&Commodity=ALL&InStockOnly=FALSE&I6.y=0&Manufacturer=ALLMFG&InStockOnly1=N&PartNumberSearch=DO-CPLD-DK&pSearchType=CompanyPart&PageNum=1&PbFreeOnly1=N&NextPage=1&I6=go&ResultsPerPage=10&PbFreeOnly=FALSE&I6.x=0&prevSearchType=)，但由于他们的信用卡处理脚本中草率的变量类型处理，我们无法在线完成订单。我们试图通过电话做这件事，但他们拒绝在电话上接受这么小的订单，即使是在网站故障期间。最终，在计入新视野过高的运费后，在 Digikey (# [122-1512-ND](http://search.digikey.com/scripts/DkSearch/dksus.dll?Detail?name=122-1512-ND) )支付全价更便宜。我们通常不会提到这一点，但由于只有两个地方购买主板，我们的经验可能值得一提。

**CPLD 开发板**

**![cct-crop-450](img/c6d5298dce3f25ba34b533ddd21e5514.png "cct-crop-450")**

[点击此处查看全尺寸示意图](http://hackaday.com/files/2008/12/cct.png) (PNG)。电路和 PCB 使用免费版的 [Cadsoft Eagle](http://www.cadsoft.de) 设计。这个项目的所有文件都包含在本文末尾链接的项目档案中。

*电路*

PIC [24FJ64GA002](http://www.microchip.com/stellent/idcplg?IdcService=SS_GET_PAGE&nodeId=1335&dDocName=en026374) 微控制器(IC1)为 CPLD 提供用户和编程接口。我们在很多项目中使用这款 4 美元的 PIC，因为外设引脚选择功能使电路板布线变得非常简单。查看我们对 PIC24F 的[介绍，了解更多详情。PIC 需要与 PC 串口通信，所以我们增加了一个廉价的 MAX3232 RS232 收发器。串行接口应该与 USB- >串行适配器一起工作。](http://hackaday.com/2008/09/18/web-server-on-a-business-card-part-1/)

我们选择的 CPLD (IC3)，一个 Xilinx [XC9572XL](http://www.xilinx.com/support/documentation/data_sheets/ds057.pdf) (PDF)，连接在 PIC 和其他几个元件之间。我们可以使用 CPLD 内部的可重编程逻辑在 PIC 和其他芯片之间创建各种各样的电路。*PIC 会用从 PC 串口发来的代码对 CPLD 编程，但是我们还是把 JTAG 管脚带到了一个头部，方便外部调试。*

 *一个 [DS1085 数字可编程振荡器](http://www.maxim-ic.com/quick_view2.cfm/qv_pk/3491) (IC4)产生 8KHz 到 133MHz 之间的时钟频率，增量为 10KHz。这非常类似于我们之前提到的 [DS1077，](http://hackaday.com/2008/11/28/parts-133mhz-162khz-programmable-oscillator-ds1077/)，但是它在所有频率之间有均匀的步进。DS1085 需要 5 伏电源(VR2)。I2C 接口也运行在 5v，所以我们把它连接到 5v 的 PIC 引脚。有可能使用 3.3 伏 66 兆赫 1085L 代替，并删除 5 伏电源。

我们使用廉价的 3.3 伏 SOT223 稳压器(VR1)为大部分电路供电。如果您使用较慢的 1085 l 3.3 伏振荡器，则可以排除 5 伏电源(VR2)。

CPLDs 通常用作存储器控制器，因此我们在开发板上包括了 32K 的 SRAM (IC5)。一个带 5v 容差输入的 3.3v 锁存将存储器输入接口到宽范围的外部电压(IC6)。锁存器输入通过一个 1mω电阻网络(RN1)保持低电平。我们将在下一篇文章中详细讨论这一部分。

*PCB*

该板是一种准单面设计。我们做了一些妥协，这样我们就可以自己制作这个高度实验性的 PCB 原型。我们提出的董事会“是”,为其他顽固分子可能会想蚀刻这个董事会在家里。如果您将 PCB 送到板房，请在生产“真正的”双面板之前尝试纠正这些问题。

CPLD 的一个电源引脚完全没有去耦电容；没有办法在那个区域放置电容器。一个 CPLD 去耦电容和 SRAM 去耦电容是通孔器件。使用这些通孔器件消除了一些跳线。

![backside-450](img/383a17de49b22c34d6eaccd6c3adb811.png "backside-450")

电路板背面的跳线针对单面生产进行了优化，而不是良好的设计实践。我们通过在背面焊接电源总线来伪造双面板。真正的双面板设计应该对电源总线进行布线，以避免信号路径交叉，并包括缺失的去耦电容。

我们使用表面贴装 PLCC 芯片插座，但通孔版本肯定是一个更好的主意。我们原以为 SMD 版本很容易焊接，但结果却是一场噩梦。我们真的希望 CPLD 放在电路板的前面，以获得最酷的演示。带有电镀通孔的双面主板可以在正面有一个通孔插座，但这在我们的单面原型主板上是不可能的。

*零件清单*

*![brd-450](img/a7bc49d162c15513e4bf48f842a997b6.png "brd-450")*

[点击此处查看全尺寸摆放图](http://hackaday.com/files/2008/12/brd.png) (PNG)。【T2

| **部分** | **值** |
| IC1 | [PIC25FJ64GA002](http://www.mouser.com/Search/ProductDetail.aspx?qs=V%2fyyTCAHA4D%2fh5r3CRQDtA%3d%3d) (SOIC) |
| IC2 | MAX3232CSE (SOIC-N) |
| IC3 | XC9572XL-10PCG44C (PLCC) |
| — | [PLCC44 插座](https://www.mouser.com/Search/ProductDetail.aspx?R=PLCC-44-AT-SMTvirtualkey64610000virtualkey737-PLCC-44-AT-SMT)，贴片 |
| IC4 | [DS1085](http://www.maxim-ic.com/quick_view2.cfm/qv_pk/3491) 或 [DS1085L](http://search.digikey.com/scripts/DkSearch/dksus.dll?Detail?name=DS1085LZ-25%2B-ND) (SOIC) |
| IC5 | 32Kx8，3.3v，静态随机存取存储器 |
| IC6 | [74 lvt 573d](https://www.mouser.com/Search/ProductDetail.aspx?R=74LVT573WMvirtualkey51210000virtualkey512-74LVT573WM)(soi) |
| VR1 | 3.3v 调节器， [LD1117S33](https://www.mouser.com/Search/ProductDetail.aspx?R=LD1117S33CTRvirtualkey51120000virtualkey511-LD1117S33C) (SOT223) |
| VR2 | 5v 调节器， [LD1117S50](https://www.mouser.com/Search/ProductDetail.aspx?R=LD1117S50TRvirtualkey51120000virtualkey511-LD1117S50) (SOT223) |
| C1-11，13-17 | [0.1uF 去耦电容](https://www.mouser.com/Search/ProductDetail.aspx?R=C0805C104M5RACTUvirtualkey64600000virtualkey80-C0805C104M5R) (0805) |
| C12 | [0.01uF 电容器](http://www.mouser.com/Search/ProductDetail.aspx?qs=6ARB0lp6jlXWqZF4lhG52w%3d%3d) (0805) |
| C15，16 | [0.1uF 去耦电容](http://www.mouser.com/Search/ProductDetail.aspx?qs=9AX3phJxokWIpR5WRGtIJw%3d%3d)(通孔) |
| C18 | [10uF 钽电容器](http://www.mouser.com/Search/ProductDetail.aspx?R=293D106X96R3A2TE3virtualkey61320000virtualkey74-293D106X96R3A2TE3) (A) |
| R1，2 | [390 欧姆电阻](http://www.mouser.com/Search/ProductDetail.aspx?qs=2BMLUTrrT4P7Xm58YbKmPg%3d%3d) (0805) |
| R3-5 | [2000 欧姆电阻](http://www.mouser.com/Search/ProductDetail.aspx?qs=jBethxrBxZb5NLDetw123g%3d%3d) (0805) |
| RN1 | [1m 欧姆电阻网络](https://www.mouser.com/Search/ProductDetail.aspx?R=4609X-101-105LFvirtualkey65210000virtualkey652-4609X-1LF-1M) (9 针) |
| LED1,2 | [LED](http://www.mouser.com/Search/ProductDetail.aspx?qs=7JStj%2fjQ2SElGv%2fp7IzKlg%3d%3d) (0805) |
| X1 | [db9 母串口连接器](http://www.mouser.com/Search/ProductDetail.aspx?qs=nAEW9fCjKd%2fyLNwP2ItddQ%3d%3d)*未测试 |
| J1 | [2.1 毫米电源插孔](http://www.mouser.com/Search/ProductDetail.aspx?qs=8xMK%2bwDsXhcfMNb/YnnwLQ==) |
| ICSP，JTAG，SV1 | [0.1″引脚接头，直角](http://www.mouser.com/Search/ProductDetail.aspx?R=4-103329-0virtualkey57100000virtualkey571-41033290) |
| S1 | [触摸开关](https://www.mouser.com/Search/ProductDetail.aspx?R=101-0164-EVvirtualkey12040000virtualkey101-0164-EV) (DTSM-6) |

*固件*

固件使用免费演示版的 [PIC C30 编译器](http://www.microchip.com/stellent/idcplg?IdcService=SS_GET_PAGE&nodeId=1406&dDocName=en010065)用 C 编写。在我们对 PIC 24F 系列的[介绍中了解所有关于使用这张 PIC 的信息。固件包含在本文末尾的项目档案中。](http://hackaday.com/2008/09/18/web-server-on-a-business-card-part-1/)

我们需要一种超级简单的方法来与主板上的硬件进行交互，而无需无休止的编译-程序-测试循环。我们制作了一个定制版本的[总线盗版固件](http://hackaday.com/2008/11/19/how-to-the-bus-pirate-universal-serial-interface/)，它提供了一个到 DS1085 时钟芯片(I2C)的简单 ASCII 终端接口、CPLD 编程接口(JTAG)和一个到 CPLD 的三线(SPI)接口。查看总线盗版教程，了解固件使用的简单语法的背景。

最初的总线盗版固件处理几个共享相同管脚的协议。对于 CPLD 版本，我们改变了引脚分配，以适应开发板上的连接。我们还删除了未使用的模块和选项。

**CPLD blinky LED 示例**

我们在 Xilinx 的 ISE 开发环境中准备了几个设计。原理图、引脚布局文件和编译设计(XSVF)包含在本文末尾链接的项目档案中。对 ISE 的全面解释超出了本文的范围；我们发现帮助文件对制作这些例子非常有用。

*![ex1](img/3318347c199812f07cd3e002bd21bc96.png "ex1")
*

第一种设计只是点亮连接到 CPLD 引脚 8 的 LED。

*准备 XSVF 文件*

XSVF 是一种压缩的 JTAG 编程格式，如 Xilinx 在本应用笔记中所述。XSVF 并不局限于对 Xilinx 设备进行编程，它可以为任何提供通用 [BSDL](http://en.wikipedia.org/wiki/Boundary_scan_description_language) JTAG 定义文件的芯片做准备。

从 ISE Design Suite 项目面板的*配置目标设备- > iMPACT* 下打开 iMPACT 编程工具。

*   选择选项*创建边界扫描文件*，并将类型设置为 XSVF。
*   当提示添加设备时，给 XSVF 输出一个文件名，然后添加一个编译的 CPLD 映像(ex1.jed)。
*   您应该会看到包含单个设备的 JTAG 链。

![boundaryscan](img/e7e10e1993afbff549062c2b16817de8.png "boundaryscan")

点击设备并选择程序；iMPACT 会将编程序列记录到 XSVF 文件中。

有了 XSVF 文件，就该打开终端并对 CPLD 编程了。我们喜欢 Windows 上的[万亿术语](http://www.ayera.com/teraterm/)和[大力士](http://www.hw-group.com/products/hercules/index_en.html)。你*必须*在客户端启用 XON/XOFF 流控制来使用 JTAG 接口。开发板终端的默认 PC 端设置为 115200bps，8N1。

> HiZ > m**<–选择模式**
> 1。HiZ
> 2。I2C
> 3。JTAG
> 4。RAW3WIRE
> 模式>3**<–JTAG**
> 900 模式设置
> 602 JTAG 就绪
> JTAG>(2)**<–探针 JTAG 链宏** xxx JTAG 初始化链
> xxx JTAGSM:复位
> xxx JTAGSM:复位- >空闲
> xxx JTAGSM:空闲- >指令寄存器(TMS 延迟一位
> XXX JTAG sm:IR->IDLE
> XXX JTAG sm:IDLE->数据寄存器
> XXX JTAG sm:DR->IDLE
> XXX JTAG sm:RESET
> XXX JTAG sm:RESET->IDLE
> XXX JTAG sm:IDLE->数据寄存器
> xxx JTAG 链报告:
> 0x01 器件
> # 0x 01:0x C9 0x 02 0x 06 09a

在终端中，我们进入模式菜单(m)，并选择 JTAG (3)。宏 2 探测 JTAG 链，在我们的例子中，这只是 CPLD。连锁报告告诉我们，芯片已连接并有响应。[阅读更多关于 JTAG 界面的信息](http://hackaday.com/2008/12/01/bus-pirate-firmware-update-v0c-jtag-and-more/)。

![up](img/2c6e215c8a3c0033c635526258729f7c.png "up")

现在我们可以运行 XSVF 编程器，宏(3)，并以二进制模式从终端*上传 XSVF 文件。第一个例子只是点亮引脚 8 上的 LED。如果 LED 亮起，我们可以验证编程成功。如果你的 LED 不亮，不要绝望；有时 JTAG 程序员卡住了，一个复位宏(1)就会让芯片运行起来。*

![ex1a](img/6da13a21e5969f0acfb76732e4785af2.png "ex1a")

LED 处于最大亮度。

*74LS32/4071 或门，半速闪烁(/2)* 

![ex21](img/21679ca1aef58789ab7d4ec765d13c0d.png "ex21")

CPLD 开发板的一个主要组件是连接到 CPLD 引脚 7 的 1085(L)频率合成器。下一个例子使用了一个[逻辑或门](http://en.wikipedia.org/wiki/OR_gate)，比如一个 [74LS32 或 4071](http://en.wikipedia.org/wiki/OR_gate#Hardware_description_and_pinout) IC，每当时钟信号为高时，使 LED 闪烁。即使在最慢的时钟速率下，闪烁也会太快而看不见，但与第一个例子相比，我们应该得到一个很好的 PWM 调光效果。

> JTAG > m**<–选择模式**
> 1。HiZ
> 2。I2C
> 3。JTAG
> 4。RAW3WIRE
> 模式>2**<–I2C 接口到 DS1085**
> 900 模式设置
> 202 I2C 就绪
> I2C>(1)**<–地址搜索宏**
> xxx 搜索 7bit I2C 地址空间。
> 发现设备在:
> 0xb 0 0x B1**–发现 DS1085 地址**I2C>

像前面一样对 CPLD 进行编程，然后切换到 I2C 模式来访问 DS1085 时钟。我们可以在数据手册中查找器件地址，但通过运行地址搜索宏可以节省几秒钟时间；报告告诉我们芯片响应 0xb0(写)和 0xb1(读)。

> I2C > { 0xb0 0x02 0b 000111111 0b 10000000 }**<–最大预分频器**
> 210 I2C 起始条件
> 220 I2C 写:0xb 0 得到确认:是
> 220 I2C 写:0x 02 得到确认:是
> 220 I2C 写:0x1F 得到确认:是
> 220 I2C 写:0x80 得到确认:是
> 240 I2C 停止条件
> I2C **<–最大分频器**
> 210 I2C 起始条件
> 220 I2C 写:0xB0 得到 ACK:是
> 220 I2C 写:0x01 得到 ACK:是
> 220 I2C 写:0xFF 得到 ACK:是
> 220 I2C 写:0xC0 得到 ACK:是
> 240 I2C 停止条件
> I2C >

DS1085 几乎与我们之前讨论的 ds 1077[一模一样，但它有一个 DAC 控制振荡器，用于所有频率之间的偶数阶。我们使用上面显示的命令将时钟编程为最慢的频率。时钟信号的脉宽调制效应使 LED 变暗。](http://hackaday.com/2008/11/28/parts-133mhz-162khz-programmable-oscillator-ds1077/)

![ex2a](img/b8efa25cd80a742c53f1b9bb0e19cd8e.png "ex2a")

一半亮度的 LED。

*74f 269 16 位同步计数器，缓慢闪烁(/* 65535 *)*

![ex3](img/9347418550ff40304a3c14c84583710a.png "ex3")

我们刚刚用类似于 74LS32 的逻辑或门对 CPLD 进行了编程。现在，我们将使用一个 16 位计数器对芯片进行重新编程，就像两个级联的[74f 269](http://www.mouser.com/Search/ProductDetail.aspx?qs=lp01TYqEl4mFnzVVG95LCg%3d%3d)一样。两个 74F269 Ics 每个 1.15 美元，比 XC9572XL CPLD 贵。16 位计数器每 65535 个节拍翻转一次，因此连接到最后一位的 LED 将每 65535/2 个节拍切换一次。

现在我们可以看到 CPLDs 很酷的部分了。CPLD 就像一个可编程的试验板；我们只是弹出了 74LS32，放入了一个 74F269，没有买零件，没有看数据表，没有蚀刻，没有布线等。连接到 CPLD 的微控制器可以重新配置自己的电路板，以修复错误、增加功能或将其重新用于完全不同的应用。

我们像以前一样上传新的设计，但现在时钟除以 65535，LED 每秒切换一次。

[https://www.youtube.com/embed/wNfJKHV0ylg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/wNfJKHV0ylg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

**更进一步**
下次我们将看看分立的 7400 系列逻辑芯片，并在 CPLD 中实现大量这类芯片，以制作高速总线嗅探器和逻辑分析仪。

**下载:** [bitclone.v1.zip](http://blog.mahalo.com/hackaday/howto/bitclone.v1.zip)*
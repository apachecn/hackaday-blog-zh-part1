# 如何:使用 Linux 编程图片

> 原文：<https://hackaday.com/2010/11/03/how-to-program-pics-using-linux/>

可以说，微芯片的 PIC 微控制器在这里没有得到足够的帖子。对我们中的一些人来说，一个缺点是 Linux 对 PICs 的支持不是很广为人知。信息就在那里，但是没有人列出从编写 C 代码到编写芯片的过程。面向熟悉微控制器、基本电路、C 编程语言并能阅读数据手册的 Linux 用户，本指南将帮助您快速使用 Linux 编程 PIC。

**编译器:**

[小型设备 C 编译器](http://sdcc.sourceforge.net/)，sdcc 将用于创建。编程 PIC 所需的十六进制文件。对 PICs 的支持仍在增长，并且仍处于测试阶段，所以请注意，本文的代码和芯片之外的东西可能需要一些调试。然而，就像其他开源项目一样，更多的贡献用户将会帮助这个项目。最重要的是，它是免费的，具有到 Windows 和 MacOS X 的端口，这是一个可以处理许多架构和设备的编译器，而没有仅限于 Windows 的付费编译器免费版本的程序限制。Sdcc 可以通过各种发行版的包管理器获得，包括 Ubuntu 和 Fedora。

要在 Ubuntu 上安装 sdcc:

```
sudo apt-get install sdcc
```

要在 Fedora 上安装 sdcc:

```
sudo yum install sdcc
```

**筹码:**

编写本教程时使用了三种不同的 PIC 芯片:40 针 [PIC16F887](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en026561) ，14 针 [PIC16F688](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en010215) ，8 针 [PIC12F675](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en010114) 。你可以跟随任何这些芯片以及其他芯片。

**程序员:**

我们将使用两个程序员，Olimex 的 PICStart+兼容 [PIC-MCP-USB](http://olimex.com/dev/pic-mcp-usb.html) 程序员，和 Microchip 的 [PICkit 2](http://www.microchip.com/stellent/idcplg?IdcService=SS_GET_PAGE&nodeId=1406&dDocName=en023805) 。两个程序员都已经过测试，可以与这里使用的三个芯片一起工作。

PICStart+程序员使用 picp 程序。几乎所有兼容 PICStart+的程序员都可以使用 picp。轻松安装在 Ubuntu 中:

```

&lt;pre&gt;sudo apt-get install picp
```

对于 Fedora 和其他发行版，可能需要从源代码下载并安装它。因此，在您选择的空目录中:

```
wget http://home.pacbell.net/theposts/picmicro/picp-0.6.8.tar.gz
tar -xzf picp-0.6.8.tar.gz
cd picp-0.6.8
make
sudo make install
```

源代码在[Jeff Post]的[PIC 程序员开发工具](http://home.pacbell.net/theposts/picmicro/)页面上，还有其他编程选项。

如果您将使用 PIC16F887 和 picp，您将需要通过添加以下行来修改/etc/picp/picdevrc 文件:

```
[16F887]
0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0
PICSTART

[16F887:def]
20 00 3f ff 3f ff 00 7f
00 7f 3f ff 3f ff 00 ff
00 ff 00 00 00 00 00 00
0D 10 20 00 04 20 07 02
00 00 01 00 00 00 00 00
00 01 22 0f

[16F887:defx]
3f ff 07 00 00 00 00 00
00 00 00 00 00 00 00 00
3f ff 07 00 00 00 00 00
00 00 00 00 00 00 00 00
```

以上几行是在【Al Williams】的[帖子](http://www.drdobbs.com/blog/archives/2010/04/microcontroller.html)中找到的 PIC16F886 的修改参数。对于不在/etc/picp/picdevrc 中的芯片，需要将附加参数添加到/etc/picp/picdevrc 中。

PICkit 2 程序员将与另一个名为 pk2cmd 的程序合作，该程序由 Microchip [在这里](http://www.microchip.com/stellent/idcplg?IdcService=SS_GET_PAGE&nodeId=1406&dDocName=en023805&redirects=pickit2)托管。您需要从源代码安装 pk2cmd。因此，在您选择的目录中:

```
wget http://ww1.microchip.com/downloads/en/DeviceDoc/pk2cmdv1.20LinuxMacSource.tar.gz
tar -xzf pk2cmdv1.20LinuxMacSource.tar.gz
cd pk2cmdv1.20LinuxMacSource
make linux
sudo make install
```

请注意，Microchip 宣传 PICkit 3 是 PICkit 2 的替代品。它不是 PICkit 2 的替代品，因为 PICkit 3 没有 Linux 驱动程序，所以不要认为 PICkit 3 可以在 Linux 上工作就购买它。

还有另外一个程序声称可以和一系列 DIY PIC 程序员合作: [PICPgm](http://www.members.aon.at/electronics/pic/picpgm/index.html) 。在这一点上，我们还没有尝试过这个程序或任何 DIY 程序员。我们知道还有其他 PIC 程序员，有便宜的也有贵的，只是没有提到。也许需要写一篇 PIC 程序员综述。

**代码:**

这个操作的代码是一种使用 led 的 hello world 程序。这方面的代码托管在 Github 上，你可以跟随 blink.c 文件的 [PIC16F887](http://github.com/Hack-a-Day/PIC-Blink/tree/master/16f887/) 、 [PIC16F688](http://github.com/Hack-a-Day/PIC-Blink/tree/master/16f688/) 或 [PIC12F675](http://github.com/Hack-a-Day/PIC-Blink/tree/master/12f675/) 。还包括正在工作的。十六进制文件。下面是 PIC16F887 代码，作为我们完成每个主要操作的参考:

```
//Simple program to get started programming
//PIC microcontrollers in Linux.
//Written by Devlin Thyne.
//Released to the public domain.

#include &quot;pic/pic16f887.h&quot;

//Use these configuration words:
//0x2ff4 0x3fff

//Set the configuration words:
unsigned int at _CONFIG1 configWord1 = 0x2FF4;
unsigned int at _CONFIG2 configWord2 = 0x3fff;

//To compile:
//sdcc -mpic14 -p16f887 blink.c

//To program the chip using picp:
//Assuming /dev/ttyUSB0 is the serial port.

//Erase the chip:
//picp /dev/ttyUSB0 16f887 -ef

//Write the program:
//picp /dev/ttyUSB0 16f887 -wp blink.hex

//Write the configuration words (optional):
//picp /dev/ttyUSB0 16f887 -wc 0x2ff4 0x3fff

//Doing it all at once: erasing, programming, and reading back config words:
//picp /dev/ttyUSB0 16f887 -ef -wp blink.hex -rc

//To program the chip using pk2cmd:
//pk2cmd -M -PPIC16f887 -Fblink.hex

//Setup variables
unsigned char ucharCount = 0;
unsigned int uintDelayCount = 0;

void main(void)
{
	//Set PORTC to all outputs
	TRISC = 0x00;

	ucharCount = 0;
	uintDelayCount = 0;

	//Loop forever
	while ( 1 )
	{
		//Delay Loop
		while ( uintDelayCount &lt; 10000 )
		{
			//Increment the loop counter
			uintDelayCount++;
		}

		//Reset delay loop counter
		uintDelayCount = 0;

		//Increment the count
		ucharCount++;

		//Display the count on the PORTC pins
		PORTC = ucharCount;

	}

}

```

第一行是您将使用的特定芯片的头文件的#include。它告诉编译器哪些寄存器可用，以及它们在内存中的位置。在大多数系统中，头文件位于/usr/share/sdcc/include 中。

然后我们设置配置字或字熔丝。它们只能在芯片编程时写入，但我们可以在这里定义它们，这样以后就不必手动编程了。PIC16F887 的头文件中定义了配置字的地址，如 _CONFIG1 和 _CONFIG2。PIC16F688 和 PIC12F675 的报头中没有定义配置字地址(我们说过 sdcc 处于测试阶段，不是吗？)，所以我们就用配置字的地址:0x2007。配置字特定于芯片型号和应用，在各芯片数据手册的“CPU 的特殊功能”一章中有所描述。在 blink.c 示例中，配置字只是一个 16 位的十六进制字，但是通过将配置选项进行 and 运算，可以使这个字更易于阅读。查看芯片的头文件，了解选项的名称。

接下来，我们设置一些全局变量，一个用于 led 上输出的值，另一个用于延迟计数器。

在 void main()中，我们将 PORTC 三态寄存器 TRISC 设置为所有输出。PIC12F675 只有一个端口 GPIO，其三态寄存器为 TRISIO。设置三态寄存器后，我们用 while(1)进入一个无限循环。环路内部是一个延迟环路，这样我们就可以看到 led 的变化。延迟循环之后，显示计数器递增，然后写入 PORTC(或 GPIO ),在 led 上显示。

**编译代码:**

现在我们已经审查了代码，是时候把它变成 PIC 可以使用的东西了。sdcc 会拿 blink.c 文件做一堆文件。其中一个文件是 blink.hex，这是 PIC 设备程序员将要写入 PIC 的内容。方法如下:

对于 PIC16F887:

```
sdcc -mpic14 -p16f887 blink.c
```

对于 PIC16F688:

```
sdcc -mpic14 -p16f688 blink.c
```

对于 PIC12F675:

```
sdcc -mpic14 -p12f675 blink.c
```

-mpic14 选项告诉 sdcc，它将针对 PIC16 和 PIC12 系列的 14 位指令进行编译。第二个选项是编译代码的具体芯片。最后一行是包含将要编译的 C 代码的文件。

**芯片编程:**

要对芯片进行编程，你需要带着你的设备编程器，把你想载入程序的芯片连接起来。除非您使用的是 PIC-MCP-USB 之类的插座编程器，否则您需要查阅编程器和要编程的芯片的数据表，以便正确连接。正确连接后，您需要运行程序来运行编程器:

对于/dev/ttyUSB0 上的 PICStart+程序员，对 PIC16F887 进行编程:

```
picp /dev/ttyUSB0 16f887 -ef -wp blink.hex -rc
```

对于 PICkit 2 程序员编程 PIC16F887:

```
pk2cmd -M -PPIC16f887 -Fblink.hex
```

如果您正在对另一个芯片进行编程，或者 PICStart+编程器在/dev/ttyUSB0 之外的端口上，您将需要对命令进行相应的更改。

注意:为 PIC16F887 提供的代码禁用低压编程。一些可用但没有直接提到的编程器仅执行低电压编程。如果您有这些程序员中的一个，您将需要更改代码，以便配置字中的低电压编程位允许低电压编程。正常工作期间，微控制器上的低压编程引脚也需要拉低。

**接通电路:**

这个项目的电路和提供的代码非常简单。以下是三种芯片的原理图:

![](img/ab2abd15731e82f6ec1baffac009062f.png "blink_schematic")

首先，将 Vdd 引脚连接到 4.5 伏至 6 伏的正电压源，Vss 引脚接地。40 引脚 PIC16F887 和 14 引脚 PIC16F688 在其主 clear 引脚上都需要一个上拉电阻。在任一或所有 PORTC 引脚(或 PIC12F675 的 GPIO 引脚)上，将带限流电阻的 led 接地。请注意，PIC12F675 的引脚 4 只是一个输入，不会点亮 LED。所使用的三个芯片的任何引脚的电流都被限制在 20mA，因此限流电阻对于大多数廉价的 jellybean LEDs 来说是可选的。当电路通电时，您应该会看到闪烁的 led。指示灯应亮起至二进制计数。

轮到你了！

现在我们已经给你一个使用 Linux 编程 PICs 的开始，我们希望看到更多的项目使用这些芯片和我们上面提到的工具。虽然本文是为 Linux 用户编写的，但是 Windows 和 MacOS X 用户应该能够使用 sdcc 来满足他们的 PIC 编程需求。

图片信息:燕尾服的标志是由拉里·尤因、西蒙·布迪格和安雅·格文斯基通过[维基共享](http://upload.wikimedia.org/wikipedia/commons/3/35/Tux.svg)设计的。微芯片标识是[微芯片技术有限公司](http://www.microchip.com/)的注册商标。

[Development Tools for PIC programmers](http://home.pacbell.net/theposts/picmicro/)
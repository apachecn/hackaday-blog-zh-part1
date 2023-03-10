# 如何:超级简单的串行终端

> 原文：<https://hackaday.com/2008/05/29/how-to-super-simple-serial-terminal/>

![](img/1f3e75a6990144401751f701c6c1844f.png)

这个黑客展示了如何用键盘、LCD 屏幕和 8 位微控制器制作一个哑终端。有时，当你不得不挽救一个出问题的无头服务器时，或者如果你正在用 WRT 构建一台小型计算机时，或者如果你只想学习如何用微控制器操作键盘和 LCD 屏幕时，便携式哑终端会很方便。这个超级简单的串行终端将使用 RS-232 来控制一个无头的 linux 系统。此外，你可能想直接从终端查看一些[命令行界面程序](http://tuxtraining.com/2008/05/15/welcome-to-the-linux-command-line-interface-desktop/)，允许网页浏览、AIM 和 IRC 聊天等，但没有什么能比用这个设备[跟踪你的披萨](http://random.noflashlight.com/)更好的了。

这里讨论的 Linux 系统是 Linux Mint。这是一个基于 Ubuntu 的年轻发行版，最近获得了很多关注，尽管这些原则可以用于其他 Linux 发行版。

硬件:
对于这个操作方法，我们将使用一个运行在 16MHz 的 ATMEGA128。由于这个设备将通过 RS-232 通信，我们需要一个电平转换器。RS-232 使用 12 伏信号，这将烧毁我们的 5V 微控制器。为了解决这个问题，我们将使用 MAX233 芯片。

![MAX233 schematic](img/69f5e81974b8f1b9ae9df4833724407a.png)

这是电平转换器电路的原理图。

![Max233 layout](img/222581bc064d4a3d16cc1217f03a6256.png)This is an example layout.

我在这个项目中使用 [ET-AVR 印章模块](http://www.futurlec.com/ET-AVR_Stamp.shtml)和[印章板](http://www.futurlec.com/ET-AVR_Stamp_Board.shtml)。这个开发板很便宜，而且内置了基本功能。我将使用板载电源和 MAX232 RS-232 电平转换器。

本项目选用的液晶显示器是非常常见的 4×20 字符液晶显示器。这些液晶显示器真的很容易控制[与一个微控制器](http://www.maxmon.com/lcd2.PDF) (PDF)，和[甚至没有一个](http://www.maxmon.com/lcd1.PDF) (PDF)。HD44780 芯片支持多种位宽的并行编程、命令甚至自定义字符。这种液晶显示器有很好的软件库，这使得它更容易使用。

一个更有吸引力的选择是图形 LCD，我们的库也支持它，但是我们手头只有字符 LCD。

一个普通的 AT 键盘将被用于字符输入，这些也不难找到，你可能在某个地方有一个额外的键盘。

如果你不想买 ET-AVR，你可以自己为这个黑客建立电路。(点击查看大图)。

[![](img/a42d54ad10d4405c909eef63b3022f7b.png)](http://hackaday.com/wp-content/uploads/2008/05/full_schematic.png)

上述电路的完整零件清单:

| 部分 | Jameco 零件号 | Futurlec 零件号 |
| Atmega128 集成电路 | [1406045](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=1406045) | [ATMEGA128-16AC](http://www.futurlec.com/Atmel/ATMEGA128.shtml) |
| 16MHz 晶体 | [14453](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=14453&productId=14453) | [CRY16.000](http://www.futurlec.com/Crystals/CRY16000.shtml) |
| DB9 连接器(阴) | [15771](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=15771&productId=15771) | [dsubcf 9](http://www.futurlec.com/Connectors/DSUBSCF9.shtml) |
| DB9 发动机罩 | [1719922](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=1719922) | [DSUBCH9](http://www.futurlec.com/Connectors/DSUBCH9.shtml) |
| MAX233 电平转换器 | [106163](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=106163&productId=106163) | [MAX233CPP](http://www.futurlec.com/Maxim/MAX233CPP.shtml) |
| 22pF 电容(x's2) | [332340](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=332340) | [C022PC](http://www.futurlec.com/Capacitors/C022PC.shtml) |
| 0.1uF 陶瓷电容器 | [151118](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=151118&productId=151118) | [C100UC](http://www.futurlec.com/Capacitors/C100UC.shtml) |
| 220 欧姆电阻器 | [690700](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=690700&productId=690700) | [R220R14W](http://www.futurlec.com/Res14W.shtml) |
| 10k 欧姆电阻器 | [691104](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=691104&productId=691104) | [R010K14W](http://www.futurlec.com/Res14W.shtml) |
| 10k 电位计 | [255522](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=255522&productId=255522) | [TRIM10K](http://www.futurlec.com/Potentiometers/TRIM10K.shtml) |
| 6 引脚 Minidin(可选) | [310789](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=310789) (切) | [迷你 6PC](http://www.futurlec.com/DIN-S-VHS.shtml) |
| 4×20 字符液晶显示器 | [658873](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=658873&productId=658873) | [BLUELCD20X4BL](http://www.futurlec.com/LED/BLUELCD16x2BL.shtml) |
| 在键盘上 | [319812](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=319812&productId=319812) |

如果您想使用 ET-AVR 或其它开发板，可以使用以下器件清单:

| 部分 | Jameco 零件号 | Futurlec 零件号 |
| ET-AVR 图章模块 |  | [ET-AVR 冲压](http://www.futurlec.com/ET-AVR_Stamp.shtml) |
| ET-AVR 邮票板 |  | [ET-AVR 冲压](http://www.futurlec.com/ET-AVR_Stamp.shtml) |
| ET-AVR 编程器 |  | [ET-AVR ISP](http://www.futurlec.com/ET-AVR_Stamp.shtml) |
|  |  |  |
| DB9 连接器(阴) | [15771](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=15771&productId=15771) | [dsubcf 9](http://www.futurlec.com/Connectors/DSUBSCF9.shtml) |
| DB9 发动机罩 | [1719922](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=1719922) | [DSUBCH9](http://www.futurlec.com/Connectors/DSUBCH9.shtml) |
| 220 欧姆电阻器 | [690700](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=690700&productId=690700) | [R220R14W](http://www.futurlec.com/Res14W.shtml) |
| 10k 欧姆电阻器 | [691104](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=691104&productId=691104) | [R010K14W](http://www.futurlec.com/Res14W.shtml) |
| 10k 电位计 | [255522](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=255522&productId=255522) | [TRIM10K](http://www.futurlec.com/Potentiometers/TRIM10K.shtml) |
| 6 引脚 Minidin(可选) | [310789](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=310789) (切) | [迷你 6PC](http://www.futurlec.com/DIN-S-VHS.shtml) |
| 4×20 字符液晶显示器 | [658873](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=658873&productId=658873) | [BLUELCD20X4BL](http://www.futurlec.com/LED/BLUELCD16x2BL.shtml) |
| 在键盘上 | [319812](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&pa=319812&productId=319812) |

软件 :
我们用的是安装了 [AVRlib](http://hubbard.engr.scu.edu/avr/avrlib/) 的 [WinAVR](http://winavr.sourceforge.net/) 。AVRlib 是一组库，可以运行伺服系统，设置 A/D 转换等。它可以做你需要它做的任何事情。要安装 WinAVR，[从这里获取最新版本](http://sourceforge.net/project/showfiles.php?group_id=68108&package_id=66543&release_id=598832)，并按照安装程序上的指示进行操作。我们通常不按照这里的说明安装 AVRlib，而是将它放入 WinAVR 安装的 include 文件夹中，该文件夹位于 C:/WinAVR/avr/include/AVRlib。这样，您包含的标题更容易看到和找到。

例如#包括

一旦完成，你就可以打开程序员的记事本开始编码了。我们已经为这个项目写好了[的代码(为一些喜欢冒险的读者留下了修改的空间)。](http://projectbloc.com/Terminal.zip)

键盘协议:
键盘使用简单的串行通信设置。只有两条线，数据和时钟。一般来说，在你按下一个键之前，这些线路(时钟和数据线都是高电平)上什么也没有发生。一旦按下一个键，数据线就变为低电平。此后不久，时钟下降。时钟将总共运行 11 个周期。此时，必须在时钟下降沿从数据线读取数据。数据从键盘反向发送(最低有效位优先)，带有一个奇偶校验位和一个停止位。

整个数据包是:

| 开始位 | D0 | D1 | D2 | D3 | D4 | D5 | D6 | D7 | 平价 | 停止位 |

在这个简单的攻击中，起始位、奇偶校验位和停止位将被忽略。

在键盘发送一个键的扫描码之后，当该键被释放时，它也发送 0xF0。

看一个例子，比较好理解。想象一下键盘上的“m”键被按下了。数据线变为低电平以产生起始位，然后发送扫描码，首先是 LSB，然后是奇偶校验(奇数奇偶校验)和停止位。因为“m”的扫描码是 0x3A，所以我们应该在包的数据部分得到该值。同样，键盘首先发送数据 LSB，因此由于我们期待 0x3A(二进制 00111010 ),我们实际上将得到相反的结果(二进制 010111100)。请记住从右向左读取数据位，以便更容易看到扫描码。在数据之后，我们将在奇偶校验位中收到一个 1，使包成为奇数奇偶校验位，然后是停止位。发送扫描代码后，松开按钮时，键盘将发送另一个扫描代码。这个发布代码总是 0xF0，可以忽略，它在代码中处理。

所以当按下“m”时，键盘会发出:

| Zero | Zero | one | Zero | one | one | one | Zero | Zero | one | one | = 'm '或 0x3A |
| 开始位 | D0 | D1 | D2 | D3 | D4 | D5 | D6 | D7 | 平价 | 停止位 |  |

| Zero | Zero | Zero | Zero | Zero | one | one | one | one | one | one | =释放(0xF0) |
| 开始位 | D0 | D1 | D2 | D3 | D4 | D5 | D6 | D7 | 平价 | 停止位 |  |

关于如何工作的更高级的解释可以在别处找到[。](http://www.beyondlogic.org/keyboard/keybrd.htm)

我们必须只在时钟下降时读取数据线，以确保获得良好的数据。我们尝试使用 ATMEGA128 上的外部中断和 AVRlib 的外部中断例程来实现这一点。事实证明，这比需要的要复杂得多。然后我们想起不久前 Sparkfun 在他们的网站上发布了某种使用 AVR 的键盘小工具。他们的键盘读取程序代码非常简单，根本没有使用外部中断。我们修改了 Sparkfun 的 Nathan 为他们的[按键计数器部件](http://www.sparkfun.com/commerce/present.php?p=Key-Counter)编写的“getkey”例程。

一旦扫描码被读取，它们必须被转换成有用的东西。据我们所知，键盘扫描码与 ASCII 码没有数学关系，所以我们建立了两个 ASCII 列表。每个列表实际上是一个 ASCII 字符数组。一个列表包含移位字符的所有值，另一个列表包含未移位字符的值。我们查找每个扫描码的 ASCII 值，并将它们按顺序放入数组中。这提供了一种简单的方法来返回给定扫描码的 ASCII 值。

例如，当你按下“h”键时，程序捕捉扫描代码 0x33，并转到数组中的第 0x33 个值，这个值恰好是 0x68，即“h”的 ASCII 值。产生的 ASCII 字符被发送到 LCD 和 UART，两者都由 AVRlib 控制，以便于处理。

数组中有许多 0 用作占位符。这是因为 AVRlib 会自动向 LCD 的 CG RAM 地址 0x 00(NULL 的 ASCII 码)加载一个字符。基本上，如果这些代码被发送到液晶显示器，它看起来就像乱码一样。我们使用“0 ”,这样我们就可以知道在这种情况下会发生什么。

目前不支持扩展密钥。功能键(F1-F12)被赋予了在 Linux 中使用的正常功能，但不被程序的其余部分支持。例如，在 Linux 中，按 F1 发送与“Ctrl+X”相同的命令。查看其他功能键的代码。不是所有的键都被使用(故意的),所以如果你想给终端添加自定义功能，有足够的空间。

UART:
atmega 128 有两个 UART 端口。使用第一个(UART0)字符可以从 AVR 发送到终端，反之亦然。UART 被初始化并设置为 9600 波特、8 位、无奇偶校验、一个停止位。确保将终端程序设置为相同的设置。我们稍后将修改 Linux 以确保设置匹配。

有了 AVRlib，使用 UART 变得轻而易举。只需初始化它，给它一个波特率，就可以开始发送和接收数据了。

摆弄 Linux:
你要么需要在 Linux 机器上安装一个显示器和键盘，要么在机器上安装 SSH 并进行设置。

网上有[几本](http://www.howtoforge.com/setting_up_a_serial_console) [好的](http://znark.com/tech/serialconsole.html) [指南](http://www.vanemery.com/Linux/Serial/serial-console.html)关于设置 Linux 机器使用串口控制台。然而，Linux Mint 是基于 Ubuntu 的，这与大多数操作系统在启动时设置串行访问有点不同。本指南解释了基础知识，但是我们需要稍微调整一下，让它为我们服务。

首先你需要弄清楚你的机器上是否有串口。看后面，试着找一个 DB9 的连接器。

![](img/50279c8c03a1eb84c243da5aada1a95d.png)

现在你需要弄清楚你的机器上的串行端口是什么。在机器上打开终端窗口，输入以下命令:

= = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
`$ dmesg | grep tty`
= = = = = = = = = = = = = = = = = = = = = = = = = = = =

输出将是这样的:
= = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
`[ 35.742036] serial8250: ttyS0 at I/O 0x3f8 (irq = 4) is a 16550A
[ 35.742435] 00:08: ttyS0 at I/O 0x3f8 (irq = 4) is a 16550A`
= = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
这表明我们在这台特定的机器上有 1 个串口。而且叫“ttyS0”。

现在，我们必须设置登录串行控制台的方式。这是由 getty 进程处理的。此过程将打开您指定的 tty 端口并发送登录提示。

为此，我们需要在/etc/event.d 中创建一个名为 ttyS0 的文件。打开您最喜欢的文本编辑器，键入以下内容:

= = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
`start on runlevel 2
start on runlevel 3
start on runlevel 4
start on runlevel 5`

运行级 0 停止
运行级 1 停止
运行级 6 停止

重生
exec/sbin/Getty-L 115200 ttys 0 vt 102
= = = = = = = = = = = = = = = = = = = = = = = = = = = =

现在将这个文件保存为/etc/event.d/ttyS0。

现在，这对于机器上的普通用户来说很好，但是要以 root 用户的身份做事，必须在/etc/securetty 文件中有一个 pass。转到/etc 并使用文本编辑器打开 securetty 文件。(那是“securetty”，不是“security”)。在该文件中，键入“ttyS0”。这允许该端口拥有根用户访问权限。保存文件并关闭编辑器。现在，最后一步是让控制台在机器启动时可用。为此，我们必须修改 grub 引导程序。您必须转到/boot/grub 并编辑 menu.lst 文件。首先转到那里，创建 menu.lst 文件的干净副本:

= = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
`cp /boot/grub/menu.lst /boot/grub/menu_orig.lst`
= = = = = = = = = = = = = = = = = = = = = = = = = = = =

现在，在文本编辑器中打开 menu.lst 并键入以下内容

= = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
`serial --unit=0 --speed=9600 --word=8 --parity=no --stop=1
terminal --timeout=10 serial console`
= = = = = = = = = = = = = = = = = = = = = = = = = = = =

第一行告诉 grub，您希望使用 ttys 0(–unit = 0)，波特率为 9600(–speed = 9600)，使用 8 n1(–word = 8–parity = no–stop = 1)

第二行命令在串行控制台和屏幕(如果有的话)上显示终端。

如果您想在串行控制台上查看引导消息，您可以在该文件中的“kernel”行的末尾添加以下行:

= = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
`console=ttyS0,9600n8 console=tty0`
= = = = = = = = = = = = = = = = = = = = = = = = = = = =

保存此文件。

现在，当您启动时，您应该可以访问串行控制台，但是默认的 shell 是 bash。这很糟糕，因为 bash 在执行命令时会发送很多额外的字符。在许多终端上，这些字符被从显示中剥离出来，然而，在 LCD 上很难做到这一点，而且只有 80 个字符，我们在屏幕上没有太多空间。我们需要用简单一点的东西。

[Fabienne]建议用 sh 做外壳，去掉 bash 的怪角色。这在测试期间有效，所以我们把它作为机器上的默认 shell。这允许它在启动过程中自动加载，使它更容易与我们刚刚制作的设备一起使用。为此，只需打开一个终端窗口并键入:

= = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
`chsh`
= = = = = = = = = = = = = = = = = = = = = = = = = = = =

这将要求您输入密码。一旦你进入它，你会看到这样一个屏幕:

= = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
`Changing the login shell for <username>
Enter the new value, or press ENTER for the default.
Login shell [/bin/bash]`
= = = = = = = = = = = = = = = = = = = = = = = = = = = =

此时，您需要键入以下内容:

= = = = = = = = = = = = = = = = = = = = = = = = = = = = = = = =
`/bin/sh` = = = = = = = = = = = = = = = = = = = = = = = = = =

再次按回车键将保存这个新设置。

现在，您已经准备好连接设备，并看到它的行动！

连接设备:
你可以在 windows 机器上玩这个，但它的真正威力是在 Linux 机器上。如果你有一台 Windows 机器，你现在可以通过超级终端或其他[终端](http://realterm.sourceforge.net/) [程序](http://hp.vector.co.jp/authors/VA002416/teraterm.html)与设备通信。只需将串行电缆插入 DB9 插头，并如上所述将端子设置为 8n1。在键盘上打字将显示在终端和 LCD 上。

要在 Linux 机器上使用它，请将 DB9 插入计算机的串行端口，然后打开机器。应该发生第一件事是系统会要求你“按任意键继续”。按键盘上的任何键开始加载操作系统。按键后，您应该会看到屏幕上滚动显示所有启动信息。一旦停止，点击“输入”。这将打开登录屏幕(还记得设置 getty 吗？).

![](img/0cc253f9aae54d354d7b0edc39dfaceb.png)

键入您的登录名，按 enter 键，然后输入您的密码。与大多数 Linux 系统一样，在密码字段中输入密码不会打印到屏幕上。继续并获得您的主目录的“ls”。请注意，屏幕不够大，无法显示所有文件和文件夹。我们已经编写了一个简单的屏幕缓冲区，它将显示屏幕上显示的前 4 行。这类似于“向上翻页”的功能。

现在你有了代码和硬件列表，让我们看看你能用它做什么。
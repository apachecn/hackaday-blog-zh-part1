# 如何:网络涂鸦墙

> 原文：<https://hackaday.com/2008/10/02/how-to-networked-graffiti-wall/>

[https://www.youtube.com/embed/G8KprTVbHD4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G8KprTVbHD4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

想知道我们上周在一个名片项目上用 web 服务器做了什么吗？它为一面巨大的 LED 涂鸦墙供电。用户可以使用[在线设计师](http://graffiti-me.appspot.com/seq.html)提交动画。你也可以[观看用户动画的直播。在线界面运行在](http://graffiti-me.appspot.com)[谷歌应用引擎](http://code.google.com/appengine/)上，以获得最大的可伸缩性和弹性。

在今天的 How-to 中，我们涵盖了构建你自己的网络涂鸦墙的所有细节。

**概念概述**

![](img/4de210fc2c7aabd10d72e3f757c0e19f.png "graffiti-wall-diagram-previ")

涂鸦序列是用 JavaScript 动画设计师在线设计的。完成的序列被验证并存储在数据库中；我们为 PHP/MYSQL 和 Google Apps (Python)做了数据库后端。序列由一个简单的[数据馈送 API](http://graffiti-me.appspot.com/feed.php?max=1&last=0) 整合而成。我们的[迷你网络服务器](http://hackaday.com/2008/09/25/web-server-on-a-business-card-part-2/)从提要中检索动画序列，并将它们缓存在 SD 卡上。最后，序列显示在一个巨大的 LED 矩阵上。

**大型低分辨率显示器**
我们的涂鸦显示器是一个 1 米见方、5×5 的 led 矩阵。它的灵感来自几年前人居出售的[蠢朋克茶几。蠢朋克桌子产生了许多 DIY 复制品，包括这张制作蠢朋克桌子的极好的说明书。随着时间的推移，这种趋势演变成几种排列方式，比如我们的](http://www.guardian.co.uk/lifeandstyle/2004/jul/09/homes)[“蠢朋克桌”](http://www.instructables.com/id/Daft-Punk-Table-Replica-Graphics-Controller/)。考虑到这些令人眼花缭乱的大家具，我们寻找了一个比“蠢朋克桌”更好的词。我们想出了“大，低分辨率显示器”或简称 LLRD(发音为“猪油”)。

![](img/3007d3fef6dfa5d8a06edbeae9199e73.png "dpt-couch-2")

最初的蠢朋克表随机闪烁，或者随着音乐的节奏闪烁。[Mathieu Roncheau]的[复制表](http://www.dailymotion.com/miniDaftPunkTable)将动画序列存储在 EEPROM 中。我们的第一个设计更进一步，将动画文件存储在 FAT 格式的 SD 卡上。现在，我们已经将设计者放到了网上，这样我们就可以通过互联网获取用户提交的动画序列。

**在线界面**
LLRD 的涂鸦动画是用一个简单的 JavaScript 序列生成器创建的。观看用户提交动画的[直播](http://graffiti-me.appspot.com/)，或者[亲自尝试](http://graffiti-me.appspot.com/seq.html)。涂鸦序列设计器和编写的数据后端，针对 PHP/MYSQL 和 Google App Engine，包含在[项目档案](http://blog.mahalo.com/hackaday/howto/graffitiV1.zip)中。

![](img/08c0f5ef89615af1965fbe5a81b2e348.png "designer-screenshot")

JavaScript 涂鸦序列设计器易于使用:

*   单击框来切换动画每一帧中显示的 led。
*   使用箭头按钮在框架之间导航。
*   备份和恢复工具提供了一种将序列存储在本地文本文件中的简单方法。

“添加文本框架”使用位图字体插入字符框架。如果你不喜欢默认字体，就创建一个新的:

*   单击“编辑字体”按钮加载现有字体。
*   进行修改。
*   单击“更新字体”用新框架替换默认字体。

*字体*数组是空格和 Z (ASCII 字符 32 到 90，"！"之间的 [ASCII 字符](http://www.asciitable.com/)的位图查找表#$% & '()*+，-。/0123456789:;< = >？@ABCDEFGHIJKLMNOPQRSTUVWXYZ”)。要永久添加新字体，只需将更新后的字体集粘贴到 JavaScript 代码中的“font=”变量之后。备份框中的“字体格式”选项将生成可变格式的位图，可以粘贴到现有字体上。

当你完成一个动画后，在作者框中输入你的名字，然后点击提交。将生成序列码并发送给服务器。

基于 JavaScript 的在线涂鸦设计器的灵感来自于 Mathieu Roncheau 的离线版本。【Mathieu】的 Delphi 源代码和可执行文件[存档在这里](http://www.instructables.com/id/Daft-Punk-Table-Replica-Graphics-Controller/)。我们基于 JavaScript 的设计器有一些额外的特性，是基于浏览器的，它不需要你运行一个未知的。exe 文件。尽管设计者打算在网络上运行，但他也将从你计算机上的本地副本开始工作。

该脚本适用于任何任意矩阵，只需将 *dptRows* 和 *dptCols* 变量更改为 LLRD 的维度即可。

live viewer 使用异步 HTTP (AJAX-ish)请求来显示用户提交的涂鸦动画的流提要。它将尝试设置一个 cookie，以便每次加载页面时都可以从新的序列开始。如果您不允许 cookie，它将在您下次访问时从 0 重新开始。

*序列位图格式*
序列生成器将每一列输出为 ASCII 格式的位图。每一列的位图由一个空格分隔，每一个完整的帧以一个[换行](http://en.wikipedia.org/wiki/Newline#Representations) (nr)结束。这种格式是由 Mathieu Roncheau 的 PC sequencer 程序定义的，我们保留它是为了保持向后兼容性。

![](img/5fb38fc4e01b2f81fb35bf5c238ada17.png "image_map-squat")

位图数据在帧的左上角归零。每列的顶部单元是位 0，底部单元是位 4。遵循标准数学符号并使用左下角的单元格作为原点似乎更符合逻辑，但我们并没有设计规范。

通过将点亮的 led 视为二进制数中的 1，并转换为十进制数，可以找到每列的值。例如，上面的第一列是 10000 个二进制数，即 1 个十进制数。最后一列是二进制的 11111，即十进制的 31。您可以使用[在线二进制-十进制计算器](http://mistupid.com/computers/binaryconv.htm)来验证我们的转换。

![](img/8671d59fd1fa1b9ee984469f9e1688e1.png "ascii2dec")

注意，列位图由实际十进制值的 ASCII 等价物表示。数字按照 [ASCII 标准](http://www.asciitable.com/)编码，即实际值加 0x30h。此外，多位数被存储为单个字符；示例中的 24 存储为 0x32h、0x34h。

服务器端
后端是一个简单的软件，它接受动画序列，进行一些验证，并将它们保存到数据库中。可以从 datafeed API 访问存储的序列。

 **后端*
我们写了两个版本的后端；两者都在[项目档案](http://blog.mahalo.com/hackaday/howto/graffitiV1.zip)里。第一个是一个简单的 PHP/MYSQL 后端，用于低容量在线 LLRDs，另一个是一个 [Google App Engine](http://code.google.com/appengine/) /Python 版本，应该能够处理一天一堆黑客读者。

为自己喜欢的平台写一个后端真的很简单。将涂鸦设计师的提交表单动作改为指向你的后端；两个版本目前都发布到*backend.php*。现在，捕捉服务器上的“author”和“seq”变量，并将它们保存到数据库中。

我们的后端执行一些验证来防止对系统的攻击。我们分阶段实施检查，这样就不会浪费太多资源。首先，检查提交的总体大小，以确保其在合理范围内。接下来，序列被分割成单独的帧，并检查每个帧的形式。如果通过验证，它将被保存到数据库中。

*Feed API*
序列可以通过一个简单的 [datafeed API](http://graffiti-me.appspot.com/feed.php?max=1&last=0) 访问。API 有两个变量:

![](img/05bffa152d8811d482d7d69443008f6a.png "feed-screenshot")

[http://graffiti-me.appspot.com/feed.php?**最大**= 1&最后 =0](http://graffiti-me.appspot.com/feed.php?max=1&last=0)

*   **max**–发送序列的最大数量。
*   **last**–读取最后一个序列，仅发送较新的数据。

datafeed 以字符“#”开始每个动画序列，后跟 ID 号和换行符。“#”是无效的位图值，用于提醒客户端新序列的开始。客户端可以使用 ID 号和 API 的最后一个变量来获取新的序列。

**硬件**
*迷你 web 服务器*
![](img/f184cb53bb0905b3ae3645899ba41407.png "server-graffiti-connected-4")
我们使用我们的 PIC24F 迷你 web 服务器作为这个项目的支持 TCP 的客户端。阅读我们之前的文章，了解如何[构建 web 服务器](http://hackaday.com/2008/09/25/web-server-on-a-business-card-part-2/)。

愚蠢的朋克桌子
【Mr galleta】有一个很棒的[建造教程](http://www.instructables.com/id/How-to-build-a-Daft-Punk-Table-Replica/)用于蠢朋克桌子复制品的实际桌子部分。不过，LLRD 可以有多种形式，比如我们的壁挂式。

大多数蠢朋克表复制设计是由一个 [74HCT595](http://www.nxp.com/acrobat_download/datasheets/74HC_HCT595_4.pdf) (pdf)输出扩展器和 [ULN2803A](http://focus.ti.com/lit/ds/symlink/uln2803a.pdf) (pdf)晶体管阵列控制的。来自[的驱动板将两者结合成一个易于蚀刻的通孔 PCB。每个驱动板有两个 74HTC595s，或 16 个输出；我们的 25 单元 LLRD 需要两块驱动板。](http://www.instructables.com/id/Daft-Punk-Table-Replica-Graphics-Card/)

![](img/9314efb045470bec5ca93a467b3012e1.png "spi-5953")

74HCT595 是一款串行输出扩展器，由类似 SPI 的接口控制。通过降低*锁存器*线来启动更新。每个 LED 的状态(开或关)被放在*数据*线上，随后是*时钟*的脉冲。一旦 latch 信号返回高电平，输出引脚上就会放置位。数据从一个 595 的数据输出引脚级联到下一个 595 的数据输入引脚。阅读此 [74xx595 教程](http://www.arduino.cc/en/Tutorial/ShiftOut)，详细了解该器件的接口。

需要注意的是，我们使用的是 74 **HCT** 595，而不是 74 **HC** 595。“HCT”部分可以在很宽的电压范围内工作，包括迷你网络服务器的工作电压:3.3 伏

![](img/2b8e92a2dc6d88c5d3aa2813cfdedd60.png "595-driver")

74HCT595 提供电流，这意味着我们可以在 3.3 伏下直接从每个输出运行单个 LED。由于大多数 LLRDs 每个单元有 2-8 个 LED，工作电压在 5 至 24 伏之间，我们采用 ULN2803A 晶体管阵列来切换较大的负载。ULN2803A 吸收电流，而不是流出电流；它切换 led 的接地连接，而不是电源。

![](img/27d79d9c67a31a2b3edefe95053fcc63.png "led-holders-450")

我们的 LLRD 每个电池有两个 led，在 20 毫安时运行，5 伏电源和 56 欧姆电阻。我们将发光二极管焊接在一块纸板周围，而不是蚀刻 25 块微型电路板。

*连接*

![](img/b4b85cfd85017990de14228c0a333f36.png "pin-connections")

微型网络服务器和驱动板之间的 5 线连接控制 LLRD。

| **服务器** | **LLRD** | **描述** |
| V+ | Vsys 吗 | 595s 的 3.3 伏电源。 |
| GND | GND | 共享接地连接。 |
| RA0 | 数据输入 | 数据信号。 |
| RA1 | 时钟 | 时钟信号。 |
| RB15 | 门闩 | 锁存信号。 |
| — | Vled | LED 电源。 |

**固件**
我们的固件是使用 MPLAB 和 Microchip C30 演示编译器用 C 编写的。在我们的[入门教程](http://hackaday.com/2008/09/18/web-server-on-a-business-card-part-1/)中了解更多关于编程和使用 PIC24F 的信息。两个固件版本包含在[项目档案](http://blog.mahalo.com/hackaday/howto/graffitiV1.zip)中。第一个只显示 all *。seq 序列文件来自 SD 卡，第二个版本添加了用于互联网连接的微芯片 TCP/IP 堆栈。在我们的[迷你网络服务器教程](http://hackaday.com/2008/09/25/web-server-on-a-business-card-part-2/)中了解更多关于微芯片 SD 卡和 TCP/IP 库的信息。

所有的图形功能，包括 TCP 客户端，都可以在 *graffitigfx.c* 中找到。TCP 客户端基于 TCP/IP 堆栈中包含的通用 TCP 客户端示例。我们遵循 Microchip 的协作式多任务处理方法，将代码分成小段，与 TCP/IP 堆栈的其他部分共享 CPU 时间。

客户端定期连接到数据馈送并请求新的序列。解析新序列的 ID 号，并将其附加到 SD 卡上的临时文件中。检测到的最后一个 ID 被写入临时数据文件的最末尾，并在后续数据馈送请求中被附加到 URL 的 *last* 变量。我们将 ID 记录在文件的末尾，以避免重复写入 SD 卡上的同一扇区。希望 1GB SD 卡内的损耗均衡足以避免最初几十年的使用问题。如果没有可用的网络连接，设备将播放任意*。SD 卡根目录下的 seq 文件。

解析器功能解码帧并将它们发送到 LLRD。解析器对错误相当健壮。通过后端验证例程的坏数据将在设备级被拒绝，而不会产生不良影响。如果一些腐败的画面出现了，它很难在墙上的其他抽象图案中被注意到。

```

#define GFX_USE_TCP_CLIENT //include the TCP client
#define GFX_TCP_ONLY //only do TCP and read temp file, don't read other files on the SD card.
#define GFX_CLEAR_TEMP_ON_RESET //optionally delete the temp file on reset. good for Google App Engine...

```

在 *graffitigfx.c* 开头的三个定义控制编译时包含哪些特性。GFX _ 使用 _ TCP _ 客户端编译启用 TCP 客户端的固件，注释该固件的仅 SD 卡版本的定义。GFX_TCP_ONLY 忽略任何。seq 文件，只能播放从网上下载的序列。GFX _ 清除 _ 临时 _ 开 _ 复位选项将在每次复位时删除临时序列文件；这对于拥有无序记录 id 的数据库很有帮助，比如 [Google 的 datastore](http://code.google.com/appengine/docs/datastore/) 。将来，这些定义可以更改为由 SD 卡上的配置文件设置的变量。

**更进一步**
我们简单的固件是在线涂鸦墙的稳定起点。当我们在这个项目上工作的时候，我们想出了很多没有在原型中实现的额外功能。

*   启动时显示 IP 地址。
*   SD 卡上的配置文件，用于设置数据馈送 url、刷新频率和其他变量。
*   用于远程配置的 telnet 或 web 界面。
*   TCP 服务器，用于直接访问显示器；从远程电脑推送动画帧。
*   报告错误和状态信息的邮件客户端。
*   启动和序列下载期间的进度信息。SD 卡不存在/已满错误。
*   滚动 Twitter 订阅。
*   你的想法？

不要光看这个项目，[为涂鸦墙](http://graffiti-me.appspot.com)贡献一些画面。

下一次我们将介绍我们最后的 PIC24F 项目，这是一个以太网背包，用于 SparkFun Electronics 生产的价值 20 美元的小型彩色诺基亚 LCD 仿制品。*
# 如何:用 Linux 启动快速编程

> 原文：<https://hackaday.com/2010/08/11/how-to-launchpad-programming-with-linux/>

当 TI 在六月底发布他们的 [Launchpad 开发板](http://hackaday.com/2010/06/22/ti-makes-a-big-bid-for-the-hobby-market/)时，它引起了很多轰动。这里有一个软件包，提供了一个编程器、调试器、两个微控制器和一些附件，价格不到 5 美元(包括运费)。他们甚至提供了两个软件套件供用户选择，但只针对那些不介意使用专有软件的 Windows 用户。如果您想另辟蹊径，您应该考虑尝试开源替代方案 MSPGCC。休息之后，我们将看看如何在 Linux 环境中建立和运行工具链。

我们将使用 Ubuntu 10.04 Lucid Lynx。当 Launchpad 连接到 USB 时，它被识别并安装到/dev/ttyACM0。现在还不清楚如何使用这种设备，但幸运的是这是可以做到的。为了与硬件进行编程和调试，我们需要使用 MSPDebugger。为了编译我们的代码，我们将使用 [MSPGCC 开源编译器包](http://mspgcc.sourceforge.net/)。

**编译安装 MSPGCC**

我们需要做的第一件事是满足我们的构建依赖。

```
sudo apt-get install subversion gcc-4.4 texinfo patch \
libncurses5-dev zlibc zlib1g-dev libx11-dev libusb-dev \
libreadline6-dev
```

现在我们将从 subversion 资源库中签出源代码:

```
svn checkout https://mspgcc4.svn.sourceforge.net/svnroot/mspgcc4
```

接下来我们进入目录并开始编译:

```
cd mspgcc4
sudo sh buildgcc.sh
```

这需要一些时间，所以[去读一些帖子](http://hackaday.com/)，20-45 分钟后回来。

要将我们刚刚安装的工具添加到路径中，我们需要编辑/etc/profile 文件:

```
sudo nano /etc/profile
```

将这一行添加到文件的末尾(完成后按 CTRL-X 退出):

```
export PATH=${PATH}:/opt/msp430-gcc-4.4.3/bin
```

现在重新加载您刚刚编辑的配置文件以使其生效:

```
source /etc/profile
```

很好，现在您有了将 C 代码编译成。微处理器能够理解的 elf 文件。接下来，我们需要一种方法把文件放到芯片上。

**编译 MSPDebug**

我们将使用 [MSPDebug 指令](http://mspdebug.sourceforge.net/download.html)进行下载和编译。首先你需要[去下载页面获取最新版本](http://sourceforge.net/projects/mspdebug/files/)。我们下载了版本 0.9，并将在以下命令的文件名中使用该版本。现在转到您保存下载文件的目录，使用下面的一组命令来解包归档文件、编译和安装软件包:

```
tar xvfz mspdebug-0.9.tar.gz
cd mspdebug-0.9
make
sudo make install
```

这应该只需要几秒钟，这是我们需要的最后一个工具。接下来，我们可以使用我们的新软件来连接设备。

**代码**

最好第一次就尝试一些经过验证的代码。[下载我们的简单代码包](https://github.com/Hack-a-Day/had_launchpad-blink)来测试编译器，并使用调试器进行编程。这比在[漫谈和断章取义的代码](http://losinggeneration.homelinux.org/2010/07/02/msp430-launchpad-on-linux/)上找到的温度演示要简单得多，因为我们正在使用他们的 Makefile，一旦你对这个过程感到舒适，在那个包里有很多很棒的代码示例。

解压缩代码，打开终端窗口，并导航到文件所在的目录。通过键入以下命令编译该文件:

```
make
```

如果进展顺利，那太好了。如果您得到类似“msp430-gcc: command not found”这样的错误，那么您的 MSPGCC 工具路径就有问题。

**连接芯片**

MSPDebug 是我们用来连接芯片的。以下命令很可能不适合您:

```
mspdebug rf2500
```

发出错误信息:

```
Trying to open interface 1 on 033
rf2500: warning: can't detach kernel driver: Operation not permitted
rf2500: can't claim interface: Operation not permitted
rf2500: failed to open RF2500 device
```

这很可能是由权限问题引起的。如果你在开头加上“sudo ”,这将会起作用，但这并不理想。让我们添加一个 UDEV 规则来处理每次插入的 Launchpad。我们需要创建一个包含这行代码的规则文件:

```
ATTRS{idVendor}==&amp;quot;0451&amp;quot;, ATTRS{idProduct}==&amp;quot;f432&amp;quot;, MODE=&amp;quot;0660&amp;quot;, GROUP=&amp;quot;plugdev&amp;quot;
```

使用 nano 打开并编辑该文件。完成后按 CTRL-X 退出，然后重新加载 UDEV:

```
sudo nano /etc/udev/rules.d/46-TI_launchpad.rules

sudo restart udev
```

***如果你在这方面需要更多帮助，请看一下[我们编写 udev 规则的指南](http://hackaday.com/2009/09/18/how-to-write-udev-rules/) ***

拔下 Launchpad 并将其插回。确保您与编译器之前创建的“main.elf”文件位于同一目录中。现在再给 MSPDebug 一次机会:

```
mspdebug rf2500
```

现在，您将看到(mspdebug)提示符。只需要给芯片编程并运行程序:

```
prog main.elf
run
```

两个指示灯将以大约 1 赫兹的频率开始闪烁。恭喜你，你已经使用开源工具编译并加载了一个程序。

**看看代码是如何工作的:**

让我们快速了解一下这个简单的程序是如何工作的，以便让您能够轻松地学习使用 MSPGCC 进行编码。代码中使用的关键字是在 MSPGCC 的包含文件中定义的。你需要花一些时间在/opt/MSP 430-gcc-4 . 4 . 3/MSP 430/include/MSP 430 目录中，直到你习惯了这些关键字。一旦你掌握了窍门，你可能会根据你在微处理器数据表中读到的内容猜出新的关键字。

我们的代码闪烁两个 led。眨眼意味着我们需要使用某种方法来跟踪时间。首先让我们研究一下系统时钟:

下载一份[MSP 430 x2 xx 系列数据手册](http://focus.ti.com/lit/ug/slau144e/slau144e.pdf)(我们使用的是 E 版)并遵照执行。这份文档比特定芯片的数据手册更有用，因为它列出了所有外设的工作信息。

回顾第 5.1 节中的各种系统时钟特性，注意 LFXT1CLK、VLOCLK 和 ACLK。接下来阅读第 289 页的第 5.2 节，它告诉我们上电后系统时钟将以 1.1 MHz 运行。如果我们使用系统时钟来计时，我们将很难使用 16 位定时器来计数足够高的时间，从而产生有意义的延迟。我们可以用辅助时钟来代替。数据手册的同一页告诉我们，ACLK 来自 LFXT1CLK(外部晶振或时钟源)，但让我们改变一下。VLOCLK 可以用作辅助时钟的时钟源，其工作频率为 12 kHz，因此 1 秒的时序完全在 16 位计数器的范围内。让我们来设置时钟源。第 5.2.2 节清楚地告诉我们“当 XTS = 0 时，通过设置 LFXT1Sx = 10 来选择 VLOCLK 源。”。现在，我们只需检查寄存器描述，直到发现寄存器 BCSCTL3 上设置了 LFXT1S，然后编写代码来实现此设置:

```
BCSCTL3 |= LFXT1S_2;
```

接下来，我们要基于辅助时钟设置一个中断。在第 12 节中，您可以阅读有关 TimerA 的内容。我们将把它配置为在 UP 模式下运行。第 410 页介绍了定时器控制寄存器 TACTL 的配置。我们需要将 TASSELx 设置为使用配置为 UP 模式的 ACLK 和 MCx。请注意，寄存器各部分的设置以二进制形式列在描述的旁边。我们可以使用这些来选择适当的位。使用以下代码将 MC 位设置为 1(二进制 01)，将 TASSEL 位设置为 1(二进制 01):

```
TACTL |= TASSEL_1 | MC_1;
```

现在，我们必须使能 TimerA 比较/捕获寄存器 0 的捕获/比较中断:

```
TACCTL0 = CCIE;
```

现在，我们可以通过向它写入一个值来启动计时器。因为我们使用 12 kHz 的内部极低振荡器，所以我们可以计数到 11999，以跟踪大约 1 秒的时间(计数为 0，这就是为什么我们将比较匹配设置为比时钟速度慢一个周期):

```
TACCR0 = 12000;
```

最后，我们启用全局中断:

```
eint();
```

现在我们只需要中断服务程序中的一些代码来切换 led:

```
interrupt(TIMERA0_VECTOR) TIMERA0_ISR(void) {
  LED_OUT ^= (LED0 + LED1);	//Toggle both LEDs
}
```

我们将所有这些放在一起制作了示例文件。花些时间去理解数据手册告诉你什么。虽然它们可能会令人困惑，但你需要知道的一切都在那里。

**资源:**

*   [我们的示例代码](https://github.com/Hack-a-Day/had_launchpad-blink)
*   [使用 TI MSP430 LaunchPad 和 Ubuntu 10.04](http://eclecti.cc/hardware/using-the-ti-msp430-launchpad-with-ubuntu-10-04)
*   [在 Kubuntu 10.04 上安装 MPSGCC4 和 MSPDEBUG](http://mylightswitch.com/2010/06/21/installing-mpsgcc4-and-mspdebug-on-kubuntu-1004/)
*   [Linux 上的 MSP 430 launch pad](http://losinggeneration.homelinux.org/2010/07/02/msp430-launchpad-on-linux/)
*   [MSPGCC](http://mspgcc.sourceforge.net/)
*   [MSPDebug](http://mspdebug.sourceforge.net/download.html)
*   [MSP430G2313 数据表](http://focus.ti.com/general/docs/lit/getliterature.tsp?genericPartNumber=msp430g2231&fileType=pdf) (PDF)
*   [MSP430x2xx 系列数据手册](http://focus.ti.com/lit/ug/slau144e/slau144e.pdf) (PDF)
*   [TI MSP430 Launchpad Wiki](http://processors.wiki.ti.com/index.php/MSP430_LaunchPad_(MSP-EXP430G2))
*   [如何编写 udev 规则](http://hackaday.com/2009/09/18/how-to-write-udev-rules/)
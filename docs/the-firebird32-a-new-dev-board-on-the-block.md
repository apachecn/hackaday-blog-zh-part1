# Firebird32，即将上市的新开发板

> 原文：<https://hackaday.com/2011/07/23/the-firebird32-a-new-dev-board-on-the-block/>

[![](img/8e2a4877fa7aa0df925eae6d77a0a008.png "firebird32")](http://hackaday.com/2011/07/23/the-firebird32-a-new-dev-board-on-the-block/firebird_trainer/)

这里还有一个开发板可以添加到你的列表中(如果你喜欢保存列表)，介绍 [Firebird32](http://www.firebird32.com/index.html "main link") 。新开发板的生产似乎永无止境，Firebird32 沿用了当前的风格，采用熟悉的 Arduino 外形，适合所有 Arduino 屏蔽。

[Wytec]的 Firebird32 围绕 32 位 Freescale Flexis MCU[[mcf 51 JM 128](http://www.freescale.com/webapp/sps/site/prod_summary.jsp?code=MCF51JM)]构建，运行工业和医疗设备中常见的 Coldfire V1 内核。在发布之前，我们被友好地捐赠了一个板，我们注意到的第一件事是板载 8×2 段 LCD，它是完美的调试工具。该板以及安装的标准 Arduino 屏蔽具有额外的键盘输入接头、加速度计和额外的通信接头(IC2/SPI/SCI)。它还配备了 8 x 12 位模拟输入，外部 32k EEPROM，RGB LED，蜂鸣器和一个额外的按钮。Flexis 芯片和强大的 32 位处理器可以使用 PLL 以高达 48Mhz 的时钟速率运行，并具有集成的 USB 端口，所有这些都不到 30 美元。

所以硬件看起来不错，你可以直接插入 Arduino 屏蔽，但是(你知道它是正确的)它还不兼容 Arduino 草图或代码。目前对于初学者来说，Firebird32 配备了 [StickOS BASIC](http://www.cpustick.com/) bootloader，它似乎是一种非常高级的编程语言，可能有助于获得 LED 闪烁，但我们并不完全相信它充分利用了芯片的潜力。要用 C/C++或汇编语言编程，需要一个 USBDM 程序员，代码使用 CodeWarrior IDE 编译，它提供了一步一步的调试，这很好，设置起来并不完全明显，但一些教程和源代码可以让你开始[可用](http://hownottoengineer.com/index.php?option=com_content&view=article&id=84%3Afirebird32&catid=43&Itemid=61)。

底线是 Firebird32 是一个外观漂亮的板，有一些很棒的硬件，成本很低，适合需要一些额外功率的项目，但它不是初学者的工具。Coldfire 芯片组在工业设备中非常常见，因此该主板为想要学习嵌入式硬件编码或迁移到更高级的 Coldfire V2/3 控制器的工程师提供了一个完美的跳板。
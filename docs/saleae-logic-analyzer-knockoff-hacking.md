# Saleae 逻辑分析仪山寨黑客

> 原文：<https://hackaday.com/2011/12/15/saleae-logic-analyzer-knockoff-hacking/>

不管这个模块是怎么说的，它肯定不是官方的 Saleae 逻辑分析仪硬件。[杰克·安德鲁斯]在易贝买了这个中国仿制品，大约 18 美元。当插入电脑时，Saleae 软件会将其作为官方硬件。但是[Jack]已经看到了其他仿制品，它们有一个跳线可以在 Saleae 克隆和 USBee 克隆之间进行选择，所以[他找到了一种用这个加密狗切换软件的方法](http://www.jwandrews.co.uk/2011/12/saleae-logic-analyser-clone-teardown-and-reprogramming/)。

他将电路板从机箱中取出，发现在焊接不良的电路板上有一个 Cypress CY7C68013A 微控制器(想象一下)。这是一款兼容 8051 的处理器，具有 USB 功能。电路板底部还有一个 EEPROM，用于存储 VID/PID 对，将其识别为 Saleae 逻辑硬件。使用 USBee 软件的诀窍是改变这一对。[Jack]在没有外部程序员的情况下成功做到了这一点。他卸载了 Saleae 驱动，安装了 Cypress 驱动。然后，他为 CY7C68013A 编写了一点代码，以重写 EEPROM，并通过 USB 连接进行闪存。现在，加密狗枚举为 USBee 逻辑分析仪硬件。
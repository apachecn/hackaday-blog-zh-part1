# PS2 到 USB 键盘转换器也记录您的击键

> 原文：<https://hackaday.com/2011/08/16/ps2-to-usb-keyboard-converter-also-logs-your-keystrokes/>

![](img/ef6bc0c2fd6ef71d353316af2b6624f1.png "teensy-key-logger")

[肖恩·麦库姆斯]对他的第一个青少年项目不怀好意。你在上面看到的电路板从 PS2 键盘获取[输入，并将其转换为 USB 连接](http://theifdark.blogspot.com/2011/08/teensy-hardware-key-logger.html)。哦，我们有没有提到它也可以记录你输入的所有内容？

从一开始，该项目旨在成为一个键盘记录器。这是一个中间人设备，可以隐藏在键盘的外壳内，使它看起来像一个普通的 USB 键盘。数据存储在 SD 卡中，因此攻击者需要在他的目标数据被键入后才能访问硬件。

它基本上和[肖恩]预期的一样。但是，他在操作 CTRL、ALT、Windows 和 Caps Lock 键时有困难。如果这真的被恶意使用，这将是一个致命的泄露。许多安全的 Windows 机器需要 CRTL-ALT-DELETE 键来访问登录屏幕。
# 神奇地修复 AVR 芯片

> 原文：<https://hackaday.com/2010/05/17/magically-repair-avr-chips/>

![](img/18d4c7d1b05c407f21134bc5586bcc7d.png "ATmega_fusebit_doctor")

如果你曾经花时间使用 AVR 微控制器，你可能至少有一次错误地设置了熔丝位。ATmega fusebit doctor 会自动修复保险丝，让你在下一次事故发生前恢复工作。为该设备供电的 ATmega8 内部存储了 ATmega 系列的芯片签名，因此它会自动检测到您正在试图“解锁”哪个芯片。从那里，它查找正确的熔丝位，并复活生病的微控制器。这有助于恢复已禁用串行编程、将 reset 引脚用作 I/O 或仅启用外部时钟而没有必要硬件来提供该功能的芯片。

这种魔力是通过使用高电压并行编程来实现的。我们已经看到 HVPP 被用在 Arduino rescue shield 中，这是 AVR Dragon(我们最喜欢的 AVR 程序员)和其他人的一个有价值的 T2 特性。尽管如此，你很难击败插入一个死芯片到这个板和按下一个按钮的容易。哦，你和阿提尼家的人上床了吗？还有一个[为那些太过](http://diy.elektroda.eu/attiny-fusebit-hvsp-doctor/#eng)的人设立的救助委员会。

[谢谢 Stewe]
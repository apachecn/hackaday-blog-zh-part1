# 微型触摸上的 Zork

> 原文：<https://hackaday.com/2011/04/20/zork-on-the-microtouch/>

![](img/ef185b2e1a1b25effe85e68d70a3385e.png "zork-microtouch")

[Rossum]刚刚完成将 Zork 移植到 micro touch 上。这个硬件是[他最初设计的](http://hackaday.com/2009/11/03/8-bit-device-quenches-iphone-envy/)，现在[可以通过 Adafruit](http://hackaday.com/2011/01/31/update-microtouch-the-8-bit-ipod-touch/)购买。这是一个微型 320×240 TFT 触摸屏，由 AVR ATmega32u4 微控制器驱动。该设备由锂电池供电，还拥有 USB 连接和 MicroSD 插槽。

这里的黑客是让 Zork 在设备可用的有限资源下运行。[Rossum]需要模拟 Z80 处理器，但不想像[Sprite_TM]使用 AVR 模拟 Z80 时那样使用额外的硬件。相反，这是基于对[弗鲁兹](http://frotz.sourceforge.net/)的精简实现。最终的代码太大，无法放在引导装载程序旁边的芯片上。这意味着你需要使用 ISP 程序员来将这个例子刷新到芯片上。我们非常确定 AVRdude 可以对 ATmega32u4 进行编程，因此几乎任何 ISP(包括 Arduino)都可以用来进行编程。
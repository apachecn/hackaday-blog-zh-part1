# ATtiny2313 系列黑客攻击

> 原文：<https://hackaday.com/2009/08/06/serial-hacking-with-an-attiny2313/>

![board](img/79106231726cee40872d966c6f0b56b5.png "board")

[Sprite_tm]通过使用 ATtiny2313 和 FT232 分线板[嗅出波特率](http://spritesmods.com/?art=autobaud&page=3)，自动化了部分串行黑客攻击。固件采用 8 个数据位，无奇偶校验，1 个停止位(8N1)。这在串行端口中几乎是事实，所以它应该工作得很好，尽管有些设备确实使用不同的设置。自动检测例程可以嗅探低至 110 波特的速率，并支持非标准速率。在 GPLv3 下发布的[软件也以十六进制格式](http://spritesmods.com/autobaud/autobaud.tgz)提供。[Sprite_tm]过去已经提供了很棒的项目，例如与 VFD[一起工作的](http://hackaday.com/2009/06/16/controllable-bristlebot/)[、](http://hackaday.com/2008/12/25/working-with-vfds/)可控毛刺和 [AVR 升压转换器](http://hackaday.com/2009/07/07/avr-boost-converter/)。休息后关于系列黑客攻击的附加信息。

许多电子产品都有一个致命弱点，那就是串行端口。这些嵌入式端口通常在开发过程中用于调试功能、加载和升级固件等。至少，电路轨迹通常是出于自动测试的目的而出现的。查找芯片引脚和追踪电路是系列黑客攻击的一小步。轨迹已知后，就可以确定电压电平(CMOS、TTL、RS232 等)。然后在端口上运行一些测试。这些测试通常给出关于端口潜力的指示(它有驱动程序吗，它有协议吗，波特是什么，等等)。如果在数据手册中找不到关于波特率和其它标准的信息，[Sprite_tm]的方法肯定会节省大量繁琐的时间。一些控制器，如 68HCxx 可能有一个引导 ROM，它消除了设置串行端口的大部分猜测工作。我们几乎每天都使用[零调制解调器仿真器](http://com0com.sourceforge.net/)项目(com0com)来帮助解决各种串行问题。对于任何长时间使用串行设备的人来说，这是非常值得推荐的。
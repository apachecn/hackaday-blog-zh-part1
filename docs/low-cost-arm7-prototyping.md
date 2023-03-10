# 低成本 ARM7 原型制作

> 原文：<https://hackaday.com/2009/09/10/low-cost-arm7-prototyping/>

![blueboard_arm7_prototyping.jpg](img/ca81fdeccbdc779455814fd0a07dd466.png "blueboard_arm7_prototyping.jpg")

当你[试图接管世界](http://www.scienceprog.com/low-cost-and-open-lpc2148-development-board-launched/)时，你有没有发现你当前微控制器的能力在拖你的后腿？升级到 [ARM7 架构](http://en.wikipedia.org/wiki/ARM7)将把你的项目放在与 iPod 和任天堂 DS 相同的舞台上。

[BlueBoard-lpc214x 是一款原型板](http://code.google.com/p/blueboard-lpc214x/),可提供许多功能。它包含两个 RS232 连接、USB、VGA、SD 卡插槽、压电蜂鸣器、JTAG、音频输出、PS2 键盘连接器和一个 2 线字符 LCD。处理器是恩智浦半导体 LPC2148，具有 512KB 编程空间和 32+8KB ram。该板还包括一个 256KB i2c eeprom。这是非常强大的原型制作能力，但是[的低购买价格](http://shop.ngxtechnologies.com/product_info.php?cPath=21&products_id=28)让我们大吃一惊:40.90 美元！可悲的是，运输将花费我们 20.43 美元，但这仍然是 60 美元左右的许多功能。

示例代码和原理图[可从](http://code.google.com/p/blueboard-lpc214x/downloads/list)下载。微控制器的所有引脚都有跳线，如果您想插入自己的硬件，处理器周围还有成排的引脚接头。我们已经看到其他的[臂板利用了预先存在的护盾](http://hackaday.com/2009/08/22/maple-beats-up-arduino-takes-its-shields/)。我们希望看到有人移除处理器，并为 LPC214x 系列之外的不同处理器实现类似 Arduino 的屏蔽。休息后的宣传片。 [https://www.youtube.com/embed/lV5wRTeRFcs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lV5wRTeRFcs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[via [科学计划](http://www.scienceprog.com/low-cost-and-open-lpc2148-development-board-launched/)

[谢谢 CH]
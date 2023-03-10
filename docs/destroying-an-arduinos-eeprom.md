# 破坏 Arduino 的 EEPROM

> 原文：<https://hackaday.com/2011/05/16/destroying-an-arduinos-eeprom/>

我们以前见过测试 EEPROM 寿命的项目，但这些项目只测试了分立的 EEPROM 芯片。tronixstuff 的[John]有一个不同的想法,并着手测试 ATmega328 的内部 EEPROM。

[John]的构建只是一个 Arduino 和 LCD 屏蔽，一次将数字 170 写入内存，下一次将数字 85 写入内存。因为这些数字在二进制中是 10101010 和 01010101，所以每个位在每次运行时翻转一次。我们认为这可能比每次运行都编写 0xFF 要好——欢迎 hackaday 读者对这一实现发表评论。Arduino 插在墙上的电源插座上，然后“在沙发后面坐了几个月”经过 47 天 1，230，163 个周期后，EEPROM 出现第一次写错误。这比 atmel 数据表上的规格好一个数量级，但与类似实验的结果相似。

我们去年报道了一个类似的项目，即[闪存破坏者](http://hackaday.com/2010/05/28/russian-roulette-for-eeprom/)，但是它测试的是外部 EEPROM，而不是微控制器的内部存储器。

休息之后，请查看 EEPROM 黑仔的大幅删节视频。

[https://www.youtube.com/embed/t8X0zip7TvU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/t8X0zip7TvU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
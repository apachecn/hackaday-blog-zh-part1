# 零件:ChronoDot RTC 模块(DS3231)

> 原文：<https://hackaday.com/2009/10/27/parts-chronodot-rtc-module-ds3231/>

![ChronoDot](img/7c00e85f19a77d3055d2585bf13cc135.png "ChronoDot")

[Macetech 的 ChronoDot](http://docs.macetech.com/doku.php/chronodot) 是一款实时时钟模块，适用于需要高度精确计时和测量的项目。ChronoDot 使用 [DS3231](http://www.maxim-ic.com/quick_view2.cfm/qv_pk/4627) 芯片，该芯片具有[TCXO](http://www.wenzel.com/documents/tcxo.html)以补偿影响正常振荡器的温度变化，就像大多数微控制器中的振荡器一样。DS3231 使用简单的 I2C 命令和寄存器来存储和检索时间，但也具有一个可变输出，一直到 1.000 hz，适合低功耗、中断式计时应用。使用随附的手表电池，ChronoDot 可以在闲置模式下保持时间长达 8 年。

通常情况下， [ChronoDot](http://macetech.com/store/index.php?main_page=product_info&cPath=5&products_id=8) 大部分都是组装好的，只需要在手表电池上焊接即可。然而，由于一个制造错误，Macetech 正在出售一个版本，其头部引脚位于错误的一侧，他们称之为 [ChronoDoh](http://macetech.com/store/index.php?main_page=product_info&cPath=5&products_id=15) 。这个模块目前几乎是正常价格 14.99 美元的一半，这使得它成为一个项目的一个非常低的成本。Macetech 向我们发送了几个这样的模块来展示它们的功能。

![Dohdot](img/0c25a50537a5acdb295035718eb0695e.png "Dohdot")

由于这个错误，使用这些零件作为试验板工具变得有点困难，因为丝印引脚名称只在“顶部”一侧。但是，如果项目是围绕这一部分设计的，或者如果使用了替代工具，如线带或探针，这个问题就会消失。也可以将接头引脚脱焊并重新安装，但无论何时脱焊，都有可能抬起焊盘，或对器件造成损坏。

![cd1](img/1bf61c056a114345b709e0dd9aa88bbc.png "Preparing to solder the battery on.")

我们按照演示设置了一个 ChronoDoh 模块，并使用一个“正面朝上”的 ChronoDoh 作为参考来固定 I2C 连接。这个点必须有一个外部 VCC 信号来响应 I2C 的命令，只有在手表电池供电的情况下才会安静地保持时间。对于 ChronoDo(h/t)，Macetech 的网站上提供了 Arduino 代码和原理图样本，使初始设置和测试变得轻而易举。我们使用 [Teensy++运行 Teensyduino 加载器](http://www.pjrc.com/teensy/teensyduino.html)来简化这个过程。示例代码简单地显示了点在 I2C 上空报告的时间，这似乎是从点第一次接收 5V 电源开始的时间(当它最有可能被初始化时)。芯片报告时间为 00:01:55，这意味着该更新寄存器了。不幸的是，示例代码在这里遗漏了，尽管所提供的文档确实提供了所有相关寄存器的列表(数据手册第 11 页)。

![CIMG0776ed](img/f880e42c2c70de3e8342e71d14ed0644.png "Soldered battery next to unpopulated dot.")

在[设置 I2C 寄存器](http://www.robot-electronics.co.uk/htm/using_the_i2c_bus.htm)之后，ChronoDoh 正确地保持时间，所以我们决定测试其准确性。我们安装了另一个模块，把它放在冰箱里一个星期，然后对两个模块进行对比测试。令人惊奇的是，他们报告的时间完全相同。虽然不科学，但这得到了 DS3231 制造商正在进行的[精度测试](http://www.maxim-ic.com/products/timers/DS3231_demo/)的支持，该测试声称“0℃至+40℃时的精度为 2ppm(每年约 1 分钟)”。

![CIMG0783ed](img/6d4449b67f25d1e4b05dc8dcf27eacf8.png "Both dots on a breadboard with the Teensy++")

这些分线板是在一个易于使用的分线板上测试这种芯片的好方法，这是 Macetech 做得最好的。

**Hack a Day review disclosure**:mace tech 给了我们几个免费的 ChronoDohs 来回顾这篇文章。
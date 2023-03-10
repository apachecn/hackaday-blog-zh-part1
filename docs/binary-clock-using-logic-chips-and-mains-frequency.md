# 使用逻辑芯片和电源频率的二进制时钟

> 原文：<https://hackaday.com/2011/01/16/binary-clock-using-logic-chips-and-mains-frequency/>

![](img/05d6611397a6b71ebbe7eef4e41832ef.png "binary-clock-uses-mains-clock-signal")

[Osgeld]为自己建造了一个二进制时钟。他没有花时间来解释他的项目，但他确实在建造时发布了精美的手绘电路图和电路图片。我们已经看到[使用电源频率作为时钟源](http://hackaday.com/2010/04/07/logic-clock-without-an-on-board-oscillator/)的时钟项目，这也是【Osgeld】为他的构建选择的路线。他开始用一个 9-12V 的交流壁式麦芽汁作为电源输入。接下来，只需使用桥式整流器转换为 DC，然后使用 7805 线性稳压器建立稳定的 5V 供电轨。一个电阻和几个二极管允许他从输入的交流电中提取 60 赫兹的频率，然后使用 4000 和 7400 逻辑芯片的组合来计数脉冲并记录时间。
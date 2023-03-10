# 硬币电池充电器

> 原文：<https://hackaday.com/2012/03/28/coin-cell-battery-charger/>

![](img/cad9b4dd50dc02f18fcc55dc5ee369d1.png "coin-cell-recharger")

[Jay Kickliter] [自己造了一个纽扣电池充电器](http://www.chasingtrons.com/main/2012/3/26/cr2450-coin-cell-charger.html)。这对绝大多数硬币电池不起作用，因为它们是作为一次性部件制造的。但是有充电选项，型号以 LR 开头，而不是 CR。在这种情况下，他围绕 MCP73832 IC 定制了充电电路，并选择了最适合为 110 mAh LR2450 充电的元件。但我们相信所有的 LR 选项都是 3.6V 的，所以改变他的设计以用于不同的型号应该是轻而易举的。

一段时间以来，我们一直不喜欢使用一次性硬币电池。当然，在实时时钟中，电池可能持续 6-8 年，这不是很浪费。但是在一个用途广泛的苹果电视遥控器中，我们讨厌选择一次性电池。我们所有使用 AA 或 AAA 的不太时髦的遥控器都有镍氢电池，并且已经用了好几年了。所以我们很高兴看到这个充电器项目的出现。

现在坏消息是。我们环顾四周，确实可以找到 LR2032CR2032 的可充电替代品。但是容量等级下降的很平缓。我们看到的型号只有 50 毫安时，而一次性 CR2032 提供大约 240 毫安时。希望随着电池技术的发展，这种情况会有所改变。
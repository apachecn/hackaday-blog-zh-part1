# 另一个关于使用“死”电池的观点

> 原文：<https://hackaday.com/2012/02/29/another-take-on-using-dead-batteries/>

![](img/750b10e10bed3288eb3e4cf78c308692.png "smaller-battery-psu")

这是另一个电路，可以用来从可能已经没电的电池中榨取剩余的电量。就像[的 AASaver](http://hackaday.com/2012/02/27/squeezing-the-juice-out-of-some-aa-batteries/) 一样，我们认为这是一个有用的原型工具，为试验板提供电力，即使它对于长期使用来说不够可靠(毕竟电池快用完了)。

首先，上面的图片显示的是可充电物质，而不是碱性物质。我们不建议这样做，因为该电路没有截止功能，升压转换器的 0.7V 输入肯定低于这些电池的推荐低压限值。但除此之外，我们喜欢焊接在电池组末端的小型电路板。它使用一个 SC120SKTRT，这是一个可变升压调节器，能够根据电阻选择输出 1.8-5V。您可以关闭电阻，它将默认为 3.3V，明确设置输出，或者加入一些电位计并使用万用表来调谐输出。

这种调节器比 AASaver 中使用的 MCP1640 成本更高，但它似乎使用了更少的无源元件，尺寸更小。加上 3.50 美元的 PCB(在家蚀刻很容易)，这是完成下一个零件订单的另一个好选择。

[谢谢 Uwe]
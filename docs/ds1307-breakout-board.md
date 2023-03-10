# DS1307 分线板

> 原文：<https://hackaday.com/2010/07/26/ds1307-breakout-board/>

![](img/b147f553f417cee7dae7e28c69298a48.png "ds1307-breakout")

Adafruit 为 DS1307 RTC 提供了一个方便的[分线板。这个芯片远不如](http://www.ladyada.net/learn/breakoutplus/ds1307rtc.html)[Chronodot](http://hackaday.com/2009/10/27/parts-chronodot-rtc-module-ds3231/)中使用的 DS3231 精确，但它便宜得多。breakout 使其易于进行试验或插入 Arduino，并拥有您需要的一切；时钟晶体、备用电池、滤波电容和上拉电阻。我们最喜欢的部分是 Adafruit 的设计是开源的，所以如果你[从他们的 git 库](http://)中取出文件，你可以自己蚀刻电路板。这将为我们的[原型硬件系列](http://hackaday.com/2010/07/25/extremely-organized-prototyping/)增添一大亮点。

顺便说一下，我们惊讶地发现，I2C 总线上拉电阻选择了 2.2k 电阻。我们的印象是 4.7k 是这里的标准值。我们希望在评论中听到你对此的想法。

[via [危险原型](http://dangerousprototypes.com/2010/07/14/adafruit-ds1307-real-time-clock-breakout-board-kit/)
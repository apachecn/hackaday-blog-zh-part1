# 电子蜡烛保护熟睡的婴儿

> 原文：<https://hackaday.com/2012/02/06/electronic-candle-protects-sleeping-infant/>

![](img/e4337fb18fac1392b8c77a5fd2df9c4e.png "electronic-temperature-candle")

[William] [开发了这种温度蜡烛](http://www.mermardesigns.com/temp_candle.htm)作为一种工具，帮助婴儿在睡眠时保持安全。环境温度似乎对婴儿猝死综合症(SIDS)有影响。这个装置是用来在室温超出建议范围时提醒你的。

该板包含一个 8 引脚 PIC 微控制器(12F683P)、一个温度传感器、一个 RGB LED 和一个按钮。圆形印刷电路板和许愿蜡烛一样大，这很好，除了你要在你的烛台上钻一个孔来容纳桶形插孔。

温度传感器由微控制器读取，并用于确定 LED 的颜色。红色是热的，蓝色是冷的，正好介于两者之间。但是如果你想知道准确的当前温度，你可以按下按钮，它会以 10 度的增量用蓝色闪烁出摄氏读数(闪烁三次是 30 度，等等)。)和红色表示单度。休息后不要错过视频中蜡烛的演示。

[https://www.youtube.com/embed/Z2PWzoKrSgU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Z2PWzoKrSgU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# 看，马，没有电池！

> 原文：<https://hackaday.com/2011/09/14/attiny-hacks-look-ma-no-batteries/>

![ATtiny Hacks Theme Banner](img/5f674cf2d4b94faba5f6b413d805f657.png "ATtiny Hacks Theme Banner")


[Gadre]在不使用任何电池的情况下建造了自己的 ATtiny 项目。这是一个电子骰子(如果你很挑剔的话，也可以说是骰子)，它使用[感应为一个存储电容器充电，作为电源](http://www.instructables.com/id/Faraday-For-Fun-An-Electronic-Batteryless-Dice/)。电压发生器由一根有机玻璃管制成，玻璃管内装有一组稀土磁铁。在管子的入口处[Gadre]加工了一个通道，可以容纳大约 1500 圈 30 AWG 的电磁线。当有人来回摇动管子时，磁铁通过导线，感应出电流。该产品存储在一个 4700 uF 电容中，该电容馈入一个升压转换器，为电路的其余部分供电。

控制电路的 ATtiny13V 以 128 kHz 运行其内部 RC 振荡器，这是尽可能低的设置，以便最大限度地降低功耗。充分摇动后，用户可以按下按钮滚动骰子，然后在七个 led 上显示几秒钟。休息后在视频里自己看吧。

[https://www.youtube.com/embed/lHOUamO67uk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lHOUamO67uk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
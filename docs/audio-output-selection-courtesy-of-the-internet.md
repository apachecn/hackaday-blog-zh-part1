# 互联网提供的音频输出选择

> 原文：<https://hackaday.com/2011/11/15/audio-output-selection-courtesy-of-the-internet/>

![](img/aa291ca086fcd0f8e9e87df38ded10cd.png "lan-audio-switch")

[Peter]厌倦了爬在他的台式电脑后面在耳机和扬声器之间切换。我们感受到了他的痛苦，因为我们电脑扬声器上的耳机端口有自己的恶魔般的嗡嗡声，使插孔对我们无用。他的解决方案是[建立这个输出选择器板，然后通过网络](http://solderintheveins.co.uk/2009/12/simple-audio-switch/)控制它。

继电器负责将单个输入路由到两个输出之一。一个输出连接到继电器的常闭引脚，另一个连接到常开引脚。这里重要的是要确保你有一个独立的音频接地，以免拾取来自其他硬件的噪音。

你在上面看到的只是开关电路。这就是[Peter]做得有点过火的地方，他使用 Arduino 和以太网屏蔽来通过晶体管驱动继电器。对于这种特殊的应用，一定有更简单的方法。但是如果你正在用你的智能手机进行家庭自动化，这可能就是让你的音频设置由浏览器控制的东西。

[通过[建立休息室](http://www.buildlounge.com/2011/11/15/lan-controlled-audio-switch/)
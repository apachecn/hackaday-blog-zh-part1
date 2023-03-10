# R2R 阶梯将多个按钮连接到一个 ADC 引脚

> 原文：<https://hackaday.com/2012/03/02/r2r-ladder-connects-multiple-buttons-to-one-adc-pin/>

如果您在一个项目中用完了 I/O 引脚，并且需要一种添加用户输入的方法，您可以找到许多支持各种通信协议的端口扩展器，如 I2C 和 1-Wire。但是，如果你只是想增加一些按钮，而不是额外的集成电路，你会喜欢这个黑客。[约翰·鲍克夏尔]展示了如何使用一个 ADC 引脚添加四个按钮。

这个概念并不新鲜。这些按钮组成了一个 R2R 电阻梯。当按下其中一个按钮时，分压器的电路就完成了。结果由 IC 的模数转换器测量，以判断哪个按钮被按下。困难的部分是计算电阻值。[John]使用了由两个不同值组成的八个电阻。每个按钮和按钮的每个组合都有一个独特的电压结果，可以被芯片识别。他甚至做了一个真值表，这样你就不用做了。

视频中的示例电路使用了 Arduino。但是这个概念直接适用于任何微控制器。使用 ADC 中断来驱动所有按钮读取事件应该很容易。[https://www.youtube.com/embed/BZ49TgZkUW8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/BZ49TgZkUW8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
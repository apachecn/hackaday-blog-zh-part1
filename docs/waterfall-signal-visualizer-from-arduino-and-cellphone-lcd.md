# 来自 Arduino 和手机 LCD 的瀑布信号可视化器

> 原文：<https://hackaday.com/2011/07/11/waterfall-signal-visualizer-from-arduino-and-cellphone-lcd/>

![](img/ea79acfda23124e2046d5be0f31feba0.png "waterfall-signal-visualizer")

[Leigh]是一个火腿经营者(你可能知道他叫 wa5znu)。他熟悉一种称为瀑布的信号可视化工具，这种工具可以绘制信号强度和频率随时间的变化。他想建立自己的瀑布，最终有了这个基于 Arduino 的版本，他称之为卡斯卡塔。卡斯卡塔在意大利语中是瀑布的意思，这与 Arduino 的原产地非常吻合

他选择的显示器是 SparkFun 的诺基亚 LCD 屏。它很容易插入，而且已经有了驱动显示器的库。音频输入只需使用一些电工胶带连接到耳机插头(你可以在上图的右下角找到它)。自由形式的电阻分压器确保信号在可测量的范围内。[Leigh]发现信号噪声有点问题，但通过在 VREF 和 GND 引脚之间的 Arduino 接头上增加一个电容，他能够改善结果。

休息之后看看它的实际效果。

[https://www.youtube.com/embed/o4oW2X8QVhk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/o4oW2X8QVhk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
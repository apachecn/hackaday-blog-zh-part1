# 后窗 LED 显示屏可以让其他驾驶员了解您的想法

> 原文：<https://hackaday.com/2011/10/20/rear-window-led-display-gives-other-drivers-a-piece-of-your-mind/>

![rear_window_led_matrix](img/64a0a8fb33109406f35b7a70d53e0a40.png "rear_window_led_matrix")

[Gagandeep]厌倦了高速公路上无礼的司机，所以他决定组织一次展示，让他们知道他对他们糟糕的驾驶技术的看法。他计划将显示屏安装在汽车的后窗上，因此他必须确保显示屏不会在驾驶时妨碍他的视线。

他认为 LED 矩阵是在旅途中显示图像和文本的最佳方式，因此他忙着为他的后窗构建 40×16 网格。他用一个木制模板来调整间距和位置，花了几天时间将 600 多个 led 焊接在一起。他使用 74HC595 移位寄存器来管理 5 列一组的 led，而 ATmega AT89C51 的任务是生成要显示的文本和图像。所有的 ICs 都被锁定在适当的位置，这有助于实现[Gagandeep]保持视线通畅的愿望。

虽然我们不太了解这种展示的合法性，但动画效果看起来很棒。在他的 Picasa 相册中有大量处于不同建设阶段的网格图片以及网格运行的视频[，所以一定要查看它们。如果你在寻找代码或 Eagle 文件，你可以在这里](https://picasaweb.google.com/104475112007830201673/LEDScroll)[找到。](https://docs.google.com/?pli=1#folders/0B5vWPuxrsdbDZjMyNjI0YWItZTg0OC00NzZjLTllZDItNDUyNjc2NTQ5ZDk5)
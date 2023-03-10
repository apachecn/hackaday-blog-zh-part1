# LED 生活和 Charlieplexing

> 原文：<https://hackaday.com/2008/10/24/led-life-and-charlieplexing/>

![](img/844369c81b8cb93eda6a1fddb028de4c.png "ledlife")
昨天，我们特别介绍了【安德鲁】的[方位感知相机](http://hackaday.com/2008/10/23/orientation-aware-camera/ "Orientation aware camera  - Hack a Day")。我们想强调他的另一个项目: [LED Life](http://ominoushum.com/life/ "LED Life") 。是一个 6×5 的 LED 矩阵在玩康威的生命游戏。他使用了低功耗的 MSP430 [，就像我们的电子纸时钟](http://hackaday.com/2008/10/14/how-to-make-an-e-paper-clock-and-hack-esquire-magazine/ "Make an e-paper clock from Esquire magazine  - Hack a Day")一样。这篇文章最精彩的部分是他对 Charlieplexing 工作方式的解释。微控制器 GPIO 引脚通常有三种可能的状态:输出高、输出低和输入。这与方向性发光二极管和一些创造性的布线相结合，意味着您只需几个 IO 引脚就可以运行一个可单独寻址的大型发光二极管矩阵。你可以改变它们的分配状态，而不仅仅是打开和关闭 IO 引脚。看看[Andrew]的网站，里面有一些关于这个系统如何工作的很好的例子。下面嵌入了他的 LED 生活板的视频。
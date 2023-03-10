# 用于光绘摄影的 LED 棒

> 原文：<https://hackaday.com/2011/07/11/led-wand-for-light-painting-photography/>

![](img/0b3cd9e3ca48c5230331f11ea2bdb352.png "Pacman's revenge")

[迈克尔·罗斯]是一名摄影师，最近迷上了光线绘画。他想出了自己的 RGB 光棒来创建一些令人惊叹的图像，还写了一个非常非常 T2 的教程，教你如何制作自己的光棒。

光棒基于 Arduino Mega 板，并使用基于 HL1606 控制器芯片的 RGB LED 灯条。我们在之前已经介绍过[这些 LED 灯条，它们非常容易与](http://hackaday.com/2009/06/17/addressable-rgb-led-strip/)[必备库](http://code.google.com/p/ledstrip/)一起使用。到目前为止，[迈克尔]已经建立了一个 48-LED 光棒和一个 6-位置程序选择器的 16-LED 光棒，使它很容易做可怕的单曝光照片[像这个](http://www.flickr.com/photos/txross/4318279412/in/set-72157627095796838)。

[Michael]在 Excel 电子表格中创建他的图像——行是地址，列是时间单位。然后将图片数据从 Excel 工作表直接复制并粘贴到 Arduino 源代码中。这本身就是 Excel 的一个非常巧妙的用法。

点击这里查看【迈克尔】如何创作他的一幅光画[。](http://www.flickr.com/photos/txross/4276026790/in/set-72157627095796838)
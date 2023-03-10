# Dippy Bird 二元时钟

> 原文：<https://hackaday.com/2011/09/11/dippy-bird-binary-clock/>

![](img/4fdaa25c96bf9c737aec950c97885047.png "drinking-bird-binary-clock")

这款 [Dippy Bird 时钟显示器](http://www.instructables.com/id/Drinking-Bird-Clock)制作简单，只需按比例放大就能用作一个完整的时钟。如图所示，在这个版本中，只有足够的鸟来读出时间。几分钟内可以添加更多层，你甚至可以使用一只单独的鸟作为温度计，添加自己的温度读数功能[。](http://hackaday.com/2011/08/23/can-a-dippy-bird-be-used-as-a-temperature-sensor/)

除了只有四位分辨率的事实之外，你应该注意到的第一件事是这些鸟没有什么可喝的。他们打算将喙浸入一杯水中，导致蒸发，改变里面二氯甲烷的温度，开始他们的摇摇晃晃。水没有被使用，因为鸟会不断运动。取而代之的是，在每个电池的底部都放置了一个电阻，当电流通过时，电阻就会发热。运动中的鸟是数字 1，静止的鸟是数字 0。一组晶体管保护微控制器不流出太多电流。在这种情况下，mbed 保持时间，但任何微控制器都可以。休息之后，我们嵌入了一个 dippy bird 时钟的快速剪辑。

[https://www.youtube.com/embed/-WRgB_GITY0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-WRgB_GITY0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
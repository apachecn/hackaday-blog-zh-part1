# 试图用 Arduino 来测量光速

> 原文：<https://hackaday.com/2011/12/01/trying-to-measure-the-speed-of-light-with-an-arduino/>

我们知道用 Arduino 测量光速是可能的。只是[实现难](http://blog.blinkenlight.net/2011/12/01/thank-you-world/)。

上个月我们看到了[Udo]的 [blinkenlight shield](http://hackaday.com/2011/11/01/turning-leds-into-a-camera/) 可以用作线扫描相机。这是一个整洁的套件，但[Udo]真的想为 [Buildlounge 激光切割机赠品](http://www.buildlounge.com/2011/10/07/buildlounge-and-full-spectrum-lasers-are-giving-away-a-laser-cutter/)提交一些东西，所以他认为测量光速将是一个简单的项目。如果一个[小孩和一块巧克力棒](http://www.youtube.com/watch?feature=player_embedded&v=9O2Keu6o3i0#!)能做到，那肯定不会太难。

[Udo]突发奇想，用脉冲激光笔测量反射的时间。因为他的闪光灯罩可以用作光传感器，所以只需要一面镜子和相当长的视线。不过这种设置有一些问题:Arduino 以 16 MHz 运行，一个光子在一个时钟周期内将传播 19 米。

即使有一些非常聪明的编码，我们也不确定在如此(相对)慢的时钟速度下检测一个发射的光子是可能的。我们认为[Udo]可以获得几百米长的光纤，这样整个实验可以放在一张桌子上，但是如果你有更好的想法，请随时在评论中留言。[Udo]的闪光灯/激光混搭演示在休息之后。

[https://www.youtube.com/embed/YrYRM3ApAoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YrYRM3ApAoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
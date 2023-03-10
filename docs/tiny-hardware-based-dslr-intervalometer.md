# 基于微型硬件的 DSLR 测距仪

> 原文：<https://hackaday.com/2011/06/27/tiny-hardware-based-dslr-intervalometer/>

![diy_dslr_intervalometer](img/5793001517935676447d4d4ecd352097.png "diy_dslr_intervalometer")

大多数 DSLR 相机有能力在设定的时间间隔拍照，但有时菜单系统会很笨重，选项往往不太理想。[Achim]是延时摄影的狂热爱好者，并一直在努力工作[创造一种基于硬件的间隔计](http://cms.diodenring.de/en/electronic/mikrocontroller/82-intervalltimerv2)来满足他的需求。他刚刚完成了控制器的第二次修改，它小到足以适合 2.5 毫米立体声插头的外壳。这种计时器并不是 100%通用的，但迄今为止，他已经证实它可以在尼康、佳能和宾得相机上工作。

基于 PIC10F222 的电路操作非常简单。一旦加密狗连接到你的相机上，你只需要在 0.4 秒到 18 分钟之间拍两张照片。intervalometer 会“观察”您在两次拍照之间等待了多长时间，并在这段时间间隔内继续拍摄，直到电池耗尽或存储卡填满。

正如你在他网站上的视频中所看到的，这个计时器非常好用。如果你想自己制作一个，可以访问他的网站，获取原理图和代码——这些都是免费的。

*哎呀，看起来我们实际上已经在之前[讨论过这个问题了。我们道歉。](http://hackaday.com/2010/08/06/miniscule-intervalometer/)
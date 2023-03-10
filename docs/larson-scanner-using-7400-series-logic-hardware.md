# 使用 7400 系列逻辑硬件的 Larson 扫描仪

> 原文：<https://hackaday.com/2011/04/20/larson-scanner-using-7400-series-logic-hardware/>

![](img/68f8c7e3eb4415651b9c2e6de11ea498.png "7400-larson-scanner")

[RandomTask]正在分享他几十年前制作的拉森扫描仪。现在你可以用 Arduino 在不到一个小时内做出一个这样的东西。他提到了这一点，但我们同意，出于怀旧的目的，没有什么比使用硬件实现扫描 LED 效果更好的了。

通常被称为赛昂之眼(在电视节目《太空堡垒卡拉狄加》之后)或被称为凯特前面的灯(来自《霹雳游侠》的汽车)，这种效果不仅仅涉及按正确的顺序开关 led。真正的 Larson 扫描仪会随着亮点远离 led 而使其褪色，导致尾部随着时间的推移而变暗。

该实现使用 555 定时器作为时钟信号，允许通过电位计进行速度控制。一个计数器芯片，J-K 触发器和线路解码器都互相合作，以解决最亮的光的移动。每个 LED 通过一个电容和一个电阻来控制衰减效果。休息后的视频显示了这一设置的令人满意的结果。

[https://www.youtube.com/embed/nbM1JpvKS_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nbM1JpvKS_A?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
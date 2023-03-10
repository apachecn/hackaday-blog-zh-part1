# 二进制时钟使用 DS3232 RTC

> 原文：<https://hackaday.com/2010/02/17/binary-clock-uses-ds3232-rtc/>

![](img/68c7afdbf61a57bd7d053f75683bf362.png "arduino-rtc-clock")

[肯尼斯·芬尼根]用他的基于 Arduino 的二进制时钟消除了我们对一天一个时钟的冲动。该时钟使用 5×7 LED 矩阵作为显示屏，显示月、日和时间。他采购了 DS3232 实时时钟，该时钟可以自动补偿温度，以实现非常精确的时间保持。我们喜欢他添加的超级电容电路，以便在断电时保持 RTC 运行。

Arduino 在这里是不是有点过了？好吧，代码当然不会填满 ATmega168 上可用的 16k。在 4.32 美元，你可以节省 1-2 美元，通过使用较低等级的芯片是不值得重写代码开发的原型。[Kenneth]还提到，这些项目通常只持续几周，然后就被重新用于下一次努力。

休息之后，看看[Kenneth]在视频中展示的高超硬件。如果你是清洁试验板的粉丝，他也制作了电路构建过程的延时。

[https://www.youtube.com/embed/2z051umtdBA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2z051umtdBA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

时钟组件说明

[https://www.youtube.com/embed/aPnveLrN4DA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aPnveLrN4DA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

电路建设的时间推移。
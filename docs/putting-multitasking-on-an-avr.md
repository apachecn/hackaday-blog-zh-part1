# 在 AVR 上进行多任务处理

> 原文：<https://hackaday.com/2012/03/26/putting-multitasking-on-an-avr/>

![](img/0283bf8e93bb662a3df38e7e293a107e.png "stack")

[vinod]想让自己熟悉 AVR 汇编编程，但想做一些比简单地闪烁 LED 更有雄心的事情。虽然完成的构建*确实让*闪烁了几个 led，但我们喜欢 e 决定在他的微控制器上实现[多任务处理。](http://blog.vinu.co.in/2012/03/multitasking-in-avr-atmega32.html)

[vinod]开发的程序使用[循环调度](http://en.wikipedia.org/wiki/Round-robin_scheduling)在每次定时器被触发时给七个编程任务中的一个一点计算时间。尽管与 VxWorks 这样的“现实生活”[实时操作系统](http://en.wikipedia.org/wiki/Real-time_operating_system)相比，它极其简单，但这仍然是一个令人印象深刻的成就。

在休息后的视频中，[vinod]展示了他用七个 led 进行的任务切换。白色 LED 是 PWM 任务，而其他六个 LED 是简单的切换任务，以相互独立的设定间隔打开和关闭 LED。如果没有某种时间表，这将很难做到——如果不是不可能的话。干得好，[vinod]。

[https://www.youtube.com/embed/HmduLzdfMhE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HmduLzdfMhE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
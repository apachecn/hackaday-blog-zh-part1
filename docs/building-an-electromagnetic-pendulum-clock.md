# 建造一个电磁摆钟

> 原文：<https://hackaday.com/2011/06/06/building-an-electromagnetic-pendulum-clock/>

![electromagnetic_pendulum_clock](img/eb3a55d989a6ab75e8d51ef85bebc051.png "electromagnetic_pendulum_clock")

为了给自己造一个时钟，斯蒂芬·霍布里一直在用电磁摆做实验。通过他的实验过程，他已经了解了很多关于钟摆是如何工作的，以及在不需要链条和重物的情况下保持钟摆运动的最佳方式，而链条和重物通常与这种类型的时钟相关联。

他的第一个实验是用脉冲马达驱动单摆。他发现保持钟摆运动的最简单的方法是使用一个线圈来检测它何时到达平衡点，通过向同一个线圈发送一个小脉冲来推动它。他注意到，如果他每隔三次触发磁线圈，他就可以保持钟摆以相当快的速度移动，所以他实现了一个 Arduino 来记录次数，并在需要时施加适当的力。

自从他的第一次实验以来，他已经取得了相当不错的进展，现在几乎所有的钟表作品都已经组装好了。他用木头制作，使用一个 15 齿的主驱动棘轮，为两个负责记录秒的 60 齿齿轮以及一对跟踪分钟和小时的较大齿轮提供动力。

目前为止看起来不错，我们等不及要看它完工时的样子了。

留下来看一个时钟及其所有传动装置的快速视频演示。

[https://www.youtube.com/embed/ekqBGOcKuJM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ekqBGOcKuJM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
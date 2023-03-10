# 使用 SN754410 的 DC 电机控制简介

> 原文：<https://hackaday.com/2011/07/21/intro-to-dc-motor-control-using-the-sn754410/>

![](img/aeda3420335c16dbfa74077a74e06cf2.png "sn754410-motor-driver-primer")

因此，你的电子爱好技能进展得相当不错，但除了闪烁几个发光二极管之外，你不会感到很舒服。现在是尝试新事物的好时机，驾驶几辆 DC 汽车。

你可能知道，你不能只是把它们挂在你最喜欢的 uC 的引脚上，然后说它很好。电机消耗大量电流(特别是当它们在提升一个重负载的时候)会烧坏你的逻辑电路。除此之外，旋转电机关闭时会产生额外的感应电流，你需要一个控制系统来应对这些危险。

进入 h 桥电机驱动器。[Chris]已经指导我们完成了过去建造和使用 H 桥的过程。这一次，他使用了内置四个半 H 桥的电机控制器。他将 SN754410 连接到两个电机上，根据进入芯片的 PWM 信号的占空比来控制两个电机的速度和方向，成本不到 2.50 美元。休息后观看视频，了解他的方法概述，然后阅读他最近发表的多页文章。

[https://www.youtube.com/embed/UzdSUYf7SLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/UzdSUYf7SLo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# Launchpad 将超低功耗发挥到极致

> 原文：<https://hackaday.com/2010/09/30/launchpad-takes-ultra-low-power-to-the-extreme/>

![](img/41862543b5c9ba14f84c73c5287e027e.png "I'm betting it lasts a month and a half. You?")

我们都知道 Launchpad 下的 MSP430s 被设计成低功耗，但谁想赌一下[仅用价值 20F 的电容器，芯片就能持续](http://kennethfinnegan.blogspot.com/2010/09/msp430-low-power-experiment.html)多久？几个小时？最多一天？[Kenneth Finnegan]设置一个带超级电容的 MSP430 来找出答案。为了确保芯片确实在运行，[Kenneth]对它进行了编程，让它在 10 秒内从 0 数到 9，然后复位。为了获得超低功耗，芯片大部分时间都处于睡眠模式，并使用原始低电流 LCD 来显示输出。虽然[Kenneth]只是每隔几个小时检查一下芯片，看看它是否还在计数，但一个非常类似于[闪光毁灭者](http://hackaday.com/2010/06/14/update-flash_destroyer-final-destroys-eeprom/)的设置，跟踪一个时钟，然后存储当前值，将会获得更准确的死亡时间。不管怎样，已经过去 3 周了…还在继续。裂痕后的视频。

[https://www.youtube.com/embed/xbjpQmjwMyU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xbjpQmjwMyU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
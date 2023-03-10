# 纯 TTL 时钟

> 原文：<https://hackaday.com/2010/03/16/pure-ttl-based-clock/>

![](img/849a1d2fc3a857e233faadb50830b972.png "I will give a shiny nickle to whoever can make a 12 hour 7400 series based TTL clock.")

我们就说，[肯尼斯]真的很喜欢钟表。他最近的一款是基于纯 7400 系列 TTL 的，即没有微控制器，如[过去的](http://hackaday.com/2010/02/17/binary-clock-uses-ds3232-rtc/)、[这里的](http://kennethfinnegan.blogspot.com/2009/11/seven-segment-led-arduino-clock.html)、[这里的](http://kennethfinnegan.blogspot.com/2010/01/arduino-four-digit-clock.html)和[这里的](http://kennethfinnegan.blogspot.com/2010/01/arduino-binary-clock.html)。信号开始时是一个典型的 32，768 晶振，分频至所需的 1Hz，然后再次进行适当分频，以提供小时和分钟。

就 TTL 时钟而言，这并不是什么太新颖的东西；直到他的创意按钮界面。通过使用一个不像听起来那么性感的多谐振荡器，他可以产生一个干净的方波，而不是按钮产生的数字信号来推进和设置时间。像往常一样，他也为我们提供了他的时钟，跳跃后彻底崩溃。

[https://www.youtube.com/embed/rzDe7GBJ0V8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rzDe7GBJ0V8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# Wifon 回来了，比以前更好

> 原文：<https://hackaday.com/2011/06/08/wifon-is-back-and-better-than-ever/>

![wifon_v2](img/26b29e633117fa6ee8a4a88af0cc458b.png "wifon_v2")

Hackaday 论坛成员[Emeryth]最近发布了他的最新创作[，Wifon 2.0](http://emerythacks.blogspot.com/2011/04/wifon-20.html) ，这是我们去年重点介绍的项目的更新[。该设备的第二次迭代看起来要在已经稳固的概念上做一些改进。](http://hackaday.com/2010/08/14/portable-wifi-penetration-testing/)

抛弃了简单的 16×4 LCD，第二版配备了全彩色 320×240 触摸面板 LCD。一个更快的 STM32 微控制器取代了他第一次使用的 Atmega88，使他能够创建一个更高级的用户界面。微处理器运行 ChibiOS/RT 实时操作系统，支持多任务处理，使整个项目变得更加容易。像第一个版本一样，最初的 Fonera 执行所有的 pen 测试，尽管这一次他放弃了普通的 DD-WRT 发行版，转而使用 Jasager，这是专门为运行 Karma 攻击而构建的。

该项目进展顺利，[Emeryth]说他已经有几个简单的应用程序在设备上运行。他发现在设备上同时运行几个应用程序正在测试 Foneras 功能的实际极限，尽管他可能会给路由器增加更多的内存，以便从中挤出更多的生命。

[通过[黑客日论坛](http://forums.hackaday.com/viewtopic.php?f=3&t=762)
# 另一个更智能的热水器定时器

> 原文：<https://hackaday.com/2011/06/09/another-smarter-water-heater-timer/>

![](img/4fb654bbfe55a4fcae282e4f363c8fb3.png "2011_06_05_14_50_26")

当粘在热水器上的纸条失效时，[Ryan]决定用一个伺服系统、一个实时时钟，当然还有一个 Arduino，制造出"[世界上最昂贵的 240V 继电器](http://ibuildthings.ryanblace.com/2011/06/smarter-hot-water-heater-timer.html "main link")。多亏了洛杉矶的“分时度假计划”，所有这些都是为了节省一两块钱。

Ryan 用 DS1307 芯片焊接了一个 RTC 模块。在船上，他添加了一些 LED 和开关，包括一个节日开关，让加热器保持关闭，当你需要一些热水时，下一个循环按钮，让费用见鬼去吧，还有一个脉冲蓝色 LED..没有任何理由。该板使用伺服和钢琴线翻转机械开关，简单而有效。我们想知道它需要几天/几周来抵消它的费用？
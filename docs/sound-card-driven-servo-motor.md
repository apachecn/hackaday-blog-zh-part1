# 声卡驱动的伺服电机

> 原文：<https://hackaday.com/2010/05/26/sound-card-driven-servo-motor/>

[https://www.youtube.com/embed/1LG2Ecsk13Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1LG2Ecsk13Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

【达雷尔】正在[用声卡驱动这个伺服](http://www.youtube.com/watch?v=1LG2Ecsk13Q)电机。电机从手机电池中获取能量，控制信号来自其中一个音频通道。这并不令人惊讶，因为电机只需要[一个 PWM 信号](http://en.wikipedia.org/wiki/Pulse-width_modulation)来操作，这就是用来在电子扬声器上产生不同频率声音的东西。我们不确定[达雷尔的]对这个系统有什么计划，但他提到可以使用两个伺服系统，每个音频通道一个。如果你不使用你的声卡，这将是一个停止使用 Arduino 的方法，只需使用一个附在伺服系统上的小标志就可以了[邮件检查器](http://hackaday.com/2009/09/05/arduino-email-alert/)。当邮件进来时，适当设计的声音会升起旗帜。
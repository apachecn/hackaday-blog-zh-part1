# 简单的电路提醒你冲出家门时要锁门

> 原文：<https://hackaday.com/2011/10/11/simple-circuit-reminds-you-to-lock-the-door-as-you-rush-out-of-the-house/>

![door_lock_minder](img/7fef47ce3e7c5379bbd33def404e466f.png "door_lock_minder")

似乎[pppd]总是冲出他的公寓去赶公共汽车，他发现自己经常问自己是否记得锁门。他经常回去查看，虽然他从来没有忘记锁门，但他宁愿不去担心。

由于他终于有了一些空闲时间，他决定组装一个简单的装置来彻底结束他的担忧。[pppd]利用 ATtiny13 设计了一种电路，可以检测到他的门何时被解锁和打开，每隔几秒钟就会发出蜂鸣声，直到锁被重新锁上。电路依赖于安装在门框内的簧片开关，这个开关被他粘在门插销上的磁铁触发。

他说这个系统到目前为止运行良好，尽管他已经有了一些改进的想法。
# IPod Shuffle 耳机遥控器反向工程

> 原文：<https://hackaday.com/2010/02/13/ipod-shuffle-headphone-remote-reverse-engineered/>

![](img/a37bec244282bebca92771c9e41e7188.png "reverse-engineered-ipod-headphone-remote")

第三代 iPod shuffle 的耳机遥控器有一个特殊的芯片，可以识别 iPod 本身。[David Carne]发布了一份关于他用来逆向工程协议的过程的深度报告。他发现，当设备通电时，遥控器使用一种特殊的信号来识别它的真实性。我们之前已经讨论过[苹果对外设授权](http://hackaday.com/2010/01/13/tricking-an-ipod-into-trusting-your-dock/)的使用，看起来这没什么不同。[David]使用 ATmega88 成功模拟了身份验证。如果你有一个 shuffle 3G，这些信息将允许你在下一个项目中用微控制器来操作它。
# DIY 应急照明系统

> 原文：<https://hackaday.com/2011/02/21/diy-emergency-lighting-system/>

![diy_emergency_lighting_system](img/ef79339e4c9349a72b23beb820672b4c.png "diy_emergency_lighting_system")

当家里停电时，你怎么办？我们中的大多数人可能会在屋子里爬来爬去寻找手电筒。[Gigawatts]想要一个更好的解决方案，所以他[在标准家用 UPS 的基础上建造了一个应急照明系统](http://stupidhax.blogspot.com/2011/02/stupid-hack-2.html)。不久前，他让[建造了一个继电器开关插座盒](http://hackaday.com/2010/06/29/power-cycling-a-problematic-modem/)来帮助周期性地重启他的电缆调制解调器，因为他不喜欢电缆调制解调器过于频繁地被挂断。由于更换了互联网提供商，他不再需要开关插座盒，并在寻找一种重复使用它的方法。

他将出线盒连接到 UPS 的“电池供电”侧，并将一个灯泡插入开关盒常闭的那一半。5v 电源接入 UPS 的“仅电涌保护”侧，用于保持继电器的开关状态。这使得通常关闭的开关盒的一半保持打开，并且灯关闭。断电时，5v 电源不再切换继电器，灯打开，由 UPS 电池供电。

如果你碰巧有一个备用的 UPS，这是一个非常有用的技巧——它肯定比在黑暗中四处寻找手电筒要好！
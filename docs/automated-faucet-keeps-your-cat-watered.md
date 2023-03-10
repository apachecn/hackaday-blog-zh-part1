# 自动水龙头保持你的猫浇水

> 原文：<https://hackaday.com/2011/05/24/automated-faucet-keeps-your-cat-watered/>

![](img/07313dd82f2d3b9b5ee78575e22e01b2.png "catsensor")

像我们许多人一样，克里斯·狄龙的猫更喜欢直接从水龙头里喝新鲜的冷水。然而，与我们不同的是，[克里斯]的猫伙伴太专注于猫的东西，以至于在用完之后懒得去关水龙头。事实证明，这不仅是[Chris]展示其项目实力的绝佳机会，也为未来的家庭自动化项目奠定了基础。虽然我们大多数人可能会选择一个简单的螺线管，但克里斯必须让这个装置完全可逆。结果是一个自动化的[水龙头控制](http://squarism.com/2011/03/09/arduino-cat-faucet-with-mongodb-and-rails/)，它包括一个红外传感器、Arduino 和一个带有伺服系统的紧密配合轨道系统，以操作水槽手柄。

在整理好所有的硬件和传感器后,[Chris]继续添加数据记录 PC。水龙头设置通过 Xbee 模块与 Linux 服务器通信，并填充一个 [MongoDB](http://en.wikipedia.org/wiki/MongoDB) 数据库。该设置甚至允许[Chris]标记误报(例如人类水槽的使用),并制作他的猫朋友的用水量图表。我们怀疑那只猫收到水费单后会不高兴。

不要忘记查看[Chris Dillon]的[网站](http://squarism.com/2011/03/09/arduino-cat-faucet-with-mongodb-and-rails/)了解项目细节，包括代码和经验教训列表。还有，既然这毕竟是互联网，[我们](http://hackaday.com/2008/09/16/hack-your-littler-box/) [有](http://hackaday.com/2008/11/07/catgenie-hacking/) [几个](http://hackaday.com/2010/01/31/recycled-cat-feeder/) [其他](http://hackaday.com/2010/07/17/rfid-cat-feeder-helps-with-the-diet/) [猫](http://hackaday.com/2010/07/19/avr-guardian-filters-out-dogs/) [相关](http://hackaday.com/2008/05/31/robotic-cats/) [项目](http://hackaday.com/2011/01/31/out-engineering-a-sneaky-cat/) [为](http://hackaday.com/2009/06/24/wireless-arduino-cat-food-dispenser/) [贵](http://hackaday.com/2009/05/27/catalog-rfid-cat-tracking/) [观赏](http://hackaday.com/2009/12/03/internet-enabled-cat-feeder/) [快感](http://hackaday.com/2011/05/22/hacking-for-feline-enjoyment/)。

[感谢克里斯·布伦斯(和侄子)]

查看跳跃后运行中的设置视频。

[https://www.youtube.com/embed/T0-EQqTW3Og?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T0-EQqTW3Og?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
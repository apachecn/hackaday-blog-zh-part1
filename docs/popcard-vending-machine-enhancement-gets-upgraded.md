# PopCARD 自动售货机升级

> 原文：<https://hackaday.com/2011/10/17/popcard-vending-machine-enhancement-gets-upgraded/>

![](img/dae1dc7d0b821e9c7b325d58d2c2ffdf.png "popcard-upgrade")

[亚历克斯]写信告诉我们，他刚刚完成了对他的 PopCARD RFID 自动售货机系统的一次重大升级。你可能还记得今年早些时候，他[在一台汽水机](http://hackaday.com/2011/04/04/rfid-drink-system-eliminates-the-need-for-change/)上添加了一个基于 Arduino 的 RFID 阅读器，这样口渴的顾客就可以用塑料而不是现金支付了。这个系统是有效的，但是在广告之后的视频开始时,[Alex]提到了它的一些缺陷。有一个按钮可以将现金从卡中以 1 美元的增量添加到机器中，而不是系统只知道要收你多少钱。此外，如果你不小心选择了缺货的商品，你就不走运了，无论如何都要付费。

新系统取消了按钮，知道什么产品卖完了。控制硬件升级到 Arduino mega 以获得额外的 I/O 引脚。这个设备现在位于机器的按钮和它自己的控制器之间。当使用现金时，Arduino 被动地坐着，让机器做它的事情。但是当卡片被扫描时，它会接管按钮的控制权，感知你的选择，然后模拟硬币和按钮的按下来进行相应的销售。新的设置还使用了一个以太网屏蔽，使[Alex]能够在不在机器本身的情况下判断哪些项目正在减少。

[https://www.youtube.com/embed/qAXSO_yA7nk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/qAXSO_yA7nk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
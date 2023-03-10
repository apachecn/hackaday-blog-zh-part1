# 给坏掉的 IPod 注入新的生命

> 原文：<https://hackaday.com/2011/03/28/breathing-new-life-into-a-broken-ipod/>

![ipad_nano_button_fix](img/7829a463928a68c5eef25651c6e3523e.png "ipad_nano_button_fix")

[克雷格]有一个坏掉的第二代 iPod Nano，已经过了保修期。播放/暂停按钮不再工作，使他无法播放或暂停音乐，也无法关闭设备。他不想废弃 iPod，所以他想出了一个办法[增加一个外部播放/暂停按钮来代替](http://flashingleds.wordpress.com/2011/03/27/fixing-a-broken-ipod/)。

他从 SparkFun 订购了一个 iPod 基座连接器，发现它的内部空间刚好够他添加电子元件。他查阅了一些关于引出线信息的在线参考资料，然后忙着把一个天线和一个按钮塞进基座连接器。

为了最大限度地减少 iPod 电池的消耗，他在不使用时将 ATiny 设置为睡眠模式。当按下按钮时，它会唤醒微控制器，并向 iPod 发送适当的信号。根据他的估计，ATiny 需要将近 250 年的时间才能完全耗尽 iPod 的电池，所以他很乐意让加密狗一直连接着。

如果你有一个 iPod 也有类似的问题，他已经公开了他的源代码，所以你也可以把你的从垃圾堆里救出来。
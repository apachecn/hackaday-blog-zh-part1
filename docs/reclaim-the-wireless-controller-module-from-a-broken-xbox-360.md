# 从损坏的 Xbox 360 中回收无线控制器模块

> 原文：<https://hackaday.com/2012/02/03/reclaim-the-wireless-controller-module-from-a-broken-xbox-360/>

![](img/fa76d9b4e8fa94057bc7f47ddedd2f66.png "salvage-rf-controller-module-from-xbox-360")

如果你是 Xbox 360 死于与 RRoD 相关的大火的一员，你可能会想知道如何处理你剩下的那个数百美元的门挡。为什么不把零件抢救出来作其他用途呢？如果你曾经想在电脑上使用你的无线控制器，这里有一种方法可以拔出射频模块并重复使用。

这个概念很简单，Xbox 360 中有一个子板，它承载无线控制器连接的 RF 模块。一旦你把它从野兽的尸体中提取出来，你只需要找到一种方法来读取并把数据推送到你的电脑上。任何支持 USB 的微控制器都可以，在这种情况下，Arduino nano 被选择用于该任务。与设备接口时，需要进行一些电平转换，但这并不太复杂。

听起来，起初在将控制器与被黑模块同步时出现了问题，但正如你在休息后的剪辑中看到的那样，问题已经解决了。

[https://www.youtube.com/embed/k_bjYME1ys8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/k_bjYME1ys8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[通过[建立休息室](http://www.buildlounge.com/2012/02/02/rip-the-pieces-out-of-your-dead-xbox360-to-use-the-wireless-controllers-on-your-pc/)
# 使用 Droid Bionic 作为移动热点，无需支付额外费用

> 原文：<https://hackaday.com/2011/09/13/use-droid-bionic-as-a-mobile-hotspot-without-paying-extra/>

![](img/a5f946a7952d13d4894f6e34321091f4.png "droid-bionic-hotspot")

显然，如果威瑞森用户想被允许使用手机作为移动热点，他们需要支付第二个数据计划。这意味着一个数据计划用于手机，另一个用于网络共享。[DroidBionicRoot]认为这有点傻，因为手机计划中已经有数据上限了。但是如果你不介意的话，他已经找到了一种方法来解决这个问题。

毫不奇怪，这是一个非常简单的改变。该手机已经能够网络共享，要启用该功能，无需威瑞森的许可，只需编辑一个数据库值。在休息后的视频中，[DroidBionicRoot]用一个根深蒂固的机器人仿生手机开始了这个过程。他花 2.99 美元买了一个应用程序，可以在手机上编辑 SQL 数据库。从那里，他导航到“设置存储”数据库，并将“权限 _ 检查”键值更改为 0。重启手机，网络共享现在解锁。

[https://www.youtube.com/embed/vuSHY7ed0oU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vuSHY7ed0oU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢麦克斯]
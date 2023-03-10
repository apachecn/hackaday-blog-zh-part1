# 博比板驱动的 Twitter 通知程序

> 原文：<https://hackaday.com/2011/07/01/boobie-board-powered-twitter-notifier/>

![boobie_board_twitter_notifier](img/fa3e6407689bdfe06b994a3402c11a7e.png "boobie_board_twitter_notifier")

Archonix 的团队经常挑战自己，在 20 分钟内创建一个完整的工作项目。[安德鲁·阿姆斯特朗]写了一篇博客，详细介绍了他们最近的“快速项目”——[一个简单的 Twitter 通知程序，使用他们的 Boobie Board](http://www.archonix.co.uk/corporate/?p=1178) 构建。

他们首先组装了一个小的通知器突破模块，该模块后来可以附加到他们的 Boobie 板上。该模块非常简单，包括三个发光二极管，提醒你几个在线服务的活动，尽管目前只有 Twitter 通知模块是完整的。通告程序的代码是在 LUA 编写的，主要是为了与 Linux 桌面交互而设计的。他们目前没有可用的 Windows 兼容版本的代码，但是如果有人希望移植他们的代码，他们非常乐意托管它。

通知者被放入一个有塑料窗的旧糖果罐中，这非常适合他们的项目。总而言之，整个过程花了他们大约 40 分钟，一半花在硬件上，一半花在代码上。通知程序只是做了它想要做的事情，但是他们有一个健康的改进列表，他们希望添加，包括使用其他两个通知程序 led。
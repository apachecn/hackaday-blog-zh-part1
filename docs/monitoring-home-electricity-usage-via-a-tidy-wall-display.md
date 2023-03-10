# 通过整洁的墙壁显示屏监控家庭用电情况

> 原文：<https://hackaday.com/2012/03/06/monitoring-home-electricity-usage-via-a-tidy-wall-display/>

![power-meter-display](img/b73830f0e2e7523735aee8850d5008db.png "power-meter-display")

[Janne mntyharju][想知道他的新家用了多少电](http://antibore.wordpress.com/2012/03/05/monitoring-electricity-usage-at-home/)，主要是想看看使用壁炉提供额外热量对他的账单有没有影响。幸运的是，他的电表安装在他家的杂物间里，便于监控他的使用情况。

他的电表有一个小 LED，每度电闪烁固定次数，所以他安装了一个光敏电阻，并在上面安装了 2313 来检测光脉冲。[Janne 的]服务器通过 XBee 连接每 5 分钟轮询一次微控制器，在 SQL 数据库中记录用电量以供进一步分析。从这个数据库中，他可以生成图表，显示他家中的温度以及特定时间段的平均用电量。

[Janne]还想让数据更容易获取，[所以他用一个 Beagleboard 和数码相框建造了一个壁挂式显示器](http://antibore.wordpress.com/2012/03/05/info-display-for-home/)。显示屏不仅显示他的用电量，还可以在天气、日历事件、IRC 日志和安全摄像头的图片之间切换。

在之前，我们肯定见过[这种电表监控，但它可以快速提醒我们，如果有合适的工具，观察你的用电量(以及其他事情)就像快速瞥一眼墙壁一样简单。](http://hackaday.com/2011/05/13/monitor-your-homes-power-usage-on-the-cheap/)
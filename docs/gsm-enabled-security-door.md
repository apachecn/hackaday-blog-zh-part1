# 启用 GSM 的安全门

> 原文：<https://hackaday.com/2009/11/28/gsm-enabled-security-door/>

![](img/870c57fb38ce30d9d3456b988fa18ed1.png "cell_operated_security_door")

[奥利弗的]大楼前面的安全门使用对讲系统让客人远程进入。每个单元都有一个带开门按钮的对讲机。[奥利弗]想要一种不用携带任何额外物品就能进入的方法，所以他建造了一个用手机开门的系统。

他接入对讲机，连接了一个 GSM 模块。该模块运行 python，因此他编写了一个脚本来监控入口通道蜂鸣器，然后等待批准的手机连接来解锁它。他为最终项目经历了几次不同的迭代。第一次尝试使用 XBee 模块在对讲机手机和 GSM 模块之间进行通信。在最终版本中，他用稀土磁铁将电缆穿过墙壁(很有创意！)以便放弃手机中电池的使用。

谁不随身带手机？正因为如此，我们认为在自动化中使用 [GSM 模块将会继续流行。](http://hackaday.com/2009/09/01/tiny-gsm-alarm-system/)
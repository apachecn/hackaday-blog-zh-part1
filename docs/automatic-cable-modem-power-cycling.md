# 自动电缆调制解调器电源循环

> 原文：<https://hackaday.com/2007/06/22/automatic-cable-modem-power-cycling/>

如果你有一个电缆调制解调器，当它离线时，你知道该怎么做。拔掉插头，等待 30 秒，再插上，重新设置您的 dhcp 请求。我很确定[brian]在不久前的评论中提到过[这个](http://www.evillawngnome.com/2007/06/20/using-x10-home-automation-and-linux-to-manage-your-home-internet-connection/)，但是现在他把它写了出来。他在他的 linux 机器上使用 cron 作业来检查互联网连接，如果测试失败，则使用一些 X10 硬件和一点脚本来重启硬件。(不要告诉你的朋友，否则他们会在外面猜密码。)

*   [永久链接](http://www.evillawngnome.com/2007/06/20/using-x10-home-automation-and-linux-to-manage-your-home-internet-connection/)
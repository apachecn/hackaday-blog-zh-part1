# 有了这款公交车到站通知器，您再也不会错过交通工具

> 原文：<https://hackaday.com/2012/03/19/never-miss-your-transport-with-this-bus-arrival-notifier/>

![](img/e4956af42cabac2e334e821f654233c1.png "router-based-bus-notifier")

约翰·格雷厄姆·卡明已经准备好开始一个基于树莓派的新项目。嗯，那是直到装运由于制造问题被延迟。不要担心，他过渡到一个路由器板，上面显示公共交通服务的到达倒计时。

他基于伦敦交通局提供的一个网页进行建造。你可以加载它，看看你的公共汽车是否准时运行。没有公开的 API，但是通过研究该网站的源代码，[John]能够弄清楚 JSON 命令是如何格式化的。

下一步是构建一个独立的设备来提取数据并显示出来。上面看到的板来自 Linksys WRT54GL 路由器。这个长期的最爱有一个串口头，可以从 Linux 内核驱动。他在路由器的外壳上连接了一个插孔，并使用一根延长线将其连接到安装在一个总线模型上的 7 段显示器上。由于有四个数字，显示屏可以告诉你，直到两个不同的公共汽车到达分钟。

[感谢伪龙虾]
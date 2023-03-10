# 关于 WEP 破解的有趣观点

> 原文：<https://hackaday.com/2010/10/07/an-interesting-take-on-wep-cracking/>

![](img/a010364103388b4105b7c8a81f9fed0a.png "wepcrack04")

[本·库尔茨]正在做一点 WEP 破解,但以一种与我们习惯的方式有点不同的方式。WEP 破解让我们想到了战争驾驶；开着笔记本开车到处跑，寻找 WiFi 接入点，找到了就停下来运行一些软件。[本]的方式类似，但在一个关键方面不同，他使用 iPhone 作为前端。

这开始是为了找到一些剩余设备的用途。他把一个 Linux 盒子扔在一起，装上了我们经常看到的[用于渗透测试](http://hackaday.com/tag/aircrack-ng/)的软件 [Aircrack-ng](http://www.aircrack-ng.org/) 。为了避免在公共场合从事可疑的活动，他用 Python 包 [Turbogears](http://turbogears.org/) 编写了一个网络界面。它使用 screen，这是一个经常与 SSH 一起使用的程序，可以在不同的终端上同时运行服务，并且可以选择在不停止进程的情况下断开连接。现在只需将硬件停在接入点附近，然后在移动设备上的浏览器中完成工作。你可以在上面链接的他的帖子中查看他写的脚本以及安装说明。

[感谢技术 b]

[注意:横幅图片与本文没有直接关系]
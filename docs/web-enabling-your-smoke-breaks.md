# 网络-让你戒烟

> 原文：<https://hackaday.com/2011/02/28/web-enabling-your-smoke-breaks/>

![](img/8b56dd64b211b5bf1dfd484e012ca763.png "web-enabled-smoke-breaks")

如果你打算在隆冬的时候不抽烟，那么你出去的时候最好有人陪着。[扎克的]公司想要处理一些关于吸烟休息时间和员工生产率的数据。他决定增加功能，而不是仅仅满足乏味的数据收集需求。

他花时间解释了系统的不同部分。上面你可以看到一个网络界面，让你知道你的哪些同事正在吸烟。它还能让你在休息时点击签到和签出。在这个系统运行之后，他发现吸烟者经常忘记在休息前“打卡下班”。作为备份系统，他在离开办公室的路上建立了一个物理接口。每个吸烟者都有自己的按钮和相应的 LED。如果灯亮着，你在休息，如果灯灭了，你在工作。该控制器基于 Arduino，使用 Perl 脚本来监控输入，并同步物理显示器和 web 界面。[扎克] [贴了几张图片](http://032koncept.imgur.com/diy_smoketracker)如果你想看看系统的其余部分。
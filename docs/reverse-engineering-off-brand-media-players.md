# 对非品牌媒体播放器进行逆向工程

> 原文：<https://hackaday.com/2009/12/23/reverse-engineering-off-brand-media-players/>

![](img/c45b1ff837f87699d4909299e433c7ef.png "hackable-33-dollar-media-player")

[Marcan]以便宜的价格买到了这个设备，并且正在对控制器进行逆向工程。这个媒体播放器是一个非品牌的中国型号，[可以以 33.97 美元的低价买到，并且免费送货。这是值得的，只是为了清除其他项目的部分，但这里的挑战是破解控制器，因为从来没有为它制作数据表。预热您的逻辑分析仪，查看](http://www.dealextreme.com/details.dx/sku.21968) [wiki](http://spmp305x.spritesserver.nl/wiki/index.php) ，您马上就可以开始研究这个基于 [ARM926EJ-S](http://www.arm.com/products/CPUs/ARM926EJ-S.html) 的系统。

战斗的号令来自[马尔康的]博客。你可能记得他是努力在 Linux 中巩固 iPhone 同步的人，或者…他还做了什么？哦，是的，不久前他有一个小项目叫做 [Wii 自制频道](http://wiibrew.org/wiki/Homebrew_Channel)。参与其中，你可以向那些真正知道自己在做什么的人学习。

[谢谢探索者先生]
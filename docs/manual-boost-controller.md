# 手动升压控制器

> 原文：<https://hackaday.com/2005/06/18/manual-boost-controller/>

![turbo](img/9f28f09bc464706ef0ae95a7488a0b62.png)

建立一个升压控制器是一个“滑坡”式的模式。一旦你完成了这个，你就会想要/需要修改系统中的其他东西。涡轮增压器通过向发动机注入尽可能多的空气和燃料来提高发动机的性能。发动机排气驱动涡轮中的叶轮，该叶轮驱动进气道中的压缩轮。发动机无法承受极端压力，因此一旦进气压力达到工厂设定值，“废气门”就会打开，让废气绕过驱动叶轮，这样涡轮就不会产生更多的增压。工厂增压设置通常非常保守(否则，他们会做很多维修)，所以有很大的改进潜力。

手动升压控制器被放置在废气门传感器的路径上。控制器排出管路中的一些压力，使得废气门处测得的压力低于实际压力。这使得废气门比平时关闭的时间更长，从而达到更高的增压水平。建造它们真的很便宜，但是这个项目中最重要的花费是获得精确的助推压力计。一点点出血会持续很长时间，如果没有合适的计量器，就无法知道你在哪里。DSMtuners 有不少关于如何构建这些设备的文章，应该可以在几乎所有的涡轮车上使用。

*   [永久链接](http://www.dsmtuners.com/forums/forumdisplay.php?s=&forumid=35)
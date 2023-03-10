# 控制带有回收部件的台面蒸馏水器

> 原文：<https://hackaday.com/2011/07/11/controlling-a-counter-top-water-distiller-with-salvaged-parts/>

![distiller_power_off_timer](img/bbbfc6bfb8f7eedadf4cceaa1f0da87c.png "distiller_power_off_timer")

Hackaday 读者[Kyle]来信分享了他最近完成的一个项目，涉及他在家中使用的一个[台式水蒸馏装置](https://picasaweb.google.com/101441616403188866046/20110710Distill)。

他住在亚特兰大，讨厌水中的味道和污染物，所以在他家里使用这个蒸馏器是绝对必要的。这种廉价装置的问题是，它要等到完全干燥后才能关闭加热元件。根据[凯尔]这带来了两个大问题。

首先，让设备变干只会蒸发掉他试图清除的所有污染物，让它们重新凝结并污染他的淡水。第二，一旦水消失，加热元件达到极端温度，这导致蒸馏单元过早失效。

他原本用一个计时器来提醒自己在电池耗尽之前关掉电池，但是这个过程变得很繁琐。他发现自己经常会忘记关掉蒸馏器，以免它污染了他刚洗干净的水。

为了寻找另一种解决方案，他决定使用他不久前构建的基于 Arduino 的玻璃容器温度/湿度控制器的一些剩余组件来自动化这个过程。一个回收的玩具钟楼被用作输入盘，它在微控制器上设置蒸馏时间。Arduino 反过来管理一组控制蒸馏器电源的继电器。

虽然[凯尔]只通过电子邮件向我们发送了这些信息，但他已经在网上发布了[代码](https://github.com/kizniche/Auto-Distiller/blob/master/still.pde)和[图片](https://picasaweb.google.com/101441616403188866046/20110710Distill)。我们相信他会很乐意回答你关于他身材的任何问题，所以请在评论区提问。

[更新]
在看到他的蒸馏器上了头版之后，[凯尔]指引我们看了[他为](http://autodidaktosanthropos.blogspot.com/2011/07/autodisstiller.html)准备的一份报告，详细介绍了该项目的一些细节。
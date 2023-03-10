# 开源神经活动监视器

> 原文：<https://hackaday.com/2008/09/19/open-source-neural-activity-monitors/>

![](img/659663bfc0e95d8ac2c1a92fc4270da6.png "diy_electrodes")

昨天我们联系了一个 [OCZ 神经激活器接口拆除](http://hackaday.com/2008/09/18/ocz-neural-impulse-actuator-teardown/)。评论中有几个人想知道更多关于传感器电极的信息。查看 [OpenEEG 项目](http://openeeg.sourceforge.net/doc/index.html)和 [OpenEEG 邮件列表](https://lists.sourceforge.net/lists/listinfo/openeeg-list)，获取关于感知、放大和记录大脑活动的信息( [EEG](http://en.wikipedia.org/wiki/Electroencephalography) )。OpenEEG 项目保持了开源的简单模块设计。ModularEEG 的另外两个开源变体是[monolithieeg](http://freenet-homepage.de/moosec/projekte/simpleeeg/index-Dateien/MonolithEEG13_e.htm)和【Joshua Wojnas’】[可编程芯片脑电图 BCI](http://pceeg.sourceforge.net/) 。这三个项目都使用了 [Atmel](http://www.atmel.com/) 微控制器，设计在 [Cadsoft Eagle](http://www.cadsoft.de/) 中。

大脑活动是用被动电极(T0)或主动电极(T3)来测量的。无源电极需要导电胶才能与皮肤适当接触(例如: [1](http://openeeg.sourceforge.net/buildeeg/electrodes.php) 、 [2](http://openeeg.sourceforge.net/doc/gallery/joe/index.html) )。主动 EEG 传感器不需要导电 goop，因为它们在电极上直接有一个放大器(例如: [1](http://openeeg.sourceforge.net/doc/hw/joe_ae/) 、 [2](http://uazu.net/eeg/ae.html) 、 [3](http://www.dcc.uchile.cl/~peortega/ae/) )。

[通过匿名读者，评论]
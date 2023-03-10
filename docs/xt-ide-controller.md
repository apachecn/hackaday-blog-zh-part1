# XT IDE 控制器

> 原文：<https://hackaday.com/2010/07/31/xt-ide-controller/>

![](img/26d2603c15623f371787ab8c701bc413.png "homemade-XT-controller")

[Geordy]想要使用一些 IDE 设备，但是他的 XT 系统没有接口卡，不能处理 16 位 IDE。他四处寻找 8 位 ISA 控制器，但很难找到，而且相当昂贵。幸运的是，有一个开源项目可以解决这个问题。[XTIDE 项目](http://wiki.vintage-computer.com/index.php/XTIDE_project)集合了一群复古计算爱好者设计了这款 ISA 卡。[Geordy]甚至能够从一个论坛成员那里订购专业 PCB。他[订购零件并焊接在一起](http://www.notanon.com/electronics/how-to-build-an-8-bit-ide-controller-for-a-pc-xt/2010/07/30/)，总共花费约 30 美元。他让一个朋友帮他将代码烧录到 EEPROM 中，但这很简单，用 Arduino 、[总线盗版](http://hackaday.com/2009/06/30/parts-spi-eeprom-25aa25lc/)或其他几种方法中的一种就可以完成[。现在他安装 DOS 6.22 的宏伟计划已经实现了。](http://hackaday.com/2010/06/14/unbricking-with-the-help-of-arduino/)
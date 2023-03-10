# 微控制器上的 Python

> 原文：<https://hackaday.com/2011/09/26/python-on-a-microcontroller/>

![](img/3c3161e1e91aba356fae01092557f9bb.png "python")

LeafLabs 的团队正在为他们的新 ARM 开发板寻找一些很酷的东西。[AJ]问是否有人玩过 Python，于是[Dave]编写了一个 [PyMite 的实现，并把它放在一个枫木板上](http://leaflabs.com/2011/09/pymite/)。虽然写的只是用微控制器闪烁 LED，但他们是在运行时用 Python 交互式地完成的。

构建使用团队正在开发的 [Maple Native](http://leaflabs.com/devices/#Maple-Native) 板。该板有一个 32 位 ARM 芯片和 1 兆 RAM——足够运行 [PyMite](http://wiki.python.org/moin/PyMite) 的马力。将 PyMite 放在枫树[上的教程在 LeafLabs wiki](http://wiki.leaflabs.com/index.php?title=PyMite) 上。

PyMite 理论上能够控制 Maple Native 上的每一个引脚，并且能够做普通 Python 发行版所能做的一切事情。LeafLabs 团队仍在为他们的主板开发必要的库(尽管我们在 [Google code](http://code.google.com/p/python-on-a-chip/) 页面上看不到任何东西)，所以现在只支持闪烁 LED。尽管如此，把 Python 放在口袋里还是很酷的。
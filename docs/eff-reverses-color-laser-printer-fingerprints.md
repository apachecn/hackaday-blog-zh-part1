# EFF 反转彩色激光打印机指纹

> 原文：<https://hackaday.com/2005/10/17/eff-reverses-color-laser-printer-fingerprints/>

![blue led](img/56a3d6128c326eeac2e8ed69781149cc.png)

EFF[破解了 Xerox DocuColor](http://www.eff.org/Privacy/printers/docucolor/) 的跟踪代码。DocuColor 在每一页上打印一个模糊的 15×8 黄色网格点。要看到这些点，你需要一个放大镜。你也可以用蓝光使这些点呈现黑色。EFF 页有一个内置的应用程序，用于解码隐藏时间、日期和打印机序列号的点。EFF 还维护了一个[列表，列出了具有或不具有此“功能”的打印机](http://www.eff.org/Privacy/printers/list.php)。

Andrew“bunnie”Huang 在这项研究中帮了大忙。为了加快对提交的打印机样本的分析，他[改装了一台扫描仪，使用蓝光](http://www.bunniestudios.com/wordpress/?page_id=51)。扫描仪会在每次页面扫描前进行白平衡校准，因此在此期间需要关闭蓝光，否则扫描仪会进行补偿。邦尼还[打开他的 HP 2600N](http://www.bunniestudios.com/wordpress/?p=53) 来确定水印是在哪里实现的。通过研究电路板，他认为大多数彩色激光打印机可能都在使用佳能引擎板。通过胁迫一家制造商，政府能够在大多数售出的激光打印机中添加水印。

[via [BoingBoing](http://www.boingboing.net/2005/10/17/eff_cracks_hidden_sn.html)

*   [永久链接](http://www.eff.org/Privacy/printers/docucolor/)
# 通过 SATA 固态硬盘转换加快 ThinkPad X41 的速度

> 原文：<https://hackaday.com/2011/02/22/speeding-up-a-thinkpad-x41-via-a-sata-ssd-conversion/>

![](img/bda54b9032b2bdd025acbab34b19d987.png "thinkpad-ssd-upgrade")

[Marek Walther]每天使用 ThinkPad x41 平板电脑办公。由于他带着设备四处奔波，他认为硬件故障最终会发生，考虑到这一点，他购买了第二台设备——略有损坏——作为备用。他从未对平板电脑的速度感到兴奋，所以他开始寻找改进之处。其中一个选择是[用固态硬盘](http://wiki.marek-walther.de/wiki/projekte/pimpmeup/thinkpad_x41_hdd_upgrade_sata) ( [翻译](http://translate.google.com/translate?js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&sl=auto&tl=en&u=http://wiki.marek-walther.de/wiki/projekte/pimpmeup/thinkpad_x41_hdd_upgrade_sata))取代传统硬盘。但是简单地放入固态硬盘不会让事情变得更快。这是因为股票驱动器使用 PATA 接口。经过一番窥探后，[Marek]发现主板有一个 SATA 接口，该接口有一个桥连接到 PATA 插头。通过移除桥接器并将 SATA 电缆焊接到电路板上，他能够在提高性能的同时增加存储容量。
# VCI-100 转盘控制器的自制固件升级

> 原文：<https://hackaday.com/2010/09/20/homebrew-firmware-upgrade-for-vci-100-turntable-controller/>

![](img/5ce7bc8802e69eec2026da657a2e90f8.png "vci100main-firmware-updating")

我们喜欢把高质量的产品做得更好的黑客。VCI-100 的这个[增强固件就是一个很好的例子。以类似于](http://www.djtechtools.com/2010/09/19/brand-new-vci-100-firmware-1-4-hd-updat/)[百灵达黑客](http://hackaday.com/2010/09/02/firmware-hacking-on-behringer-midi-devices/)，【戴维】，[的方式，对设备的固件](http://www.djtechtools.com/forum/showthread.php?t=17022)进行逆向工程，并找出了一些改进的方法。它提高了刮擦控制器和滑块的精度，使用 ADC 读数的 9 位精度，在股票版本中被向下移动到 7 位。还有一些他们称之为迪斯科模式的 LED 小把戏。他们正在出售一种“芯片”,你需要用它来刷新固件，但从我们所看到的来看，它只是一个 RS232 转换器，所以你也许能够知道没有这部分如何工作。休息之后，我们嵌入了固件版本 1.4 的演示。

[https://www.youtube.com/embed/cjDQmEkWBw4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/cjDQmEkWBw4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢史蒂夫]
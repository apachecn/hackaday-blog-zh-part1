# 预旋转硬盘

> 原文：<https://hackaday.com/2010/02/05/pre-spun-hard-drives/>

![](img/a48c402610b875f79ed07512909d07b7.png "spinmaster")

这个装置被亲切地称为自旋控制仪。[Linux-works]建立它是为了在主板启动之前旋转多个硬盘驱动器。它检测来自 PSU 的加电，并使用继电器将主板保持在复位状态，由红色 LED 指示。四个继电器中的每一个都会旋转硬盘，并在准备就绪时点亮绿色 LED。一旦所有绿灯亮起，复位继电器关闭，bios 启动。这种类型的交错启动为动力不足的 PSU 减轻了很多负担。他的[发布了固件](http://www.netstuff.org/spinmaster/)，还有[的原理图](http://www.flickr.com/photos/linux-works/4324470636/)也可以使用。我们看了看他的视频，但没有太多东西可看，因为它只是机器启动时的内部。
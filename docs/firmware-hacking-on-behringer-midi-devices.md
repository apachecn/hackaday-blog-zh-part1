# 百灵达 Midi 设备上的固件入侵

> 原文：<https://hackaday.com/2010/09/02/firmware-hacking-on-behringer-midi-devices/>

![](img/e6abcf0676556a7a6d026ea015b6308c.png "bcr2000-firmware-hacking")

一个名为[的非官方百灵达控制开发套件](http://willem.engen.nl/projects/bc2000-dev/)的新项目让你调整或完全替换流行设备上的固件。概念验证演示显示了在 4 字符 7 段显示屏上滚动的自定义消息，但您可以使用该设备做的事情只受到您可以为内部的 ARM 处理器编写代码的程度的限制。使用 [GNU ARM 工具链](http://www.gnuarm.com/)进行开发，但是不要担心，你不必打开外壳来编程芯片。该项目支持的 BCR2000 和 BCF2000 型号都运行引导加载程序，允许通过 midi 命令更新固件。如果你把事情搞砸了，甚至还有恢复模式。只要确保您有一个直接的 midi 连接用于恢复，USB 端口不会为此而工作。如果你需要一个推力来让你开始，在资源库中有一个很好的小示例文件[。](http://bazaar.launchpad.net/~bc2000-dev/bc2000-dev/trunk/annotate/head:/README.firmware)

[谢谢比约恩]
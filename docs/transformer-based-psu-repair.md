# 基于变压器的 PSU 修复

> 原文：<https://hackaday.com/2011/09/13/transformer-based-psu-repair/>

![](img/8a66ec1cacb24dbd5cf07aedbf895b32.png "OLYMPUS DIGITAL CAMERA")

修复别人的设计错误比从头开始要难得多。因此，每当我们遇到擅长这类故障排除的人时，我们都会给予关注。[吉姆]家里有一辆桑吉安 HDR-1。这是一个桌面高清收音机，由于某种原因停止供电。他把它敲开，问题就迎刃而解了。

首先要做的是拆卸，这对于这种型号来说并不太难。手里拿着万用表，他开始探测变压器，发现初级线圈的触点是开路；发出问题信号。没有内嵌保险丝进行保护，对次级绕组的进一步研究让他发现了 1N5817 二极管的用途。这些都是这个特殊的变压器被低估的部分。他用 1N4003 二极管取代了它们，使设备符合规格。但是仍然存在保险丝保护的问题。一点电路自由成型允许他添加一个保险丝和变阻器直接焊接到变压器的触点。

为什么停在那里？在[Jim]打开箱子的同时，他还换出了低端运算放大器和几个电解电容，以改善收音机的音质。运算放大器的替代似乎是改善高清收音机声音的一种流行方式。
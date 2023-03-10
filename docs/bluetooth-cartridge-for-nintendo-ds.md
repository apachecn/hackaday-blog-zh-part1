# 任天堂 DS 的蓝牙盒

> 原文：<https://hackaday.com/2009/10/21/bluetooth-cartridge-for-nintendo-ds/>

![bluetooth-cartridge-nintendo-ds](img/403009cc69f7776f7f0f630bf8c1d101.png "bluetooth-cartridge-nintendo-ds")

我们已经从一些不同的人那里收到了关于新的[蓝牙模块的提示，该模块可以作为任天堂 DS](http://dsbrut.sukzessiv.net/site/bluetooth) 的游戏模块进行连接。这是一个自制的解决方案，而不是一个官方的任天堂插件。该盒包含一个 ATmega168 微控制器，该微控制器提供 DS 和一个[漫游网络 RN-41 蓝牙模块](http://www.rovingnetworks.com/rn-41.php)之间的接口。

他们已经[提供了该设备的原理图](http://dsbrut.sukzessiv.net/files/schematics/ds_bluetooth_rev_b.png)，但是我们没有看到任何电路板插图或内部图片，因此您需要自行设计电路板布局。将蓝牙连接用于自制软件所需的库可供下载。这应该提供了一个很好的方式来使用蓝牙 GPS 模块的 DS，或者作为一个离散的蓝牙嗅探器和欺骗器。
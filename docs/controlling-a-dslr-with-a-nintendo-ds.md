# 用任天堂 DS 控制 DSLR

> 原文：<https://hackaday.com/2012/03/13/controlling-a-dslr-with-a-nintendo-ds/>

![](img/f2850dd45cf9872c3f12a53bbfdcbaed.png "camera")

在 Hack a Day，我们已经看到了几十个远程打开和关闭相机快门的 intervalometer 构建。[卢克·斯卡夫]决定通过用任天堂 ds 自动控制相机的焦距和快门来将这些构建提升到一个新的水平。

[Luke]的构建基于[开放式相机控制器项目](http://www.hdrlabs.com/occ/),该项目将音程计、声音触发器、音序器和 HDR 支架拍摄的能力交给了专业摄影师。开放式相机控制器是为了在任天堂 DS 上运行而构建的，该游戏机带有一个连接到 Game Boy Advance 墨盒端口的 [AVR 卡](http://www.hdrlabs.com/occ/hardware.html)。

开放式相机控制器连接到相机的快门端口，但[卢克]通过使用[USB 主机控制器](http://www.ftdichip.com/Products/ICs/VNC1L.htm)和实现[图片传输协议](http://en.wikipedia.org/wiki/Picture_Transfer_Protocol)来加快速度。现在，不再是[卢克]的控制器告诉他的相机何时打开和关闭快门，相机的焦距也可以调整。[Luke]的构建使用 Xilinx CoolRunner-II CPLD 和 [USB 主机控制器](http://www.ftdichip.com/Products/ICs/VNC1L.htm)将 DS cartridge 端口转换为每个 DSLR 都可以连接的 USB 端口。

[卢克]他手上仍然有一堆乱七八糟的电线，但即使是我们也能看到廉价的自动化将给数码摄影世界带来的力量。

[https://www.youtube.com/embed/aGAHeJVDePk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aGAHeJVDePk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# Bitbang IR Remote

> 原文：<https://hackaday.com/2011/03/11/bitbang-ir-remote/>

![](img/01a3b29dae0652b24da82f95b68a96f4.png "hw_ftdi.geschaald")

[Albert]使用传统的 RS232 串行连接制作了一些 PC 红外发射器和接收器，这很好，但正如我们所知，并不是每台计算机都有标准的串行端口。通过普通 USB <> RS232 加密狗的搜索不符合他的要求。他决定自己动手，于是他发明了这个 [FTDI bit-bang IR 接收器/发射器](http://www.huitsing.nl/irftdi/)。

虽然 FTDI 制造了一系列芯片，但大多数(如果不是全部)支持 bit-bang 模式，在这种模式下，您可以手动控制 IC 的引脚。FTDI 芯片处理定时，当与 [libFTDI](http://www.intra2net.com/en/developer/libftdi/) 配对时，控制起来相当轻松。该软件正在开发中，但[艾伯特]已经有了一个连接到[LIRC](http://www.lirc.org/)的驱动程序，它可以让你控制一系列远程设备和一个载波生成测试程序。

在他的网站上可以找到原理图、源代码和几页有用的信息。
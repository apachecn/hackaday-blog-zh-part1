# 英特尔 Mac Mini 上的 Xen

> 原文：<https://hackaday.com/2006/08/13/xen-on-intel-mac-mini/>

![mac mini](img/755b63b3a4ec934921176d4a264d4c36.png)

可扩展计算实验室发布了关于如何让 Xen 在英特尔 Mac mini 上运行的说明。 [Xen](http://www.cl.cam.ac.uk/Research/SRG/netos/xen/) 是一个开源的虚拟化系统，允许多个客户操作系统在同一个处理器上运行。Mac mini 很小，相对便宜，而且因为它支持 VT 指令，你可以不加修改地运行 WindowsXP。这使得 mini 成为硬件虚拟化设备的绝佳选择。安装确实有一些怪癖。你需要一个使用 lilo 引导的发行版，因为 Mac mini 没有 A20 门。一旦安装完毕，你将切换到 grub 的补丁版本，因为这是 Xen 所需要的。

[感谢史蒂夫，好史蒂夫]

*   [永久链接](http://www.scl.ameslab.gov/Projects/mini-xen/index.html)
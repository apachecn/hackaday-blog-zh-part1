# 用于在系统编程的 USB 集线器

> 原文：<https://hackaday.com/2010/06/07/usb-hub-used-for-in-system-programming/>

![](img/661f5dace692c568d88bf193db08d259.png "usb-hub-ISP")

你订购 4 端口 USB 集线器是因为它几乎是免费的，但现在它只是坐在你的垃圾箱里吗？为什么不[把它变成 AVR 芯片](http://www.pjrc.com/hub_isp/)的在系统编程器？[保罗]想出了 HUB ISP 作为我们在[和其他 diy 程序员](http://hackaday.com/2010/06/03/usbasp-avr-programmer-based-on-atmega8/)身上看到的先有鸡还是先有蛋的问题的答案。它使用来自四种不同 USB 电缆的数据线对 AVR 芯片进行编程，并在此过程中获得了 74HC00 与非门的帮助。你不需要一个编程的微控制器，因为所有的魔法都发生在软件方面。一个警告是[Paul 的]方法目前只在 Linux 机器上有效。
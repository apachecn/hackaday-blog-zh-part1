# 小型试验板上的 AVR HVSP

> 原文：<https://hackaday.com/2011/04/06/avr-hvsp-on-a-tiny-breadboard/>

![](img/9083f610255fe96357d22c19053beb77.png "avr-hvsp-on-breadboard")

AVR 芯片很方便，因为你可以在它们的工作电压下对它们进行电路编程。也就是说，除非你把保险丝的设置搞砸了，他们就不会再听系统内的程序员的话了。如果你发现自己面临这个问题，只需在试验板上构建这个电路，然后按住按钮就可以“解开”了。

上面的电路是一个高压串行编程器。这是 AVR 芯片使用的两种高压协议之一；HVSP 适用于没有足够引脚来使用高电压并行编程的芯片。这种再现使用 12V 电源，这是高电压方法所必需的电平。一个 7805 线性调节器与一个晶体管、一个用于控制电路的 ATtiny2313、一个用于反馈的 4 位 7 段显示器和一个用于控制的按钮一起加入 mix 以提供工作电压。

休息后观看视频，看到 ATtiny13 使用试验板编程器编程禁用 reset 引脚[。然后，该芯片很容易被挽救，已经通过使用其设备签名被自动识别。](http://hackaday.com/2010/12/14/make-your-own-minimalist-avr-isp/)

[https://www.youtube.com/embed/rHaswi-OYXo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/rHaswi-OYXo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
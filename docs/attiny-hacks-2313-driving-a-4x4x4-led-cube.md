# ATtiny Hacks: 2313 驾驶 4x4x4 LED 立方体

> 原文：<https://hackaday.com/2011/09/18/attiny-hacks-2313-driving-a-4x4x4-led-cube/>

![ATtiny Hacks Theme Banner](img/5f674cf2d4b94faba5f6b413d805f657.png "ATtiny Hacks Theme Banner")


[Kirill]写来分享他的 ATtiny hack，[一个 4x4x LED 立方体](http://img600.imageshack.us/img600/4691/444ledcube.png)。64 LED 显示屏是一个很好的选择，可以充分利用他选择的硬件。是按等级复用的。四级中的每一级都与公共阴极相连，由 2N3904 晶体管开关。阳极由两个 595 移位寄存器驱动，总共提供 16 个可寻址引脚，与 4×4 栅极完美匹配。总而言之，只需要 ATtiny2313 的七个引脚来驱动显示器。这比 ATtiny85 等更小的芯片多了一个引脚。但是，这种芯片确实包括一个 UART，这意味着该项目可能会被修改，以接收来自计算机或其他设备的动画指令。

你可能已经注意到了上图中的 USB 端口。这是作为调节电源的来源，而不是拥有自己的电压调节硬件，并且根本不用于数据。休息后观看视频，了解[Kirill]在显示屏上使用的动画。您也可以在那里找到源代码的链接。

[https://www.youtube.com/embed/d4na-kO2q1Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/d4na-kO2q1Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

这里有一个链接指向[基里尔的]源代码:[http://www.mediafire.com/?c47p92t0rl3z90p](https://www.youtube.com/redirect?q=http%3A%2F%2Fwww.mediafire.com%2F%3Fc47p92t0rl3z90p&session_token=dgYQ8D7Nh0djJklmw34vqr8uTIB8MTMxNjA5NDczOEAxMzE2MDA4MzM4 "http://www.mediafire.com/?c47p92t0rl3z90p")
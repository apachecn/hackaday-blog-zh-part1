# 诺基亚 LCD、双截棍和 MSP430 联手

> 原文：<https://hackaday.com/2011/02/02/nokia-lcd-nunchuck-and-msp430-join-forces/>

![](img/4c82435b14edb975810d3d84d5d75dfd.png "launchpad-nokia-lcd-and-nunchuck")

使用 MSP430 通过 Wii 双节棍的输入驱动诺基亚 6100 液晶显示器。他正在使用 Launchpad 附带的 G2211 微处理器，并用 MSP-GCC 开发他的代码。正如你在休息后的视频中看到的，这是可行的，但还有一些改进的空间。也就是说，他碰到了代码内存限制，只剩下大约 500 字节可以使用。LCD 屏幕是 SPI，目前它占用了用于硬件 i2c 的引脚。由于他需要 i2c 总线与双截棍通信，他不得不使用 i2c 软件，这解释了他的程序内存问题。

我们不是这方面的专家，但他似乎可以通过重写 LCD 驱动程序来重新映射引脚，从而节省空间(并提高输入响应能力)。话说回来，[升级到更大的 MSP430](http://hackaday.com/2010/09/28/launchpad-not-limited-to-value-line-chips/) 可能会更好。如果你有一些建议，一定要留下评论来分享。

[https://www.youtube.com/embed/HtVn17k08fk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HtVn17k08fk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
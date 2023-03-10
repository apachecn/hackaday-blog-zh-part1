# 解码，然后克隆一个红外直升机玩具的控制信号

> 原文：<https://hackaday.com/2012/03/23/decoding-then-cloning-an-ir-helicopter-toys-control-signals/>

![](img/aa4f4d02ec93b07d0675cd8d9bcc71b5.png "ir-controlled-fpga-heli")

[迈克·菲尔德]得到这架司马 S107 直升机的目的是要黑掉它。在摆弄了一会儿之后，他开始着手为玩具制作自己的红外控制器。似乎有一些关于它的协议信息发表在各种论坛帖子中，但他决定自己弄清楚会更有趣。

他开始尝试用 [Adafruit 的教程捕捉红外信号，这个教程在其他一些项目中派上了用场](http://hackaday.com/2011/09/29/remote-controlled-usb-switch/)。他可以让他的电视遥控器注册，但不是玩具的控制器。这并没有停止乐趣，相反，他撕开控制器，抓起一个逻辑嗅探器，看看是什么被推到红外发光二极管。信号有点奇怪。似乎每个命令都发送了两个不同的数据包，而[Mike]认为这是用于两种不同型号的玩具。除此之外，帧是不同步的。但是一点 10 MHz 的采样帮助他搞清楚了一切，他相信他得到了一个比以前发现的更精确的协议版本。为了证明这一点，他使用 VHDL 开发了一个基于 FPGA 的控制器，并在休息后的视频中展示了这个控制器。

[https://www.youtube.com/embed/89HvwYWg838?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/89HvwYWg838?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
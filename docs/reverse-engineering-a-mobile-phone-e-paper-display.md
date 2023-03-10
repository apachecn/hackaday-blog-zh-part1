# 手机电子纸显示屏的逆向工程

> 原文：<https://hackaday.com/2011/02/24/reverse-engineering-a-mobile-phone-e-paper-display/>

![msp430_epaper_display](img/689ebfe33c9ace466dfc59083da7abe7.png "msp430_epaper_display")

虽然电子纸在电子阅读器中很常见，但除了 MOTOFONE 之外，很少有手机专门使用电子纸显示屏。[史蒂夫]有一部这样的手机，他认为可以用它来制作一个低功耗的时钟。因为双稳态电子纸显示器即使在断电时也能保持当前活动的内容，所以当时间改变时，他只需要每分钟更新一次时钟。

不幸的是，对于摩托罗拉使用的显示控制器，公开可用的文档非常少。为了了解显示器是如何驱动的，他必须嗅探处理器和显示器之间的 SPI 通信。一旦他记下了基本的命令，他就花了相当多的时间来弄清楚如何激活显示器的不同部分，这似乎是摩托罗拉方面仓促的设计过程。

既然[史蒂夫]已经对几乎所有东西进行了逆向工程，他将手机连接到 TI MSP430 来驱动显示器。他将 LaunchPad 编程为一个基本时钟，效果非常好，正如你在下面的视频中看到的。

如果你对电子纸黑客的兴趣被激起，一定要看看我们以前的电子纸报道[这里](http://hackaday.com/2008/10/14/how-to-make-an-e-paper-clock-and-hack-esquire-magazine/)。

[https://www.youtube.com/embed/HZdV2iKakqA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HZdV2iKakqA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
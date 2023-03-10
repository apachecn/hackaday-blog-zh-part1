# 艰难地将 RS232 添加到万用表

> 原文：<https://hackaday.com/2011/11/12/adding-rs232-to-a-multimeter-the-hard-way/>

![](img/17d61904632d3a041161e61337b6dca8.png "adding-rs232-to-a-multimeter")

您可能希望存储万用表的信息，以便随时间绘制图表。几乎所有的高端专业型号都有这个。但是如果你买一个超级便宜的仪表，你可以打赌这不是一个选项。[Jazzzzzz]找到了一种通过 RS232 从 4 美元的电表中获取数据的方法。这不是不可能的，但我们肯定认为他在用强硬的手段。那是因为他不仅仅是[挖掘了一个潜在的特性](http://hackaday.com/2010/11/30/unlocking-rs232-serial-comm-on-a-multimeter/)。他实际上添加了一个微控制器来采样数据，并通过 RS232 协议推送数据。

从好的方面来看，这比从头开始制造万用表要容易得多。采样电路仍在使用，PIC 16F688 在信号进入股票微控制器时拦截信号。他所追求的信号只在一个引脚上进入芯片，但为了在 PIC 上获得正确的读数，他必须使用运算放大器。这只是难题的一部分，因为他还需要一种方法来判断选择开关设置在什么位置。最后加上一个电位器，读取它的值，让他计算出位置。

[谢谢卡尔]
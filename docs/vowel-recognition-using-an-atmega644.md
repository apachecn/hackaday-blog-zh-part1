# 使用 ATmega644 进行元音识别

> 原文：<https://hackaday.com/2011/08/27/vowel-recognition-using-an-atmega644/>

![](img/78664f838e3b6e5d80f35a19a8a62a19.png "atmega644-vowel-recognition")

[张友春]和[Annie (Wei) Dai]找到了一种使用 atmega 644 区分元音的方法，作为他们的微控制器设计课程的最终项目。语音识别并不常见，但大多数时候它使用计算机、智能手机或专门设计的硬件。该实现使用 ATmega644、通过运算放大器连接的麦克风和几个按钮。在休息后的演示中，您将看到他们通过 RS232 连接向 Putty 输出状态数据，但这只是为了让您可以看到芯片内部的情况。这是做所有艰苦工作的原因。

为了区分元音之间的差异，在研究阶段使用 MATLAB 分析了每个声音的波形。这种分析使研究小组能够收集每种声音的数据，这些数据包含了在其他声音中最少出现的峰值。现在，微控制器分析传入的声音，并将其与数据集进行比较。由于团队使用了[快速沃尔什变换](http://en.wikipedia.org/wiki/Fast_Walsh_transform)，分析变得快速、实时。它将声音转换成一组方波，并以 64 位样本的形式呈现出来。结果可以用作密码保护方案，但据我们所知，这不只是一个人的密钥，任何知道密码元音的人都可以使用它。

[https://www.youtube.com/embed/YLE5DEedxaY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YLE5DEedxaY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
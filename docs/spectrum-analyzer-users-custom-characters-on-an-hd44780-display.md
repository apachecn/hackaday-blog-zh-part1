# 频谱分析仪用户在 HD44780 显示器上自定义字符

> 原文：<https://hackaday.com/2011/09/08/spectrum-analyzer-users-custom-characters-on-an-hd44780-display/>

![](img/bbfedd32865314666bc7eae28aded204.png "hd44780-spectrum-analyzer")

[卡米洛]建造了一个频谱分析仪，和他的音频系统一起使用([翻译](http://translate.google.com/translate?sl=auto&tl=en&js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&u=http%3A%2F%2Fcandelectronica.blogspot.com%2F2011%2F09%2Fanalizador-de-espectro-de-audio-con-lcd.html))。硬件非常简单，使用运算放大器、微控制器和 LCD 显示器。他选择了 LMV324M 低压运算放大器，该放大器连接到输入音频信号，并将其输出馈入微控制器的 ADC。在这种情况下，他选择了 HCS08 系列的 Freescale 微控制器，其工作频率为 20 MHz。这使项目有足够的速度来正确分析传入的音频。他提到他遵循了[奈奎斯特-香农采样定理](http://en.wikipedia.org/wiki/Nyquist%E2%80%93Shannon_sampling_theorem)中提出的指导方针，并在处理样本时使用了[快速傅立叶变换](http://en.wikipedia.org/wiki/Fast_Fourier_transform)。

这不是我们第一次看到字符 LCD 被用作频率分析仪的显示器。另一个基于 ATmega8 的再现支持几种不同的屏幕布局。这些显示器有足够的内存来存储八个自定义字符。每个字符为 5×8 像素，每个字符有 8 个级别，上面看到的每列共有 16 个级别。我们喜欢项目中硬件的简单性，但我们不介意看到一个额外的电位计来微调数据在屏幕上的显示方式，以利用其全部范围。休息后，在剪辑中查看项目的运行情况。

[https://www.youtube.com/embed/dm2jUzTKCWc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dm2jUzTKCWc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# DIY 声音定位传感器

> 原文：<https://hackaday.com/2011/05/10/diy-sound-localization-sensor/>

![sound_localization_sensor](img/99cab0c8496e5ff15d630abf10200723.png "sound_localization_sensor")

声音定位在执法界非常受欢迎，因为其准确性和快速将枪声与其他类似噪音分开的能力。这些系统并不便宜，[在尝试自己建造一个之后，【Fileark】知道为什么](http://filear.com/index.php/arduino/90-diy-sound-localization-sensor)。

他认为基于人耳如何确定声音的来源来构建声音定位传感器是一件很棒的事情。然而，一旦他开始工作，他就意识到做好本地化工作是多么困难。

他使用 LM324N 运算放大器作为音量比较器，他说这已经足够好了，尽管他认为还有 IC 可以做得更好。[Fileark]报告称，当声源距离传感器约一英尺时，声音检测器工作良好，但距离越远，性能越差。如果他制作第二个版本，他可能会考虑使用 ARM Cortex-M3 作为他的声音处理器，因为他使用的 Arudino 没有足够的能力在他要求的 10-50 微秒窗口内采样和运行计算。

请继续阅读，观看他的声音定位传感器的视频。

[https://www.youtube.com/embed/yHyuzKRZFUY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yHyuzKRZFUY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
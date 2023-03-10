# Pidato Box 为数码钢琴增加了颤音效果

> 原文：<https://hackaday.com/2011/04/16/pidato-box-adds-vibrato-effect-to-digital-pianos/>

![piano_vibrato_box](img/ecdda954a470c5c717aed0024d5ffce7.png "piano_vibrato_box")

[Joren]喜欢他的数码钢琴，但它缺少一个他想使用的关键部件:在演奏时产生颤音的能力。颤音可以在普通钢琴上以几种不同的方式实现，但在设计数码钢琴时，似乎没有太多考虑这种效果。

他喜欢演奏各种各样的音乐，包括来自弗朗茨·李斯特的独奏，其中建议有时使用颤音，所以[他决定为自己建造一个颤音盒](http://0110.be/artikels/lees/The_Pidato_Experiment%253A_Vibrato_on_a_Digital_Piano_Using_an_Arduino)。在 [Hackerspace Ghent](http://0x20.be/) 的友好人士的一点帮助下，他的“Pidato”集成了一个 Arduino 和三轴加速度计来完成工作。

Arduino 连接到钢琴的 MIDI 输出以及他安装在手腕上的加速度计。演奏时，他需要做的只是快速移动他的手来产生颤音，正如你在下面的视频中看到的那样。Arduino 代码过滤掉任何其他种类的移动，以确保他不会在不希望的时候意外触发效果。

查看下面的视频，快速演示 Pidato 盒子。

[https://www.youtube.com/embed/phDV_qioBMU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/phDV_qioBMU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# Chipophone 播放视频游戏经典

> 原文：<https://hackaday.com/2010/07/22/chipophone-plays-video-game-classics/>

这个旧货店风琴作为一个 8 位音乐制作人获得了新生。这款手机名为 chip ophone T1，它依靠 ATmega88 来产生声音，你可能会联想到经典的视频游戏。[Linus Akesson]在休息之后带我们浏览视频中所有不同的声音设置，包括您最喜欢的主题音乐的表演。

最初的风琴使用晶体管逻辑，这使得它很容易接入硬件。感谢[构建日志](http://www.linusakesson.net/chipophone/making.php)，我们知道【Linus】使用 74HC165 输入锁存器来监控 120 个输入的每个开关。其中 15 个锁存器像反向移位寄存器 74HC595 一样工作，将所有并行输入级联成一个串行信号。从那里微控制器接管，监测按键，踏板，开关和电位计，并输出适当的声音。

[https://www.youtube.com/embed/m1pchpDD5EU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/m1pchpDD5EU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[感谢 7e]
# Arduino 小行星

> 原文：<https://hackaday.com/2011/02/08/arduino-asteroids/>

![](img/2865fde0abb3718f3abe5ef3092690d8.png "Screenshot-9")

[nootropic]为 hackvision 出了一款新游戏，[“小行星”](http://nootropicdesign.com/projectlab/2011/02/06/asteroids-on-hackvision/)！当 [hackvision](http://hackaday.com/2010/10/24/hackvision-is-build-your-own-retro-game/) 在 2010 年 10 月首次出现时，我们报道过它，从硬件角度来看，它没有改变。它仍然是一个 Arduino(软件)兼容系统，配备 atmega328，视频和音频输出连接([使用电视输出库](http://www.arduino.cc/playground/Main/TVout))，所有这些都在一个漂亮的印刷电路板上，带有按钮，类似于一个游戏控制器。

虽然在使用 Arduino 和一个库的情况下运行类似 [space invaders、pong 和 tetris](http://nootropicdesign.com/hackvision/games.html) 的街机游戏已经足够令人印象深刻，但 Asteroids 将游戏提升了一个档次。

使 Asteroids 变得更好的特性是，Asteroids 包括一个 TV-out 库的 mod，这样位图可以在不擦除它们下面的像素的情况下彼此飞过，以提供旧的时间向量拱廊感觉，以及“[多边形中的点](http://en.wikipedia.org/wiki/Point_in_polygon)”风格的碰撞检测，这是一种针对不规则形状、受限平台或不受限平台的奇妙/有效的碰撞检测方式。

最后但并非最不重要的是，[nootropic]在声音设计中使用了电视输出库的 set_vbi_hook()函数，从简单的“哔哔声”和“boops”到持续 60Hz 刷新的“哔哔声”和“boops”(在 NTSC 的情况下)，这使他能够构建更复杂的声音效果，提供爆炸和激光爆炸的美妙拱廊声音。

休息后加入我们，观看一个快速视频，记住，这是基于 Arduino 的，所以如果你已经有一个 Arduino，你可以添加支持硬件(按钮，电阻和 RCA 插孔)并运行当前提供的任何游戏，或者制作你自己的游戏。

[https://www.youtube.com/embed/w03dO0Hd660?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w03dO0Hd660?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
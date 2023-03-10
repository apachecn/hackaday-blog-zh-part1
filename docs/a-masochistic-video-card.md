# 受虐视频卡

> 原文：<https://hackaday.com/2011/10/06/a-masochistic-video-card/>

![](img/ae7dd26bb2652ff2f34f4372efba113f.png "videocard")

对疼痛有嗜好？为什么不用一个绕线工具来破坏你的指尖，来制作一个完全由分立元件组成的显卡呢？

当[克里斯]决定为危险的原型制作一个参赛作品时，他已经忙得不可开交了。他手头的 74xx 芯片的最大时钟频率为 25MHz，但 VGA 像素时钟的运行频率为 40MHz。[将 H 同步时序除以 4](http://www.pyroelectro.com/projects/masochists_video_card/sync_theory.html) 意味着显卡所需的最高速度仅为 10MHz，尽管分辨率有所降低。

视频卡构建在带有绕线插座的 perfboard 上。包括一个 8 位 DAC，允许该卡显示 256 种不同的颜色，但只有三条主要线路连接到 VGA 电缆。就像这样，卡片在一个恒定的循环中循环通过 8 种不同的颜色，对于一堆筹码来说还不错。

VGA 输出已经在从[手臂](http://hackaday.com/2011/06/02/vga-out-on-a-maple-board/)到 [ATtiny](http://hackaday.com/2011/08/31/vga-video-output-with-an-attiny/) 的所有东西上完成，但是很少在分立元件上完成 VGA 输出。虽然这个显卡可能不是我们比特币挖矿的首选，但它仍然是一个非常令人印象深刻的构建。休息之后，请观看视频演示。

[https://www.youtube.com/embed/mIgU32ny3pQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mIgU32ny3pQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
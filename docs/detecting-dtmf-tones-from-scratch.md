# 从头开始检测 DTMF 音调

> 原文：<https://hackaday.com/2011/10/20/detecting-dtmf-tones-from-scratch/>

如果你想知道如何最好地从电话线上检测拨号音和 DTMF 音。

[Debraj]使用 [Goertzel 算法](http://www.eetimes.com/design/embedded/4024443/The-Goertzel-Algorithm)构建了一个 DTMF 检测器。通常，当我们考虑检测音调时，我们会从我们的锦囊妙计中取出 [FFT](http://en.wikipedia.org/wiki/Fast_Fourier_transform) 。Goertzel 算法不像 FFT 那样计算复杂，甚至可以在最小的微控制器上实现。

对于构建，首先要焊接的是一个不错的音频变压器和一些保护二极管。电话线路的铃声从+35 V 到-35 V，比微控制器能处理的略高。PIC18F4520 开发板被用作系统的大脑，所有的[代码](https://sites.google.com/site/hobbydebraj/home/goertzel-algorithm-dtmf-detection/18F4520_Goertzel.zip?attredirects=0&d=1)都可以在[Debraj]的网站上获得。

尽管 Goertzel 算法的实现有点不常见，但是[Debraj]已经看到了一些使用这种技术的有趣项目。例如，只需对代码做一些修改，就可以很容易地将[Debraj]的版本修改成吉他调音器。

这个项目是作为一个家庭自动化系统的命令和控制而建造的，从休息后的视频中，我们迫不及待地看到[Debraj]对这句话感到恼火，“*要打开厨房的灯，请按 1……”*

[https://www.youtube.com/embed/xr_V1AEROMI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xr_V1AEROMI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
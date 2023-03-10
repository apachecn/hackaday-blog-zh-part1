# Arduino 视频采样器

> 原文：<https://hackaday.com/2011/07/15/arduino-video-sampler/>

![](img/3ac4b34a0ff5a72d223489641ee4c3d2.png "videosynth")

[gijs]送来了他一直在做的 Arduino 视频采样器。采样器能够捕捉，暂停和播放一个短视频向前和向后。

视频采集电路基于[益智设计视频实验器](http://nootropicdesign.com/ve/)。我们见过[的几个项目](http://hackaday.com/2011/06/07/capturing-video-with-an-arduino/)使用这种视频实验板，但从来没有用这样的[流畅视频](http://vimeo.com/26442419)。采样器以 128×96 的分辨率对帧进行采样，并将所有数据存储在 256Kbit 的 SRAM 中。一个粗略的计算告诉我们，采样器可以保存不到一秒的视频，足以做一些很酷的事情。

[gijs]说他的视频采样器有 1 位版本和 1.5 位版本。当我们忙于思考半位是什么的时候，他将把 1.5 位版本升级到 2 位。他还订购了一些多氯联苯，预计 10 月份会有一套。休息之后来看看演示。

[https://player.vimeo.com/video/26420870](https://player.vimeo.com/video/26420870)
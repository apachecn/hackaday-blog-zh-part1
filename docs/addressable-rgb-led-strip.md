# 可寻址 RGB LED 灯条

> 原文：<https://hackaday.com/2009/06/17/addressable-rgb-led-strip/>

![ledrgb](img/39cbd74a1f01f5c024e9c189c93cca8c.png "ledrgb")

【天气实验室】偶然发现了一个 [RGB 光带，带有可单独控制的 led](http://www.synopticlabs.com/blog/index.php/2009/06/10/addressable-rgb-led-strip/)。该试纸使用 5 伏电压，由 HL1606 控制。因为纸条很难找到，这个芯片大多是无证件的，他开纸条有困难。他无法让它工作，直到他会见了[约翰科恩]，谁以前逆向工程的串行协议。他们一起工作，为 Arduino 发布了一个[库来驱动 strip。到目前为止，该库只支持淡化每个 LED，这是唯一已知的功能。如果有更多这样的条带，构建 LED 矩阵将会容易得多。下面嵌入的是一段带子在彩虹中褪色的视频。](http://code.google.com/p/ledstrip/)

[https://www.youtube.com/embed/ydVPq7UGVZc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ydVPq7UGVZc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

【相关: [LED 环境灯条](http://hackaday.com/2008/05/30/led-ambient-light-strips/)
# 此图像包含隐藏的音轨

> 原文：<https://hackaday.com/2012/02/27/this-image-contains-a-hidden-audio-track/>

![](img/5b4042d17bd2301345f6c560ab89a1ea.png "hiding-an-mp3-in-this-picture")

这张图片包含一个你非常熟悉的隐藏音轨。嗯，以前是。我们敢打赌，当我们调整原始图像大小时，我们打乱了[Chris McKenzie] [用来在图像](http://qaa.ath.cx/PiggyPack.html)中隐藏数据的精心编码。

他使用一种叫做[隐写术](http://en.wikipedia.org/wiki/Steganography#Digital)的方法来隐藏信息。由于数字图像使用数百万种颜色，所以你可以稍微改变一下颜色数据，而肉眼实际上不会察觉到任何差异。每个像素的八个最低有效位都被替换为[Chris]隐藏的数据。由于图像使用 24 位颜色，底部八位的最大可能变化(从 0 到 255)只会导致大约 0.15%的颜色变化。这只是一个像素。在大多数情况下，变化会小得多。

他展示了他的工作，包括使用 Ruby 进行解码和编码，甚至提供了一个命令行程序，让您无需下载任何东西就可以播放音频(只要确保您已经安装了所有的依赖项)。永远不会放弃，你，放弃…

[via [Reddit](http://www.reddit.com/r/programming/comments/q75bz/hiding_things_out_in_the_open/)
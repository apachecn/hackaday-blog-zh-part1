# 熔岩灯随机数发生器

> 原文：<https://hackaday.com/2005/06/05/lava-lamp-random-number-generator/>

![lava lamp](img/46add31e8c30d96ec35c562e46693f48.png)

那个标题真的有误导性；这个黑客不再需要[熔岩灯](http://www.hackaday.com/entry/3193323787821866/) …了。我最初去谷歌搜索 1996 年 SGI 的一个项目，通过拍摄熔岩灯的照片来生成随机数。熔岩灯之所以被选中，是因为它的混沌本性。我惊讶地发现 SGI 已经获得了 lavanand^(TM)技术的专利/商标。该系统要求你使用 IRIX，占用了大量的空间，而且由于专利的原因不容易实现。2000 年，最初版本背后的工程师们决定开发一个开源的替代品，名为 [LavaRnd](http://www.lavarnd.org/index.html) (注意大写的“L”和“R”)；-).这个迭代没有使用熔岩灯。它的混乱来源是带镜头盖的相机。CMOS 传感器上的增益被一路调高，以产生一个非常嘈杂的图像。然后，图像数据通过算法发送，以生成随机数。如果你想看原始项目，你必须[去问时光倒流机](http://web.archive.org/web/*/http://lavarand.sgi.com)。

*   [永久链接](http://www.lavarnd.org/index.html)
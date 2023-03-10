# G-35 圣诞灯确实是一个伟大的 LED 矩阵

> 原文：<https://hackaday.com/2011/11/07/g-35-christmas-lights-do-make-a-great-led-matrix/>

![](img/2d3e4b991cae3e8db8b523ead88483de.png "ge-color-effects-matrix")

这个完全可寻址的 RGB LED 矩阵是由[约翰·格雷厄姆·卡明斯]建造的。他没有从头开始，而是明智地重新利用了一束 GE 色彩效果灯，并[建造了一个看起来很不错的箱子，用来安装 G-35 硬件](http://blog.jgc.org/2011/11/turning-ge-color-effects-g-35-christmas.html)。

我们之前已经见过这个硬件[以类似的方式](http://hackaday.com/2011/01/11/scrolling-marquee-made-from-ge-christmas-lights/)使用。因为每个“灯泡”都有自己的微控制器，颜色数据通过串行总线输入。按照您选择的任何模式定位模块，并在软件中说明该布局。

因为这些线有 50 个灯泡，所以[John]只需剪掉末端的一个灯泡，用剩下的 49 个单元组成他的 7×7 矩阵。一个带有网格孔的方形胶合板将每个孔固定在适当的位置。电线混乱不是一个问题，因为多余的被切掉，剩下的被重新焊接在一起。[John]使用 Arduino Pro 输入数据，您可以在休息后的片段中亲自查看。

[https://www.youtube.com/embed/O97SXlcEsbE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/O97SXlcEsbE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[感谢 Evalpix]
# 555 幅漫画

> 原文：<https://hackaday.com/2011/02/22/555-cartoons/>

![](img/1ed595c3559eccbc088b05b0c12505dd.png "open")

Drehkino 是一个[转盘电影院](http://drehkino.blogspot.com/)，从特殊印刷的磁盘上播放短(50 帧)循环动画，并被安置在一个类似于唱机的木制框架中。纸盘是动画和光学旋转编码器图案的帧，该图案由从一只老老鼠身上提取的红外对拾取。该信号然后被传递到一个 555 定时器上，该定时器被配置为施密特触发器，该施密特触发器(间接地)驱动 led 频闪灯，产生与转台速度同步的动画。

这听起来很好，但是分割一个动画并计算每一帧的位置等肯定是一件很痛苦的事情，这也是由几个脚本所涵盖的。电影剪辑通过 [virtualdub](http://www.virtualdub.org/) 发送，以选择你想要的 50 帧，然后导出到单独的图像，然后由一个 sh 脚本接管， [gawk](http://www.gnu.org/software/gawk/) 用于处理数据并创建一个[ImageMagick](http://www.imagemagick.org/)(" conv script ")文件。完成脚本舞蹈后，你会得到一个带有编码器的完美间隔的轮子，可以用 PDF 格式打印在标准纸上。

软件和原理图包括在内，未来的改进已经在工作中，它很漂亮，所以值得一查。这是对旧的 [zoetrope](http://en.wikipedia.org/wiki/Zoetrope) 设计的一个有趣的改变。
# 全彩色电子书阅读器只需要 8 位的肌肉

> 原文：<https://hackaday.com/2011/10/10/full-color-ebook-reader-needs-only-8-bits-of-muscle/>

![](img/7d7337ec9b73e08b34254b3f3e40fef6.png "microtouch-ebook")

[Rossum's]仍在想办法使用他的 microtouch 硬件。这一次，他从亚马逊的公告中获得了灵感，该公告称全彩色电子书阅读器(和电影播放器)即将问世。从休息后的视频来看，[他的全功能阅读器是设备](http://rossum.posterous.com/8-bit-device-kindles-ebook-fire-an-e-reader-f)的一大胜利。

你可能对硬件很熟悉，一个基于 ATmega644 的电路板连接到一个触摸感应 LCD 屏幕。你可以自己做或者[买一个预先组装好的](http://hackaday.com/2011/01/31/update-microtouch-the-8-bit-ipod-touch/)(但是目前缺货)。该板有一个 microSD 卡插槽，可以很容易地将书籍添加到设备中。在项目开始时，[Rossum]认为他可能能够直接读取 ePub 文件，但对于 8 位处理器的限制，嵌入式图像和打开包文件所需的解压缩功能有点太多了。一个简单的步骤就能成功。在将文件传输到设备之前，可以使用助手脚本来格式化文件。这将进行解压缩，缩放图像，并将文本重新分页为适合显示大小的格式。

现在，如果我们只有一个漂亮的小盒子来装硬件，我们就可以做生意了。

[https://www.youtube.com/embed/314v1H_aN2o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/314v1H_aN2o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
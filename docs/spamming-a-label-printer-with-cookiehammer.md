# 用#cookiehammer 向标签打印机发送垃圾邮件

> 原文：<https://hackaday.com/2011/10/01/spamming-a-label-printer-with-cookiehammer/>

![](img/03438fc6ff7c2834b1edc48f4c42a8ed.png "cookiehammer")

[约翰]一直喜欢股票报价机。这些机器具有很高的收藏价值，所以除了找到一台不是 1929 年从曼哈顿摩天大楼上扔下来的机器，股票行情自动收录器对于业余爱好者来说是遥不可及的。不过，还有另一种方法可以获得类似股票行情自动收录器的设备:[黑掉一台标签打印机](http://rineysoft.com/blog/2011/09/tickertweet/)来打印 Twitter 上的内容。

建筑确实很简单。梁永能热敏标签打印机被修改以接受标准的 2.25 英寸销售点收据纸。既然打印机可以打印出一行又一行的文本，[约翰]用一个 [Twitter API](http://twitter.rubyforge.org/) ， [RMagick](http://rmagick.rubyforge.org/) 进行图形处理，用一个[梁永能打印机驱动程序](http://freelabs.com/~whitis/software/pbm2lwxl/)写了一点 Ruby 代码。

每隔 30 秒，代码就会在 Twitter 上搜索一个特定的标签，并打印这些推文。第一个想到的就是#cookiehammer ，所以就牢牢记住了。现在有一些#cookiehammer 的推文，但我们预计[John]很快就会在他的打印机里放一卷新纸。

它可能不如股票报价机信息丰富，但我们认为[约翰]的 twitter 打印机肯定比看 CNN 要好。休息之后，请仔细观看。

[https://www.youtube.com/embed/RQrhODI4PVM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RQrhODI4PVM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# 带计算机监视器的微控制器通信

> 原文：<https://hackaday.com/2011/12/22/microcontroller-comm-with-a-computer-monitor/>

[![](img/bd2fc5dbeb141617c9b9a54213c88f09.png "LOST")](http://hackaday.com/wp-content/uploads/2011/12/lost.jpg)

一天多产的黑客作者[Mike S]又在他的实验室里玩了，他想出了一个用 LCD 显示器与微控制器对话的简洁方法。[迈克]工作背后的基本理念与 20 世纪 90 年代怪异和/或酷的 [Timex Datalink](http://en.wikipedia.org/wiki/Timex_Datalink) 手表没有太大区别。

尽管有花哨的开发板，但硬件非常简单——一个光敏电阻指向计算机显示器，并使用 T2 曼切斯特编码读取比特。由于一个简单的 Javascript/HTML 页面，计算机闪烁着一系列黑白屏幕，数据(大部分)被传输到微处理器。[Mike]说他有大约 60%的时间会收到一条失败的消息，他不太确定问题出在哪里。他正在研究另一种曼彻斯特编码，这种编码使用样本而不是边缘，所以我们希望一切对他都适用。

这个版本非常相似——并且受到了启发——一篇关于带闪光灯的微控制器通信的早期文章。尽管如此，[迈克]的建设让我们想起了奇怪的未来铁人手表，我们在 97 年。休息过后，看看【迈克】的电脑/微型通讯链接演示，以及他在 [github](https://github.com/szczys/Light-Programmer) 上的代码。

[https://www.youtube.com/embed/NGbpC91oZJ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/NGbpC91oZJ4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
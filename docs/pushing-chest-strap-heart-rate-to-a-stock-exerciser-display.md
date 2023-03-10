# 将胸带心率推至健身者显示屏

> 原文：<https://hackaday.com/2011/11/26/pushing-chest-strap-heart-rate-to-a-stock-exerciser-display/>

![](img/1833f3db6383341c1eff415f1fd3ea13.png "chest-strap-data-hack")

这一招效果如此之好，以至于[Levent]希望他几年前就尝试过了。锻炼时，他戴着 Polar 心率监测器，该监测器将数据从胸带发送到手表。但是他的健身车也有一个心率读出器，它依赖于你的手触摸车把上的金属触点。他开始尝试是否能把胸带数据插入健身车的液晶显示屏。

黑客的第一部分非常简单。正如我们之前多次看到的，你可以购买[一个从胸带](http://hackaday.com/2011/09/25/arduino-heart-rate-monitor/)获取数据的接收器模块。现在的问题是把这个接收器的数据接入 Schwinn 213 卧式健身车。[Levent]拉出 PCB 并找到负责手柄心率的小子板。经过仔细研究，他能够识别出引出线。有两条数据线。一个负责心率检测信号，另一个推送实际心率数据。凭直觉，他把一个信号发生器接到后者上，发现只需要一个方波。

剩下的就很简单了。休息之后看看他视频中的证据。[https://www.youtube.com/embed/IjfmNU5yVbk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IjfmNU5yVbk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
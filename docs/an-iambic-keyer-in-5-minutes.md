# 5 分钟后一个抑扬格键盘

> 原文：<https://hackaday.com/2011/12/05/an-iambic-keyer-in-5-minutes/>

![](img/e643960b62262dae4e80c068eb3761e1.png "key")

当大多数人想到电报键时，脑海中浮现的是 19 世纪 90 年代的一件带有上下移动杠杆的科技产品。这些“直键”对电报员来说是可怕的，会导致重复性压力损伤，如腕管综合症..抑扬键出现了，把触点移到水平位置。如果你曾经看到一个火腿玩他的 CW 钻机，机会是他们正在使用一个抑扬格键。那么，很棒的是，你可以在五分钟内用你手头的零件制作出你自己的抑扬格琴键[。](http://www.jel.gr/cw-mode/iambic-keyer-with-arduino-in-5-minutes/)

[Dimitris]的构建非常简单——只有两个金属触点和一对 470K 上拉电阻。所有这些都连接到 Arduino 上的三个引脚。所有的微控制器需要做的是测量一个触摸传感器引脚在施加电压时的上升时间。如果引脚上有手指，电容会增加，上升时间会更长。之后，只需将一个传感器指定为“dit ”,另一个指定为“dah ”,就可以得到一个抑扬格键。

[Dimitris]把他项目的所有代码放在他的博客上。他的抑扬格键似乎是继微型莫尔斯训练器之后的完美项目。休息之后，请看关键时刻的视频

[https://www.youtube.com/embed/eNmSSgCqDPM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eNmSSgCqDPM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
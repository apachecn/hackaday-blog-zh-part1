# Dub 球有很多 Wub

> 原文：<https://hackaday.com/2011/10/29/ball-of-dub-has-lots-of-wub/>

![](img/c65ffcd1a403968671ee2148dee57a33.png "dub")

来自 lust lab[Lizzie]送来了她的[配音球](http://vimeo.com/30721732),它转动几个加速度计和一个数字音频工作站，把一切都变成一种 wubs 和 Dub 的听觉体验。Dub Ball 可以将任何东西转换成 dubstep，并且使用了一个相当有趣的用户界面。

“配音之球”没有构建日志，但 LustLab 的人确实提交了她的项目的基本概述。在球内，有一个来自 Sparkfun 的 [Razor IMU](http://www.sparkfun.com/products/9623) ，它连接到一直受欢迎的 XBee 无线收发器。Arduino 上的一个小程序校准陀螺仪和加速度计，并以 50Hz 的频率将数据发送给 DAW。

主机正在运行 [Renoise](http://www.renoise.com/) ，这是一个非常受欢迎的跟踪器，可以接受 MIDI 和 OSC 输入。一个处理应用程序分析球的旋转、自由落体和撞击，在一段时间内对它们进行平均，并将其输入 Renoise 的 OSC 输入。在[Lizzie]的视频中，球旋转被发送到基线轨道上的低通滤波器，平均影响被应用到人声轨道。

这不是我们第一次看到一些相当奇怪的方式来调节 wub 本月早些时候，我们看到了覆盖史奇雷克斯的真实乐器。不过，配音之球在简洁方面胜出。
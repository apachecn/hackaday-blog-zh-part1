# Etch-a-Sketch 自动向 Hack A Day 致敬

> 原文：<https://hackaday.com/2011/08/05/etch-a-sketch-automatically-draws-a-tribute-to-hack-a-day/>

![automated_etch_a_sketch_hack_a_day_logo](img/a96226cf3de4e929259b2377f3155146.png "automated_etch_a_sketch_hack_a_day_logo")

在我们这个时代，我们已经看到了相当多的自动蚀刻素描机，但是当[Jason]写信来分享他对这个主题的看法时，它附带了一笔不错的贿赂。我们虚荣。这并不是我们引以为豪的事情，但当看到一个机器人画出的 Hack a Day 徽标时，我们会被说服。

[Jason]有几个 CNC 路由器，他认为自动化他小时候喜欢的玩具 Etch-a-Sketch 会很有趣。他用他的新数控机床给玩具切了一些齿轮和面板，然后开始忙着给他的螺旋桨微控制器编程来完成他的命令。

一块 CNC 软件处理位图图像到轮廓的转换，然后轮廓被转换成 CNC 切割路径。切割路径由一点 C++代码转换成 x/y 坐标，然后输入微控制器，微控制器正在运行一个他称为 RoboSketch 的小型旋转应用程序。推进器负责剩下的工作，快速将图像或图案绘制到草图上。

如果你想看[Jason]致敬 Hack a Day 的视频，请继续阅读，如果这是你要做的事情，请不要错过我们之前的自动蚀刻草图报道。

[https://www.youtube.com/embed/-MNqW1GT4nc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-MNqW1GT4nc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
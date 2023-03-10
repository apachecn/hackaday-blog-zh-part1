# 使用 Kinect 的高级机械臂控制

> 原文：<https://hackaday.com/2011/05/06/advanced-robotic-arm-control-using-kinect/>

![kinect_teleoperation](img/c6f2a053fc8049b4b6e85668afbbe76d.png "kinect_teleoperation")

[瑞恩·洛伊德]、[桑德普·杜尔]和[鲁本·德萨]来信分享了他们最近一直忙于的一个机器人项目。明尼苏达大学的三名学生[正在使用 Kinect 传感器远程控制机械臂](http://embeddedzone.blogspot.com/2011/05/teleoperation-of-5-dof-robotic-arm.html)，但这并不像听起来那么简单。

使用 OpenNI 和 PrimeSense，该团队在使用机械臂之前，先做了一些简单的骨骼跟踪。该手臂有五个自由度，这使得控制它的任务有点棘手。这个机器人有相当多的关节可以玩，所以三人组不仅可以跟踪肩膀，肘部和手腕的运动，还可以监控用户手的状态，以驱动机器人的手爪。

当一切都说了，做了，结果非常令人印象深刻，正如你在下面的视频中看到的，但团队肯定看到了改进的空间。使用反向运动学，他们计划过滤掉当肩膀以某种方式移动时出现的一些关节跟踪不准确。他们还计划使用具有更多自由度的机械臂来看看他们的软件能执行得有多好。

一定要去他们的网站看看更多的细节和视频。

[https://www.youtube.com/embed/nB8WmU0oFFA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nB8WmU0oFFA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
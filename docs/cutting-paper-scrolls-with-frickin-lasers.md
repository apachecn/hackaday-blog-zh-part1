# 用该死的激光切割纸卷

> 原文：<https://hackaday.com/2011/05/04/cutting-paper-scrolls-with-frickin-lasers/>

![](img/75d8994086e08205ea6b3a8990f6b9b3.png "scrolling-add-on-for-laser-cutter")

该电路图[为激光切割机](http://www.instructables.com/id/Scrollable-Laser-Cutting-Addition)的床身增加了一个滚动送纸器。在休息后的视频中，您可以看到实际组件被放在激光切割机床上。在激光切割出指定的图案后，卷轴被卷绕以将未切割的部分移动到位。它使用伺服电机来驱动其中一个线轴。

带有伺服屏蔽的 Arduino Uno 被用于该应用。它有一个按钮，可以在预先设定的时间内缠绕一个卷轴。这种设置有一些问题，即它没有绑定到运行激光器的 CNC 程序中。像这样使用连续旋转的伺服系统也缺乏精确性。如果它升级到使用步进电机，并与 CNC 硬件相连，这将使为你的钢琴切割新卷轴变得轻而易举。

这是一个相反的项目，[它将旧的播放器钢琴卷数字化](http://hackaday.com/2011/01/11/digitizing-player-piano-rolls/)。

[https://www.youtube.com/embed/3UIKW_1kibo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3UIKW_1kibo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# IDisplay，网络摄像头多点触控

> 原文：<https://hackaday.com/2009/06/26/idisplay-webcam-multitouch/>

[https://www.youtube.com/embed/mlLY0zic7u0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mlLY0zic7u0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

上面嵌入的是由[Lahiru]制作的有趣的多点触控演示。该项目的目标是找到一种简单的方法来为多点触控改造当前的液晶显示器[。它没有使用红外或电容识别，而是使用安装在头顶的标准网络摄像头。为了校准，你在桌面屏幕周围画一个多边形，就像摄像头看到的那样。摄像机可以识别放置在屏幕上的标记的位置及其颜色。iDisplay 还可以识别手的挤压动作，并通过 TUIO 将这些动作作为触摸事件发送，因此它可以与现有的触摸软件配合使用。它是用 C++写的，使用](http://www.soundofcode.com/idisplay "Sound of Code | Research | iDisplay") [OpenCV](http://sourceforge.net/projects/opencvlibrary/ "SourceForge.net: Open Computer Vision Library") 进行图像处理，使用[open framework](http://www.openframeworks.cc/ "openFrameworks")作为应用框架。

[via [NUI 集团](http://nuigroup.com/log/i_display/ "NUI Group - Natural User Interface Group")
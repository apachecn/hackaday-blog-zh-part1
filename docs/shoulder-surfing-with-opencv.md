# 使用 OpenCV 进行肩部冲浪

> 原文：<https://hackaday.com/2011/07/12/shoulder-surfing-with-opencv/>

![shoulder_surfing_with_shoulder_pad](img/91f00eb2c41e80e35b872a0af726d1c3.png "shoulder_surfing_with_shoulder_pad")

虽然看起来许多人明智地肩负起上网的责任，警惕任何人窥探他们的密码，但[哈龙]写道，提醒我们今天的威胁和过去一样真实。

他的研究对象是触摸屏手机和平板电脑，它们利用屏幕键盘进行数据输入。他说，虽然这些设备上几乎所有的密码输入框都被传统的星号线遮住了，但键盘本身是一个非常有趣的漏洞。

由于触摸屏技术有时会很挑剔，大多数供应商都会在他们的设备上安装某种按键验证系统。例如，在 iPhone 和 iPad 上，按下一个按钮后，每个键都以蓝色高亮显示。如果你不注意的话，这个功能使得肩扛冲浪者可以很容易地窃取你的密码。

但是如果你很清楚你周围的环境呢？[哈龙]开发了一款他称之为 shoulderPad 的软件，这款软件基于 openCV，可以帮他冲浪。该应用程序可以监控视频流，无论是直播还是录制的，从高亮显示的按钮按压中提取用户的密码。他的演示显示录音发生在相对较近的距离，但他说，使用监控录像或变焦镜头从远处捕捉按键是非常容易的。

他确实说，在 iPhone 的选项窗格中可以很容易地禁用按钮高亮显示，这应该在很大程度上消除了这种攻击。

继续阅读，观看 shoulderPad 的快速视频。

[https://www.youtube.com/embed/RGS4q-WHTlg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RGS4q-WHTlg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
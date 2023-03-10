# 无线控制器操作您的数控铣床

> 原文：<https://hackaday.com/2011/05/28/wireless-controller-operates-your-cnc-mill/>

![](img/c4356190743ebc529d4a68134b306886.png "sixaxis-cnc-control-pendant")

[Darrell Taylor]想为他的工厂增加一个 CNC 控制悬架式操纵台，但不想支付通常高达数百美元的费用。这些挂件基本上是一个物理遥控器，操作控制机器的 CNC 软件。因为他已经在使用运行 EMC2 的 Linux 系统，所以弄清楚如何用 PlayStation 控制器操作工厂并不困难。

为了让控制器与他的 Linux 机器对话，他使用了一个名为 [QtsixA](http://qtsixa.sourceforge.net/) 的包。该软件包通过蓝牙配对来识别和加载控件。在那里，它可以用来将按钮和操纵杆映射为键盘上的按键或鼠标。在休息后的视频中，[Darrell]演示了他是如何设置快捷方式的。他能够移动机器的头部，甚至启动或逐步完成程序。正如他提到的，如果你的手很脏，这是很好的；只需将控制器放入拉链袋中，您就可以开始工作了。

[https://www.youtube.com/embed/ZIg2FO6e52k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZIg2FO6e52k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
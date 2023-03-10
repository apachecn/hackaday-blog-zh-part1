# 一个随机的 USB 沙漏

> 原文：<https://hackaday.com/2009/12/21/a-random-usb-hourglass/>

![](img/7791e102f86d3e76d05b1a9042ebbf42.png "ditigtalhourglass")

[【彼得】想到了一个](http://home.comcast.net/~hourglass/)创意，以低于 100 美元的价格产生[随机熵](http://vimeo.com/6389601)的方法。

USB 沙漏结合了一个带有旋转机构的沙子计时器和一个穿过计时器中心的光束，以观察下落的沙子。到达探测器的光量以频繁的间隔被数字化，并由微控制器处理[以确定何时旋转沙漏。数字化的光水平也通过 USB](http://www.arduino.cc/en/Main/ArduinoBoardDuemilanove) 被[发送到主机，在那里它们可以被用作随机熵的来源。通过 USB 电缆供电。](http://www.ftdichip.com/Products/FT232R.htm)

使用 USB 沙漏，用户可以看到沙子从沙漏的中心落下，并监控 USB 输出数据的随机性。并且一个[可以逐行读取代码](http://home.comcast.net/~hourglass/Hourglass.pde)，编译它，并仅使用开源和广泛支持的工具将其上传到微控制器。
# 我是 Root！–IP 摄像机外壳访问

> 原文：<https://hackaday.com/2011/06/03/i-am-root-ip-camera-shell-access/>

![](img/4c9ff25447f297f64f05eb1c5e3dd277.png "ip-camera-shell-access")

[Shawn]给我们发了一些照片和他最近被黑的描述。他打开了一个罗斯威尔·RXS-3211 IP 摄像头，因为网络界面的输出让他确信它运行的是 Linux，他想从这个设备中释放更多的潜力。这些摄像头用于安全，并通过 WiFi 连接提供基于浏览器的界面。在研究了电路板之后，他开始在一组无人居住的四个焊盘周围摸索，并设法让一个串行连接启动并运行。该设备的串行终端使用八个数据位、一个停止位和偶数奇偶校验位以 115200 波特运行。

他想知道从这里去哪里，我们有一些想法。你可以在上面的终端读数中看到，当检测到运动时，它会发出通知。我们认为这种运动检测对于小型漫游者来说非常有用，同时增加了现场视频广播。嵌入式 Linux 系统应该能够与设备接口，我们认为一点创造性的编码将为其他用途打开 WiFi 连接。对于一个售价仅为 29 美元的模块来说，这已经不错了。我们已经包括了[Shawn]在休息后发给我们的所有图片，我们很乐意在评论中听到您对这些图片用途的想法。

[![](img/17d5083d0802225f3d4d73151c275e31.png)](https://hackaday.com/wp-content/uploads/2011/06/ip-camera-shell-access.jpg)[![](img/1e87a5fb560ea23562e4f271cd2d350e.png)](https://hackaday.com/wp-content/uploads/2011/06/242866_2116324354159_1427220026_32574683_8174018_o.jpg)[![](img/a69d126868531b6c4f5bb880194b3c10.png)](https://hackaday.com/wp-content/uploads/2011/06/257437_2116325194180_1427220026_32574690_6546964_o.jpg)[![](img/10e56fa971225f19d56d5bad917dd340.png)](https://hackaday.com/wp-content/uploads/2011/06/259296_2116323914148_1427220026_32574682_5545474_o.jpg)[![](img/ac6a157a8b86094ba2b9bbd72a8cefd1.png)](https://hackaday.com/wp-content/uploads/2011/06/259549_2116324834171_1427220026_32574686_1097861_o.jpg)
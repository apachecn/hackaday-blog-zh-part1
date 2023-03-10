# DIY 机器人遥控器

> 原文：<https://hackaday.com/2011/07/18/diy-robot-remote-control/>

![](img/249898d1465b6080d6f0808933c3887a.png "customController")

[Patrick]想要一个遥控器来控制他制造的一些机器人。他还想从他的机器人那里获得一些数据，因此一个廉价的现成解决方案无法完成这项任务。像所有优秀的极客一样，[Patrick]决定[建造他需要的东西](http://www.patrickmccabemakes.com/PatrickMccabeMakes/ControllerV2.html)。

对于模拟控制，[Patrick]决定使用 Wiimote 双截棍。事实证明这是一个非常好的选择——双截棍在一个小巧、易于接口的封装中集成了 2 轴操纵杆和 3 轴加速度计。无线电台由 XBee 模块负责。对于微控制器，创建了定制的“ [lcd 背包](http://www.patrickmccabemakes.com/PatrickMccabeMakes/ControllerV2_files/DSC05877.jpg)”，为双节棍提供一个 I2C 端口，为按钮和单个电位计提供输入，为 FTDI 和 XBee 提供 2 个串行端口。

虽然用已经排列好的 LCD 显示器的引脚制造 PCB 的想法非常好，但我们想知道机器人可以接收什么样的数据。9.6kbps 不是很大的带宽，所以视频是不可能的。如果你有什么可以从机器人上下载的想法，请在评论中提出来。

下面是[Patrick]定制控制器的视频。

[https://www.youtube.com/embed/u5egHV2l_So?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u5egHV2l_So?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) [https://www.youtube.com/embed/oVdeYgdxxjM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/oVdeYgdxxjM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
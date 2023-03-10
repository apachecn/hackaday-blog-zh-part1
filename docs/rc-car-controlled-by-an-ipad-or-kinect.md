# 由 IPad 或 Kinect 控制的遥控汽车

> 原文：<https://hackaday.com/2011/03/31/rc-car-controlled-by-an-ipad-or-kinect/>

![ipad_kinect_rc_control](img/5349d9e43c0f402abbf413430d6c3a16.png "ipad_kinect_rc_control")

遥控汽车可以带来无穷的乐趣，但有时乐趣过一会儿就没了。[Gaurav]厌倦了用遥控器操纵他的遥控汽车，所以他建立了一个界面，让他使用两种不同的运动检测设备控制汽车。

他为自己的 iPad 开发了一个 HTML5 应用程序，可以让他驾驶汽车。正如你在下面的视频中看到的，该应用程序利用 iPad 的倾斜传感器来激活汽车的电机和转向，这取决于他在屏幕上移动导向标记的位置。

他设计的第二种转向方法是使用 Kinect 传感器来跟踪他的运动。他的手势被映射到一组类似于 iPad 使用的虚拟空间。通过在这些区域移动双手，Arduino 就像使用 iPad 一样触发汽车的遥控器。

实际的遥控接口是通过几个光隔离器将汽车遥控器连接到 Arduino 来实现的。Arduino 也通过串行端口连接到他的计算机，在那里它等待命令被发送。对于 iPad，Python 服务器等待 HTML5 应用程序发出命令。Kinect 的界面略有不同，一个 C#应用程序监控他的动作，并将命令直接发送到串行端口。

查看下面的视频，看看汽车的运行情况，如果你有兴趣抓取一些源代码并亲自尝试一下，请访问他的网站。

[https://www.youtube.com/embed/D7Ses-VGU9U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/D7Ses-VGU9U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
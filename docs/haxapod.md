# 六足履带车

> 原文：<https://hackaday.com/2008/11/01/haxapod/>

![](img/bf9b9e753d8325eef5f749c83bb7b3da.png "bug")

这个六足机器人是在【杰米】的[终点](http://hackaday.com/contact-hack-a-day/)送到我们这里的。如果你想把六足机器人带得比我们之前的帖子更远一点，这里的和这里的，这是给你的[六足机器人](http://www.webx.dk/robot-crawler/robot-crawler.htm)。对结构件进行建模，并使用 CNC 从 3 毫米厚的胶合板上切割下来。他使用-220 晶体管尼龙隔离安装轴承，螺栓和锁紧螺母在每个关节。主体装有八个伺服系统，六个用于腿部，两个用于摄像头的平移和倾斜。另外还有六个伺服系统，每条腿一个，用来抬起脚。整个事情是由一个时钟频率为 8 Mhz 的 Atmel AT90S8515 控制的。代码是使用 WinAVR free GCC GNU-C 编译的。他使用一个 [PlayStation 控制器](http://www.webx.dk/robot-crawler/ps-joy.htm)来帮助调试行走周期，并根据需要更改参数。跳完后看个视频。
 [https://www.youtube.com/embed/jWQVH0tBcIY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jWQVH0tBcIY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
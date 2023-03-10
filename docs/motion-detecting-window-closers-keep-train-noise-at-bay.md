# 运动检测闭窗器可防止列车噪音

> 原文：<https://hackaday.com/2011/09/13/motion-detecting-window-closers-keep-train-noise-at-bay/>

![motion_detecting_window_closers](img/e98b3cababb3a118067e92d915d3e7d2.png "motion_detecting_window_closers")

[Ed Rogers]不幸地住在一组火车轨道旁边，作为一个高度重视睡眠的人，他需要找到一种方法将卧室的噪音降到最低。为了对抗过往火车的声音，他为自己建造了一个系统，当火车经过他的公寓时，它会自动关闭窗户。

该装置依赖于一个网络摄像头，它使用运动感应软件来检测经过的火车。视频由他房间里的电脑进行分析，当火车靠近时，电脑会向 Arduino 发送信息。Arduino 然后发送一对安装在窗户上的线性致动器，慢慢地(安静地)关闭他的窗户。

正如你在下面的视频中看到的，线性致动器移动得相当慢，但我们怀疑这有什么关系。由于看起来[Ed]住在一个慢行区，一列货运列车可能需要相当长的时间才能通过，因此 40 秒的关闭时间是不合理的。

[https://www.youtube.com/embed/aBhF_qfG4Qc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aBhF_qfG4Qc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
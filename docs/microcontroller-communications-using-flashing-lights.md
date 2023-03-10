# 使用闪光灯的微控制器通信

> 原文：<https://hackaday.com/2011/07/28/microcontroller-communications-using-flashing-lights/>

![phototransistor_pc_microcontroller_communications](img/d09e668f59af914c613ed238051fa28c.png "phototransistor_pc_microcontroller_communications")

[斯科特]在瓢泼大雨中开车，跟在一辆开着转向灯的汽车后面[，这时灵感来了](http://www.swharden.com/blog/2011-07-26-pcmicrocontroller-wireless-data-transfer/)。他之前用他的声卡创建了一个简单的通信系统，允许他从他的个人电脑向微控制器[发送数据，但是他认为用光做同样的事情会是一个有趣的练习。](http://hackaday.com/2011/07/10/sound-card-microcontrollerpc-communication/)

他认为建立这样一个系统的最好方法是使用一个光电晶体管和他的计算机显示器来发送数据到他的微控制器。虽然他真的想不出这个项目的任何实际应用，但这并没有阻止他只是为了开心而把它放在一起。

[Scott]说电路非常简单，包括一对光电晶体管及其所需的电阻。接收器被连接到他的微控制器的 ADC 中，在那里他可以很容易地拾取一些简单的光图案。他的最终目标是组装一个 javascript 应用程序，将数据发送到他的微控制器，尽管他正在寻找编程方面的一点帮助——有人愿意吗？

虽然[斯科特]一时想不出任何申请，但我们知道至少有一个。任何熟悉彭博金融应用程序的人都可能遇到过他们的“B 单位”。这个硬件和信用卡差不多大，但是更厚。它配备了指纹扫描仪和光电二极管，可以从您的计算机屏幕上读取一系列闪烁的灯光，以便为每个不是通过彭博官方键盘启动的登录会话“同步”设备。所以有一个给你！

继续阅读，观看系统运行的视频。

[https://www.youtube.com/embed/lvVjsMMCx0U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lvVjsMMCx0U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
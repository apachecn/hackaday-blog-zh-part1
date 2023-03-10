# 构建步进驱动器

> 原文：<https://hackaday.com/2011/07/11/building-a-stepper-driver/>

![](img/afa0eefa68e94edf89601557d31721eb.png "stepper-motor-controller")

[TBJ]正在建造他称之为垃圾箱的 3D 打印机。你可能会猜测，他正试图挽救设备的大部分部件，在从一台旧打印机中取出步进电机后，他需要一种方法来控制它。他想出的是[一个步进驱动器，它使用容易获得且便宜的分立元件](http://i1190.photobucket.com/albums/z441/TBJsTechStuff/stepmotor.png)。该设计需要两个输入，一个切换电机旋转的方向，另一个触发电机的一个步骤。CD4013 双触发器在一个芯片封装中处理这两种输入。

该电机由一对 H 桥驱动，每对 H 桥由六个晶体管组成。步进电机的诀窍在于，你需要在特定的时间将电机的四个电极驱动到特定的逻辑电平。为此[TBJ]使用了 CD4017 十进制计数器。基于控制方向的触发器，二极管网络将一半输出线接地。我们的朋友 555 定时器为电路提供了一个时钟，使一切都以预定的速度运行。休息之后，请观看视频，了解解释和演示。

[https://www.youtube.com/embed/Y2fGj9A0MQI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Y2fGj9A0MQI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
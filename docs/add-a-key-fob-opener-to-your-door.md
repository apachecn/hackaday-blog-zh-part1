# 给你的门增加一个遥控钥匙开启器

> 原文：<https://hackaday.com/2009/10/14/add-a-key-fob-opener-to-your-door/>

![key-fob-door-opener](img/0073ef8cd8a2d7191c57eec4205b7d28.png "key-fob-door-opener")

似乎制造一个自动宿舍开门器是每年秋天的极客仪式。【亚当】是[瓦萨](http://www.vassar.edu)的学生，通过[创建这个干净的设置](http://www.youtube.com/watch?v=GJVnNBD6aw4)成功通过。休息后我们有视频，更多图片和描述。

![door-opener-overview](img/84ea4849e9a37dce787e0b25dd7dff28.png "door-opener-overview")

上面我们看到这个装置安装在门的里面。较大的盒子中装有一个打印头托架，它可以转动手柄。当马车从右向左移动时，它拉动连接在门把手上的长杆上的绳子(见柱子顶部的图片)，从而提供转动运动。这个盒子下面是我们接下来要看的控制电路。

![door-opener-electronics](img/eb6c705b830e0e1f3e75fe22279c65ff.png "door-opener-electronics")

这里我们有操作的大脑。在左侧的项目框中是一个电路板，负责无线 fob 通信。[Adam]告诉我们，它在大约 250 英尺的温度下工作，使用基于射频的滚动算法来确保安全，并且有一个专用的 12v DC 电源。中间是控制电机运行的定时器电路，四节 9v 电池为电机供电。

![door-opener-breadboard](img/e1ba5bc34de702f65dbb46ef18ec257f.png "door-opener-breadboard")

电机控制由使用三个 555 定时器 IC 的定时电路提供。[Adam]的设计基于一个双芯片延迟电路,但将其扩大到三个，给他更多的选择。该电路负责驱动电机，直到锁闩打开，保持一段设定的时间，然后将电机返回到其原始位置。

![door-opener-module-connection](img/c438d0c417ae5cf469b06ebfc457a3e8.png "door-opener-module-connection")

因为他将在年底搬出去，[亚当]想使系统易于运输。他使用了一个千斤顶系统，这样控制器可以安装在他下一个住处的电机单元的上方或下方。

这样做很好，而且有了项目箱上的盖子，就不会像我们看到的最后一个开门器上的胶带一样乱七八糟。干得好！

[https://www.youtube.com/embed/GJVnNBD6aw4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/GJVnNBD6aw4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
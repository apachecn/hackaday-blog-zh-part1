# 2010 年智能地面车辆竞赛第二天报告

> 原文：<https://hackaday.com/2010/06/07/intelligent-ground-vehicle-competition-2010-day-two-report/>

[![](img/b2bc3fd2e0ba996a4a24945c04856b35.png "cultureshockII")](http://hackaday.com/wp-content/uploads/2010/06/cultureshockii.jpg)

劳伦斯理工大学团队的机器人“文化冲击 II”首先引起了我们的注意，因为它独特的传动系统。经过进一步的调查，我们发现了一个非常好的机器人，有很多独特的功能。

关于 CultureShockII，我们首先注意到的是巨大的 36 英寸车轮。车轮组件实际上是由底部的齿轮马达驱动的独轮车。选择如此大的轮子的原因是为了保持重心远低于轮轴，提供一个非常自我稳定的机器人。该机器人还有两个带悬挂系统的脚轮，在震动和倾斜的情况下充当减震器和稳定器。如下图。

[![](img/f2f697ac5ca253e4fcdfb8d75e6893e2.png "suspendedcaster")](http://hackaday.com/wp-content/uploads/2010/06/suspendedcaster.jpg)

我们注意到的下一件事是安装在脚轮上方的奇怪的半圆。经过进一步的调查，我们发现机器人使用 10 个激光器将十字线投射到地面上，这样它就可以在晚上使用它的立体视觉。

[![](img/d1e569f1b0baeeab0b1f06202024047e.png "lasers")](http://hackaday.com/wp-content/uploads/2010/06/lasers.jpg)

这个机器人有两个来自 Videre 的立体视觉摄像头，这个品牌在今年的 IGVC 上非常受欢迎。相机重叠并为人工智能提供与像素相关的 3d 点地图。该团队还想出了一个聪明的方法，通过两根“拐杖糖”伸入机器人的视野，来调整相机以适应不同的照明情况。机器人可以看到这些，并使用算法来调整相应的颜色。这对白线检测非常有帮助。(机器人必须呆在草地上画的两条相距约 10 英尺的白线内。)

[![](img/85562be6ca0ba034a103ff4694caf645.png "caaaandycaaane")](http://hackaday.com/wp-content/uploads/2010/06/caaaandycaaane.jpg)

除了立体视觉，机器人还具有一个 Omnistar-VBS 启用的 gps，能够达到亚米精度和一个[数字指南针](http://www.tri-m.com/products/precisionnav/tcm3.html)。除了摄像机的驱动软件，这个机器人完全是用 Java 编写的。人工智能使用逐帧映射。每一帧机器人都在远处设定一个目标并向它移动。在下一帧中，机器人检查目标是否仍然可以到达，并向其移动，否则它会改变路径。为了绕开物体，机器人会抱住障碍物，直到它在障碍物后面。该系统是映射和反应式人工智能的混合。

机器人的大脑是一个运行 32 位 windows 的 2.4GHz 英特尔酷睿 2 四核处理器。它有一个固态硬盘和 4GB 内存。值得注意的一件很酷的事情是，所有的传感器和微控制器都使用 ATX 为计算机供电。他们没有使用逆变器，而是找到了合适的 12V ATX 电源。

[![](img/26ec6b676a2a2c1732ce091ffa749bcb.png "rearcontrolpanel")](http://hackaday.com/wp-content/uploads/2010/06/rearcontrolpanel.jpg)

后控制面板也很整洁。它有一个触摸屏，所有主要组件的开关和状态 led。在它的下面，你可以看到电脑的背面，装在一个梭型的 thermaltake 盒子里。

[![](img/de8c9ae92d4a583aca01e89bc4ace878.png "guuuuutssss")](http://hackaday.com/wp-content/uploads/2010/06/guuuuutssss.jpg)

如果你把前面的面板拿掉，你会看到机器人的电源和信号分配。绿色电路板是一个运行电机并管理 PID 反馈的 [Roboteq AX3500](http://www.roboteq.com/brushed-dc-motor-controllers/ax3500-dual-60a-brushed-dc-motor-controller.html) 。这个机器人的底部有 70 磅的密封铅酸电池，可以运行大约两个小时。这个机器人的远程紧急停止(规则要求的)实际上是一个远程车库门开启器，被黑客入侵来打开和关闭机器人。

我们将以一个快乐的工程师在他们的机器人上工作的镜头来结束。

[![](img/d7319a6b5dfc1520a3d30be8649f0612.png "igvctent")](http://hackaday.com/wp-content/uploads/2010/06/igvctent.jpg)

*取决于机器人的状态

[第一天报告](http://hackaday.com/2010/06/05/intelligent-ground-vehicle-competition-2010-day-one-report/)
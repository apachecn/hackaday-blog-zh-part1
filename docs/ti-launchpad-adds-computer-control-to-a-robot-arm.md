# TI Launchpad 为机器人手臂增加了计算机控制

> 原文：<https://hackaday.com/2011/11/21/ti-launchpad-adds-computer-control-to-a-robot-arm/>

![](img/74be79fcd928c8d4ac4939dad05274e3.png "launchpad-gives-better-robot-arm-control")

[Eric Gregori]有一个 OWI535 玩具机械臂。虽然很便宜(大约 30 美元)，但这种手臂只能通过有线控制盒使用。[Eric]知道他可以通过 TI Launchpad 和电机驱动外设增加计算机控制来做得更好。

手臂有肩关节、肘关节和腕关节，一个旋转基座和一个手爪。所有这些都是由 3V DC 电机驱动，只有两条控制线。[Eric 的]用于 Launchpad 的电机驱动器附件在这种情况下非常有用。它有三个 FAN8200 双电机驱动器芯片，因此它可以控制多达六个电机。一旦他建立了硬件连接，就只需要通过 USB 接口向 Launchpad 发送命令，但你还需要使用比 Launchpad 更大的微控制器。这里他选择了一个 MSP430G2553。

为了让事情变得更有趣，他还写了一个 GUI 来控制电脑上的手臂。他使用了 RobotSee，这是一种编程语言，可以让你使用硬件的图像，并在其上覆盖控件。现在他只需要把它做成一个网络界面，他就可以拥有一个智能手机控制的起重机游戏。

休息之后别忘了看看视频。

[https://www.youtube.com/embed/TRHseQalxdY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TRHseQalxdY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
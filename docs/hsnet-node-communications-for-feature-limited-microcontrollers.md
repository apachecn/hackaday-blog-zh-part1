# HsNet:功能受限微控制器的节点通信

> 原文：<https://hackaday.com/2011/04/15/hsnet-node-communications-for-feature-limited-microcontrollers/>

![](img/3237f5e6c1af0d8a6ce68387176dd46d.png "HsNet-node-communications")

[迭戈·斯皮诺拉]来信告诉我们他一直在研究的一个名为 HsNet 的节点通信系统。目标是建立一个由小而便宜的微控制器组成的节点系统。问题是最便宜的控制器通常没有硬件 UART。HsNet 使用软件 UART 和纤薄、时尚的寻址方案实现 RS485 协议。

开发的第一个模块是使用 PIC 12F683 的单通道脉宽调制节点,见上图和休息后的视频。它可以在[HsNet 数据包格式](http://www.hackeneering.com/Tiki/wiki/tiki-index.php?page=HsNetNetCmds)的有效载荷中发送命令。PWM 模块接受三种不同的命令；一个是期望的 PWM 值，另一个是 PWM 步骤之间的延迟，最后一个触发闪烁功能。

他还开发了模拟传感器模块和基于 Arduino 的 TCP/IC 网关模块。既然已经建立了包通信，那么在此基础上添加节点就相当简单了。[Diego]将这些组件组合在一起，构建了一面互动墙，休息后也可以看到。

**PWM 节点:**

[https://www.youtube.com/embed/I8UC-3-twBo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/I8UC-3-twBo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

**墙壁艺术品:**

[vimeo http://vimeo.com/18570263 w=470]
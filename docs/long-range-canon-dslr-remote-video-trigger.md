# 远程佳能 DSLR 远程视频触发器

> 原文：<https://hackaday.com/2011/05/26/long-range-canon-dslr-remote-video-trigger/>

![canon_60D_remote_video_trigger](img/ce504240190c86a9d0bff9f934ea246a.png "canon_60D_remote_video_trigger")

Instructables 用户[Justin]普遍喜欢用他的佳能 60D DSLR 拍摄视频，尽管有一个小问题。唯一可以远程触发摄像机拍摄视频的方法是通过一个 10 英尺范围的小型红外遥控器。更糟糕的是，遥控器必须直接指向摄像机前方才能工作。为了补救这种情况，他决定安装自己的远程触发装置。

他用身边的组件拼凑了一个 Arduino，将其安装在相机顶部的项目箱中。一个商用的射频遥控快门也安装在相机的顶部，并使用一个 2.5 毫米的小插头连接到 Arduino。当他激活 RF 遥控器时，它会向 Arduino 发送一个脉冲，Arduino 又会通过一个小的 IR LED 向他的相机发送适当的信号。

虽然他很乐意承认他可能使用了更简单的配置，但 Arduino 完成了它的工作，他对自己的解决方案很满意。我们同意他关于 Arduino 的观点，但是很难否认使用你手头已经有的组件来省钱。
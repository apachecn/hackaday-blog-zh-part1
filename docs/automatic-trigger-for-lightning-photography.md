# 闪电摄影的自动触发器

> 原文：<https://hackaday.com/2011/03/26/automatic-trigger-for-lightning-photography/>

![lightning_trigger](img/9b0cfaf1a07073324bc846e09040acdf.png "lightning_trigger")

[Vicktor]一直对闪电照片着迷，并决定尝试用他的相机捕捉一些闪电。然而每次他尝试的时候，他都没有成功。他决定[制造一个闪电触发器来代替手动操作他的相机拍摄图像](http://diy.viktak.com/2011/03/zeus-lightning-trigger-for-cameras.html)。

他的电路使用一个大型光电二极管来感应闪电，通过被黑掉的快门释放电缆触发相机。PIC 微控制器用于调整设备的灵敏度，并向摄像机发送实际的触发信号。他的电路通过一对光耦合器连接到相机，以确保他的电路不会对相机造成任何伤害。

当盒子通电时，它进入校准模式，在该模式下，用户可以调整电路来补偿存在的任何环境光量。一旦启动，盒子等待环境光线的突然变化，向相机发送曝光释放信号。

在他的网站上有一个原理图，他会根据你的要求把他使用的代码发给你。目前还没有触发器动作的视频，但希望我们能很快看到。

如果你有兴趣看看其他遥控相机触发器，看看这个由空气清新剂部件制成的[和这个使用激光的](http://hackaday.com/2011/02/04/remote-camera-trigger-built-from-air-freshener-parts/)。
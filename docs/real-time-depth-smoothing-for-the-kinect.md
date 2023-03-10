# Kinect 的实时深度平滑

> 原文：<https://hackaday.com/2012/01/25/real-time-depth-smoothing-for-the-kinect/>

![](img/7955e097442e542f0cb774d412396947.png "real-time-depth-smoothing")

[Karl]着手改善 Kinect 摄像头能够输入计算机的深度图像。他想出了一个预处理包[，实时平滑深度数据](http://www.codeproject.com/Articles/317974/KinectDepthSmoothing)。

这里有几个问题，一个是 Kinect 的分辨率相当低，它的深度仅限于距离设备大约 8 米的范围内(这是我们在研究基于 Kinect 的地图解决方案时没有考虑的问题)。但是这些缺点的缺点可以通过改进它收集的数据来减轻。[Karl]的方法是双重的:像素过滤和运动平均。

像素过滤与深度数据一起工作，以帮助澄清对象的轮廓。加权移动平均用于帮助减少逐帧渲染的闪烁区域的数量。[Karl]包含了一个很好的 GUI 代码，可以让你调整过滤器设置，直到它们刚刚好。休息后在剪辑中看到该界面的演示，并通过留下评论让我们知道您可能会使用它。

[https://www.youtube.com/embed/YZ64kJ--aeg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YZ64kJ--aeg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
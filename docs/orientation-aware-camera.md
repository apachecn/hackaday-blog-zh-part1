# 方位感知相机

> 原文：<https://hackaday.com/2008/10/23/orientation-aware-camera/>

![](img/1576e31825cb77638c0f7ad19a018cf1.png "oac")
【安德鲁·马吉尔】刚刚把他的[方位感知相机](http://ominoushum.com/oac/ "Orientation Aware Camera")加入了 [Hack a Day Flickr 池](http://www.flickr.com/groups/hack-a-day/pool/ "The Hack a Day Pool")。它使用三轴磁力计和三轴加速计。他不想在 USB 方面花费太多精力，所以他选择了 USBMicro 的 U421。这是一个相当好的记录预编程 USB 微控制器。他后来后悔了；由于所有的开销，他的最终采样率只有 5Hz。使用位置数据，摄像头图像可以针对任何种类的抖动进行校正。[Andrew]更进一步，使用 OpenGL 将所有视频帧拼接成完整的全景图。请务必观看下面嵌入的他的精彩视频演示。
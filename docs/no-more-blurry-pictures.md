# 不再有模糊的照片

> 原文：<https://hackaday.com/2011/01/22/no-more-blurry-pictures/>

![](img/64e69bb3782243175e8aae496b04f50b.png "deblurring-images-using-inertial-sensors.jpg")

有了这款附加硬件，您就可以告别被破坏的图像了。当拍摄照片时，它会测量相机的移动，[会校正图像以消除运动模糊](http://research.microsoft.com/en-us/um/redmond/groups/ivm/imudeblurring/)。上面你可以看到一个高速相机，它只是用来测试和微调修复照片的算法。一旦他们做对了，相机连接的设置只包括 Arduino 板、蓝牙调制解调器、三轴加速度计、陀螺仪和相机触发器。你使用新的硬件来拍摄每张图像，它负责触发单反的快门，以确保惯性数据和图像正确同步。

[谢谢罗伯]
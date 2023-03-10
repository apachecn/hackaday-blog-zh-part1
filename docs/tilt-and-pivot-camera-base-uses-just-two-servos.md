# 倾斜和旋转摄像机底座仅使用两个伺服系统

> 原文：<https://hackaday.com/2011/03/15/tilt-and-pivot-camera-base-uses-just-two-servos/>

![](img/15c6baf2016f439dffff7027143aa491.png "motorized-camera-base")

[Caled]向我们展示了如何建造一个倾斜和旋转的摄像机底座。其中一个可以非常方便地拍摄精确对齐的图像，这些图像随后可以拼接成全景图像，甚至球形图像。我们有一个宏伟的愿景，那就是能够制作出类似于[这些令人惊叹的互动图像](http://www.tourdeforce360.com/madison_protest/)的东西，其硬件比[另一个机动钻机](http://hackaday.com/2010/07/14/panoramic-and-spheric-tripod-rig/)更便宜也更容易制造。

该设计仅使用两个伺服电机。在上面的图片中，你可以看到一对圆盘作为装备的底座。在上面圆盘的中心是第一个伺服系统，指向下方，它旋转摄像机。傻瓜相机两侧的两个直立支架为倾斜功能提供了框架。相机安装在一个框架中，其中心是近侧的螺纹杆，第二伺服电机位于远侧。一个带有伺服保护罩的 Arduino 通过一个按钮垫和一个作为用户界面的 LCD 屏幕来控制运动。项目日志中的最后一步指向[软件选项，用于组合捕获的照片](http://en.wikipedia.org/wiki/Comparison_of_photo_stitching_applications)。
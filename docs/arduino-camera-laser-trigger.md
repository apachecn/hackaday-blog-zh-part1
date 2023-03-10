# Arduino 摄像机激光触发器

> 原文：<https://hackaday.com/2009/06/19/arduino-camera-laser-trigger/>

![pict0005](img/b730a6b628344f7cf0068c27598b943b.png "pict0005")

[亚当]做了一个使用激光的[遥控相机触发器](http://abehman.com/2009/05/11/project-arduino-laser-camera-trigger/)。他必须在他的相机上安装 [CHDK](http://chdk.wikia.com/wiki/CHDK) ，为了让它工作，我们[已经在指南](http://hackaday.com/2008/05/27/how-to-expand-your-camera-with-chdk/)中介绍过了。CHDK 允许通过 USB 端口远程触发快门。激光从一面镜子上反射回来，射到连接在 Arduino 上的感光树脂上。当光束中断时，Arduino 就会触发触发器。他还计划使用触发器通过以太网发微博。嵌入式是演示其功能的视频。

[https://player.vimeo.com/video/4603644](https://player.vimeo.com/video/4603644)

[相关[用你的 DS](http://hackaday.com/2008/09/17/control-your-camera-remotely-with-a-ds/) 遥控你的相机

[途径 [adafruit](http://www.adafruit.com/blog/2009/06/19/arduino-laser-camera-trigger/)
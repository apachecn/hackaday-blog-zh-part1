# PID 控制吸烟器

> 原文：<https://hackaday.com/2011/02/03/pid-controlled-smoker/>

![](img/ad5b5c0283613753ecc65f5ec5699138.png "The-Smoke-O-Tron")

[dafonso]购买了一个不错的 1500 瓦的吸烟器，但有点沮丧的是，它只有一个烹饪温度。为了弥补这一点，他设计了自己的 PID 控制系统，这使得他可以用数字方式设定烹饪温度。该系统的核心是一个 PICAXE 18 微型控制器，它通过一个固态继电器控制吸烟者的开关。他没有在吸烟者身上测试 110 伏的系统(这在室内会很痛苦)，而是用一盏灯来代替。为了看看他是否得到了正确的温度，他把热电偶绑在灯泡上，让 PID 开关灯。也一定要检查他的[视频](http://www.instructables.com/id/Home-reflow-SMD-soldering/)，它很好地解释了他如何能够焊接控制板所需的表面贴装元件。
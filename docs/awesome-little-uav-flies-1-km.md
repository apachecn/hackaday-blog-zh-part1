# 牛逼的小无人机飞 1 公里

> 原文：<https://hackaday.com/2011/12/07/awesome-little-uav-flies-1-km/>

![](img/0d58a91fc3a4cb065c3e52611169ea39.png "UAV")

在去了斯图加特 hackerspace ShackSpace 的 SMD 焊接车间后，[Corvus]决定成为一名成功者，为他自己的[无人机](http://shackspace.de/?p=2659)制造一个飞行控制器。

这架飞机本身是一个普通的商店购买的泡沫装置，本身并不十分有趣。不过，自主飞行激起了一些兴趣。[Corvus]设计并制造了一个定制的飞行控制器 PCB，与一个小型 STM32 Linux 板一起工作。这两块板与 [OpenPilot 项目](http://www.openpilot.org/)结合在一起，让飞机能够自主控制高度、方位、速度和位置。地面站和飞行器之间的遥测由[无人机和一台 ThinkPad 处理。](http://wiki.openpilot.org/display/Doc/UAVTalk)

在休息后的视频中，[Corvus]驾驶飞机上升到高空，然后指挥它向北飞 500 米，然后掉头。结果是超过一公里的自主飞行。该项目的下一阶段是实现一些带有光学路径寻找和障碍避免的 [SLAM](http://en.wikipedia.org/wiki/Simultaneous_localization_and_mapping) 应用。

[https://www.youtube.com/embed/nWNWuUiUTNg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/nWNWuUiUTNg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
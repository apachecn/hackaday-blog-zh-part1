# Android 中的多点触摸补丁

> 原文：<https://hackaday.com/2009/01/13/multitouch-patched-into-android/>

![g11](img/698a11d9a143186c4d3a86e55c60db37.png "g11")

[卢克·哈奇森]想出了一个相当聪明的办法，让 G1 支持多点触摸。他针对 Synaptics 触摸屏驱动程序编写了一个补丁。当放置两个手指时，驾驶员报告中点的 x/y 和尺寸字段的半径。如果只使用一个手指，则大小报告为零。这种方法的好处在于它是向后兼容的；额外的数据将被当前的应用程序忽略。不幸的是，谷歌的 Android 团队表示，如果增加多点触摸，它将识别单个手指，肯定不会使用这种方法。

[via [ABN](http://andblogs.net/2009/01/actual-multitouch-no-weirdness/)

[照片: [tnkgrl](http://flickr.com/photos/tnkgrl/2963842016/in/set-72157608262752711/ "211020082429 on Flickr - Photo Sharing!")
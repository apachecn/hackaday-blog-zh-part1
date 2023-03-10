# V-Synch 检测器允许您在 Linux 系统上使用 3D 快门眼镜

> 原文：<https://hackaday.com/2012/03/28/v-synch-detector-lets-you-use-3d-shutter-glasses-on-linux-systems/>

![](img/0e503311fb057e5bcb5958a54f14e6cd.png "vsync_stereo_closeup")

这个电路就是[John Tsiombikas] [如何让他的廉价 3D 快门眼镜与 Linux 机器](http://codelab.wordpress.com/2012/03/02/vsync-driven-shutter-glasses/)一起工作的。这并不是说它们与 Linux 不兼容。问题是，只有某些视频卡具有驱动头戴式硬件所需的立体声端口。

快门眼镜一次阻挡一只眼睛的光线，因此可以显示不同的效果图来创建立体效果。由于[刺激眼部肌肉实际上不起作用](http://hackaday.com/2011/01/16/electrodes-turn-your-eyelids-into-3d-shutter-glasses/)，你需要找到一种方法，用视频信号在完美的时间内驱动眼镜。他的电路观察垂直同步信号，然后用它来切换快门眼镜。由于硬件无法知道生成的是左帧还是右帧，所以他将拨动开关作为用户控制的调整。如果 3D 效果不佳，您可能用错误的眼睛观看画面，需要切换开关。

不亲自试用硬件，真的没办法展示效果。但是[John]报告说，当与 OpenGL 立体包装器一起使用时，它的效果非常好。
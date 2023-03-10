# 电机驱动器:带制动器的半 H 桥等

> 原文：<https://hackaday.com/2011/10/28/motor-drivers-half-h-bridge-with-brake-and-more/>

![](img/3733a56ad2e007c36475a931d1d38a14.png "half-h-bridge-with-brake")

这里有一个很好的小电路，它将驱动一个马达，并允许你停止它的旋转，给你的机器人一套刹车。这是[JM]关于[构建微控制器友好电机控制器](http://webdelcire.com/wordpress/archives/1269)([翻译为](http://translate.google.com/translate?sl=auto&tl=en&js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&u=http%3A%2F%2Fwebdelcire.com%2Fwordpress%2Farchives%2F1269))的细节的帖子的一部分。

这种特殊设置是半 H 桥。它允许你只在一个方向上驱动电机。电机接地端使用的 MOSFET 实际上不需要在那里。这是让你用电子方式停止马达旋转的制动器。没有它，当半桥关断时，电机将在自己的动量下继续转动。根据应用的不同，这可能是一个大问题。在折叠下方的视频剪辑中，有一个很好的电路制动快速旋转电机的演示。

这是有可能使用 PWM 驱动程序，但[JM]有一些像快速 PWM 内置功能的警告。确保你阅读了他的忠告，如果你需要复习，不要错过这个黑客视频片段。

[https://www.youtube.com/embed/_lqyuR_iWuY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/_lqyuR_iWuY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢贾维]
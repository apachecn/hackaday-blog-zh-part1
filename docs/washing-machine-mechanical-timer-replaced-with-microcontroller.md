# 用微控制器取代洗衣机机械定时器

> 原文：<https://hackaday.com/2011/06/05/washing-machine-mechanical-timer-replaced-with-microcontroller/>

![](img/4d2edb24d7a0c2f39047904ce421ad18.png "panel")

在(保罗·卡内洛的)洗衣机的机电定时器第三次坏了之后，他决定停止修理，并找到一个更永久的修复方法。他决定建立自己的基于微控制器的洗衣服系统 ( [翻译](http://translate.google.com/translate?js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&sl=auto&tl=en&u=http%3A%2F%2Fwww.pablin.com.ar%2Felectron%2Fcircuito%2Fmc%2Flavapic%2Findex.htm))。**注意:**【保罗的】页面上的图像链接似乎被破坏了，如果你点击它们，就会释放出一场永无休止的空弹出窗口风暴。休息之后，我们已经嵌入了所有的图像，为您节省了一些麻烦。

洗衣机上的控制器只不过是一个机械闹钟。它开始循环，然后根据时间的推移在各种模式之间移动。[Paul]通过观察周期之间的延迟时间，并记录机器的哪些部分在每个阶段被打开和关闭，开始了他的黑客生涯。

原来，当转动机械旋钮时，它会改变水流过洗涤剂室的路线。由于新系统中没有这个旋钮，Paul 想出了一种方法，让微控制器通过使用伺服电机来处理这个问题。其余的控制包括控制电机的继电器和水的电磁阀。还有压力开关，可以反馈机器中的水位。PIC 16F872 作为新的控制器，在 7 段显示器、蜂鸣器和一对按钮的帮助下作为用户界面。

这是一个较老的项目，但是在阅读了 Arduino 控制的洗碗机后，Ramiro 给了我们一个链接。谢谢！

[![](img/a3c77f55efbce266a98b51866a8bc379.png)](https://hackaday.com/wp-content/uploads/2011/06/panel.jpg)[![](img/d833a53da07e615a7add2a0bc0548c8e.png)](https://hackaday.com/wp-content/uploads/2011/06/plaqueta.jpg)[![](img/da51961dffad234ecf1b3f33ee4d248c.png)](https://hackaday.com/wp-content/uploads/2011/06/reles.jpg)[![](img/d47ea6d975133137035627e391ae475f.png)](https://hackaday.com/wp-content/uploads/2011/06/servo1.jpg)[![](img/9bca7f99c86dd9fcce1cab524ce41348.png)](https://hackaday.com/wp-content/uploads/2011/06/servo2.jpg)[![](img/381c9db132c65fbb4a31e9a4c25a18f9.png)](https://hackaday.com/wp-content/uploads/2011/06/trafo.jpg)[![](img/b0213a1f598f139da7d5564d93b7c10c.png)](https://hackaday.com/wp-content/uploads/2011/06/valvula.jpg)
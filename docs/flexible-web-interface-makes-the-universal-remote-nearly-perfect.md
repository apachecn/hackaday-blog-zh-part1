# 灵活的网络界面使通用遥控器近乎完美

> 原文：<https://hackaday.com/2012/02/01/flexible-web-interface-makes-the-universal-remote-nearly-perfect/>

![](img/fc7680adc1107bb7f89bc7edbe413e29.png "universal-remote-with-web-interface")

建立了一个基于 Arduino 的通用遥控系统。它使用一个既有红外接收器又有发射器的防护罩。这给了它从你现有的遥控器中学习代码的工具，并播放它们来控制设备。这个功能并不是什么新东西，但是我们认为他为系统开发的用户界面绝对棒极了！

软件是基于网络的。您只需将遥控器对准 Arduino，然后按下按钮。接收器将存储代码，该代码随后可被分配给虚拟按钮。上图显示了正在创建的频道增加选项；一旦确认，它将被添加到列表中。从那里，任何支持网络的设备——智能手机、平板电脑、上网本等——都可以用作系统的遥控器。我们认为唯一缺少的功能是改变按钮布局的能力，用更大的区域来显示最常用的命令。

休息之后，你可以看到这个系统的演示，以及一个我们还没有提到的额外功能。[落聋]在硬件设计中包括一个压电元件，如果智能设备不在手边，它可以让他敲敲咖啡桌来使用遥控器。

[https://www.youtube.com/embed/E3-kM5PS1TE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/E3-kM5PS1TE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
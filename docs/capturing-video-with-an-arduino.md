# 使用 Arduino 捕捉视频

> 原文：<https://hackaday.com/2011/06/07/capturing-video-with-an-arduino/>

[Carlos Agell]提交了一个提示，他用 Arduino 从模拟摄像机中捕获了图像。

我们已经看到[几个](http://hackaday.com/2010/01/18/more-avr-tetris/) AVR/Arduino 黑客*生成*视频，尽管[超频](http://hackaday.com/2011/02/13/overclocked-atmega32-gaming/)是必要的，如果你想做任何超出突破克隆的事情。[Carlos]hack 反其道而行之，现在他可以用 Arduino 捕捉视频。

该项目以 128×96 的分辨率从 NTSC 视频中捕捉单个帧。虽然 Arduino 的功能不足以进行实时捕捉，但[Carlos]通过只捕捉阈值并将它们发送到运行 LabVIEW 中编码的程序的计算机上，成功做到了这一点。PC 程序重新组合阈值的图像，并产生一个 3 位灰度的微小图像。

[卡洛斯]使用了[视频实验者](http://nootropicdesign.com/ve/)盾牌，这本身就令人印象深刻。视频实验者能够进行对象跟踪和边缘检测，所以我们想知道什么时候我们会看到具有计算机视觉的机器人在 Arduino 上运行。休息之后，请查看益智设计视频实验者保护罩的演示。

更新:Carlos 在处理中写了一个[草图，和他的 LabVIEW 程序做同样的事情。](http://hackingelectronics.blogspot.com/2011/06/update-on-arduino-imaging-processing.html)

[https://www.youtube.com/embed/TGy70XxhpMY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/TGy70XxhpMY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
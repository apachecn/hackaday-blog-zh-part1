# 将 BlinkM 变成世界上最小的 Arduino

> 原文：<https://hackaday.com/2011/03/30/converting-the-blinkm-into-the-worlds-tiniest-arduino/>

![blinkm_arduino](img/d2501e383da2a853a3b436419e73cd30.png "blinkm_arduino")

BlinkM“智能 LED”本身就是一个很棒的小设备。它允许使用内置微控制器完全控制其 RGB LED，使用户能够完成通常需要 PWM 才能完成的一系列工作。这个小设备只有半英寸多一点，可能也是市场上最小的 Arduino。

BlinkM 装有 ATiny85 微控制器，这使得它可以与 Arduino 引导加载程序一起刷新，这要感谢[麻省理工学院高低技术小组]的人。他们对 Arduino IDE 配置文件做了一些调整，并加入了一些由[Alessandro Saporetti]创建的核心库代码来完成这项工作–[所有这些都可以在他们的网站](http://hlt.media.mit.edu/wiki/pmwiki.php?n=Main.ArduinoATtiny4585)上找到。

一旦代码被上传到 BlinkM，你实际上就有了一个运行在 8MHz 的微型 Arduino，它有一个内置的 LED 和 2 条 I/O 线(如果你剪掉 LED，有 5 条)。如果你觉得一个完全成熟的 Arduino 在你的项目中是多余的，这是一个很好的设备。

留下来看看重新刷新过程的视频教程。

[https://www.youtube.com/embed/tXbxfsceAEM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tXbxfsceAEM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
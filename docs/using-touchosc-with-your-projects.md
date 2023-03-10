# 在项目中使用 TouchOSC

> 原文：<https://hackaday.com/2011/03/31/using-touchosc-with-your-projects/>

![](img/5dd81f13b461d45072fefb9ed2391436.png "using-touchosc")

[Marcus]写了一个使用 touch OSC 控制你的项目的指南。在阅读了我们关于[在没有以太网屏蔽的情况下为 Arduino](http://hackaday.com/2011/03/27/arduino-and-open-sound-control-without-an-ethernet-shield/) 使用开放式声音控制的专题后，他给我们发了一个链接。他使用这种方法已经有一段时间了，但通过使用智能手机作为控制设备，他更进了一步。他使用 TouchOSC 为 iPhone 设计了自己的用户界面。这是一个[我们在其他项目](http://hackaday.com/2010/08/27/iphone-drum-machine-isnt-synthesized/)中见过的包，但是现在你可以知道它有多简单了。

该项目首先将 Arduino 与您想要控制的设备连接起来。上面的电路用几个晶体管连接成一个遥控器。现在 Arduino 可以模拟遥控器上的按钮，发送信号开灯或关灯。接下来，TouchOSC 用于智能手机——这里是 iPhone，但该套件也适用于 Android。在休息后的视频中，您可以观看一个快速的界面设计演示。按钮被拖动到存在，上传到手机，然后配置为通过网络控制您的设备。处理草图监听 OSC 命令，然后通过 USB 向 Arduino 发送指令。

[https://www.youtube.com/embed/bjMEoPwIA6w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bjMEoPwIA6w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
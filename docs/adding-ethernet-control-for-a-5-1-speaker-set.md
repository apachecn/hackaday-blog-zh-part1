# 为 5.1 扬声器添加以太网控制

> 原文：<https://hackaday.com/2011/05/16/adding-ethernet-control-for-a-5-1-speaker-set/>

![](img/f5c6175c393cc84e20545621a67a04b9.png "ethernet-controlled-5-1-surround-sound-speakers")

[HuB]的 5.1 环绕声扬声器在待机时消耗了大量电力，从超低音扬声器发出的 50 赫兹嗡嗡声和电源上燃烧的热散热器可以看出这一点。他想增加一种自动控制系统的方法，并提供断开电源的新功能。

第一部分并不太难，尽管他使用了迂回的原型法。他计划用扬声器上的红外接收器来控制它们。当时，[HuB]手头没有可以用来捕获 IR 协议的示波器，所以他最终使用 Audacity(开源音频编辑套件)来捕获连接到声卡输入的信号。他用这个来为原来遥控器上的所有八个按钮建立所需的定时和编码。

接下来，他拿起一块用 ATmega168 和 ENC28J60 以太网芯片制作的电路板。这使您可以通过互联网发送命令，然后将这些命令转换为适当的红外信号，以控制房间内的扬声器和其他一些设备。拼图的最后一块是将一个射频控制插座包装到项目中，让他在不使用时切断扬声器的电源。您可以在休息后看到嵌入的视频演示。

[https://www.youtube.com/embed/Coa74-hGV-Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Coa74-hGV-Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
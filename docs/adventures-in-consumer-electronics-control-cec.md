# 消费电子控制冒险

> 原文：<https://hackaday.com/2010/08/24/adventures-in-consumer-electronics-control-cec/>

![](img/a4eae9b3ead57418c8240c966fd19cae.png "cec-audio-hacking")

[瓦尔基里-MT]因为无法从电脑上控制 TrueHD 音频音量而感到沮丧。这是因为数字音频通过电缆传递到接收器，在那里进行音量调节。这意味着他的射频电脑遥控器不好，因为接收器使用的是红外遥控器。他开始寻找一种方法来解决这个问题，最终完成了消费电子控制(CEC)协议的工作。

[CEC 协议](http://en.wikipedia.org/wiki/CEC_(consumer_electronics_control)#CEC)是内置于 HDMI 标准中的单线串行总线。他解决的解决方案需要主板上的一个焊接连接以及上面看到的内部 USB 转换器模块。那个翻译盒，[叫做 RainShadow](http://rainshadowtech.com/default_files/HDMICECUSB.htm) ，是一个 PIC 18F87J50 控制板，它翻译来自 USB 连接的输入命令，并将它们作为 CEC 十六进制代码发送出去。写一点代码，[瓦尔基里-MT]就投入了业务。你可以在休息后的视频中看到，它不只是控制音频，他现在可以控制整个娱乐中心，包括打开电视和设置适当的输入。

[https://www.youtube.com/embed/kE47CxD5xrQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kE47CxD5xrQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
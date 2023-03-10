# 用可佩戴的乐器模拟行进乐队

> 原文：<https://hackaday.com/2011/05/13/emulating-a-marching-band-with-wearable-instruments/>

![](img/4be6ad29cf1f5da1bce99d0b4b64429d.png "glove-detail")

[Scott]是一名设计和技术硕士生，他刚刚设计出了虚拟行进乐队，这是一种可以戴在手上的虚拟乐队乐器。

从《少数派报告》和 [NES 力量手套](http://en.wikipedia.org/wiki/Power_Glove#In_popular_culture)中获得灵感，该系统在这一点上能够模拟 6 种乐器——小号、长号、大号、小军鼓、低音鼓和钹。手套本身从各种传感器读取数据[，并将其传递给 Arduino Uno，后者将串行数据发送回计算机。这些数据然后被一个](http://www.imaginarymarchingband.com/technology/)[串行 MIDI 转换器](http://www.spikenzielabs.com/SpikenzieLabs/Serial_MIDI.html)解析，然后可以通过一个采样器、合成器或者通过管道传输到你选择的音序器中进行回放。令人高兴的是，[斯科特]将为他的手套设计定制的 PCB，以减少空间和重量，并且他最终还将使他的项目开源。

[Scott]在 kickstarter 上为他的项目建了一个页面，到目前为止，他已经开始为这个项目筹集资金。休息之后来看看演示。

 [https://www.youtube.com/embed/xOe4y5fR8jo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xOe4y5fR8jo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
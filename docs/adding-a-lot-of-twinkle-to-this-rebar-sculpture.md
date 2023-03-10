# 给这个钢筋雕塑增添了许多光彩

> 原文：<https://hackaday.com/2012/03/07/adding-a-lot-of-twinkle-to-this-rebar-sculpture/>

闪亮的灯光有一种吸引注意力的方式，这正是毛伊岛制造商 hackerspace 的成员所追求的。上面的雕塑是源节的标志，一个燃烧的人启发在阿罗哈州的音乐聚会。为了今年的节日，他们疯狂地安装了由七块 Arduino 板控制的 12 米长的 RGB LED 灯条。

目标是将这个 12 英尺高的雕塑变成一个灯光互动的展示品。除了 led 以外，它还包括麦克风、电容传感器、蓝牙连接和压电扬声器。有一个 Arduino 来管理它们，另一个 Teensy 控制器来驱动控制箱中的 LCD 显示器，五个 Teensy 板来处理 LED 灯条。他们抓住【比尔·波特的】[易转移库](http://www.billporter.info/easytransfer-arduino-library/)来促进微控制器之间的通信(他的库正在变得流行，我们刚刚在周二看到他的 [mp3 shield 库用于另一个项目](http://hackaday.com/2012/03/06/your-theme-song-greets-you-at-the-front-door/))。

驱动 LED 动画的代码基于一些 Adafruit 示例。我们真的很享受在广告之后的片段中看到的摇旗效果。

[https://www.youtube.com/embed/g8b8IzOB4I0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/g8b8IzOB4I0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
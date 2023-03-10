# LiveLight 是一款专业制作的流光溢彩克隆产品

> 原文：<https://hackaday.com/2011/06/05/livelight-is-an-expertly-crafted-ambilight-clone/>

![](img/ea8ae8eeec4fab26c3159258e762e71c.png "livelight-ambilight-clone")

[SunWind] (Edit 2018:现在以[nerda sic]的身份出现)开发了自己版本的菲利普斯流光溢彩系统，他称之为 LiveLight。我们已经见过不少[这样的黑客](http://hackaday.com/2009/12/23/atmolight-clone-of-an-ambilight-clone/)，他们中的很多都是基于 Arduino 的[，大多数](http://hackaday.com/2011/03/03/arduino-based-ambient-lighting-improvements/)[使用 LED 条形照明](http://hackaday.com/2011/02/17/more-ambient-lighting-monitor-hacks/)。[nerda sic]也使用条形照明，但他的设计比我们见过的任何其他设计都要干净和精致。在我们看来，这甚至会受到最挑剔的影音爱好者的欢迎。

他找到了大小合适的 project box，并设法将所有东西都放在一个精心打磨的 PCB 上。外壳本身也经过打磨，以允许九个 RGB LED 灯条中的每一个都有迷你 USB B 连接器。但他并没有就此止步，外壳的顶部有铣成的标签，以帮助挂好所有东西。

ATmega32 根据计算机输入的数据对 LED 灯条进行寻址。一个板载 FTDI 芯片增加了 USB 连接,[ nerda sic]使用黑客技术重写了该芯片上的 EEPROM，使其以“LiveLight USB 接口”的名称枚举。一个名为 [Boblight](http://blogger.xs4all.nl/loosen/articles/408184.aspx) 的程序从当前播放的视频中收集数据。您可以在休息后嵌入的视频中看到最终项目。

[https://www.youtube.com/embed/ILArJQlQPN0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ILArJQlQPN0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[感谢 Lauri 和 Jussi]

(2018 编辑:旧论坛帖子，详细介绍了这个项目的发展，可以在这里找到[。)](http://www.ruuvipenkki.fi/foorumi/viewtopic.php?f=15)
# 廉价的唱机

> 原文：<https://hackaday.com/2010/05/15/kaossilator-on-the-cheap/>

![](img/537f7f69b1864988a94ef9d30fc91f22.png "KORG+KAOSSILATOR")

我们最近偶然发现了一种方法，可以将普通的笔记本电脑变成穷人的助唱机。使用笔记本电脑的触摸板、一些 [PureData](http://en.wikipedia.org/wiki/Pure_Data) 软件、 [Touchpad2MIDI](http://www.livelab.dk/touchpad2midi.php) 和几个定制补丁，[zenpho]已经让每个人都能创作出孩子们现在听的疯狂电子音乐。

但那是什么？你买不起一整台笔记本电脑，需要在更紧的预算下实现这一目标？哦，[我们支持你](http://www.instructables.com/id/The-5-Karduinoss-pad/)。仅仅使用触控板和 Arduino，[Bastian]就创建了一个基本的 PS2 到 Arduino 到 USB 的链接，它可以被你的[最爱的](http://en.wikipedia.org/wiki/C%2B%2B) [语言](http://www.python.org/)的[选择](http://en.wikipedia.org/wiki/X86_assembly)解析成一个工作的 MIDI 接口。对于所有懒惰的黑客来说，这是一个好消息，他正计划用一个 Teensy 来替换 Arduino，并制作一个真正的 USB 到 MIDI 接口。
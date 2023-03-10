# 用 Common Lisp 生成 g 代码

> 原文：<https://hackaday.com/2009/02/01/generating-g-code-with-common-lisp/>

![gcode](img/f996fb8bea519cd1e723dca060eae654.png "gcode")

Ruin & Wesen 是一家两人店，专门制作音乐装备。作为他们最近 MIDI 命令开发的一部分，他们进入了外壳制造领域。他们购买了一台迷你数控铣床来切割铝外壳。对提供的软件选项不满意【伪森】决定[编写自己的 g 代码生成器](http://ruinwesen.com/blog?id=387 "Ruin & Wesen")。 [G 代码](http://en.wikipedia.org/wiki/G-code "G-code - Wikipedia, the free encyclopedia")是数控的一部分，用来命令数控机床。他用自己最熟悉的语言实现了自己的解释器:Common Lisp(如果你注意到[网站的后端](http://bknr.net/html/home.html "BKNR - home")，这并不奇怪)。这篇文章涵盖了使用的设计哲学和出现的一些问题。我们期待着未来的版本，因为解释器可以使用 processing.org 草图生成铣削代码，并直接从 Eagle 切割 PCB。

你可能还记得 Ruin & Wesen 分享他们的 [Eagle 布局视频](http://ruinwesen.com/blog?id=181 "Ruin & Wesen")。

[感谢 [fbz](http://fabienne.us/ "fabienne.us")
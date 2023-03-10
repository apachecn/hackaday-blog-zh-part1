# CadSoft 的 EAGLE 6 发布测试版并打包好东西

> 原文：<https://hackaday.com/2011/11/05/cadsofts-eagle-6-hits-beta-and-packs-goodies/>

![](img/16466ff094ab50c339473797b3771eac.png "minyboost-eagle-xml")

[流行的原理图和 PCB 布局软件 EAGLE](http://www.cadsoftusa.com/betatest/) 的第 6 版目前正在测试中。最显著的变化是[到 XML 文件格式的迁移](http://hackaday.com/2010/10/14/cadsoft-eagle-migrating-to-xml/)，我们上个月已经讨论过了。

[PT]没有浪费任何时间去接触这个软件，并且[对它进行了彻底的测试](http://www.adafruit.com/blog/2011/11/04/eagle-v6-beta-xml-export-some-example-files-and-screenshots/)。上图显示了一个 MintyBoost 的文件。这种分辨率是不可能的，但它确实在下面的窗口中吐出了人类可读的(也许)XML，而不是他们过去使用的“不侵入”二进制文件。

今天早些时候，在开发一个功能时，我们不得不跳到另一台安装了 EAGLE 的计算机上，以便查看一个. SCH 文件。我们想知道是否有人会推出一个渲染包，可以解析新格式，并吐出一个快速的 PNG？至少，我们希望看到一些有用的部件更换或引脚交换技巧。当改变一些存储值时，应该不难发现发生了什么。你有什么想法可以通过手工编辑来实现吗？

哦，我们差点忘了！这样做的最大好处是增加了版本控制的兼容性，因为像 git 这样的程序将能够对文件执行不同的功能。
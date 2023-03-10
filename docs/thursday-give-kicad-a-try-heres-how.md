# 给 KiCAD 一个机会。以下是方法

> 原文：<https://hackaday.com/2011/03/10/thursday-give-kicad-a-try-heres-how/>

![](img/92f4d4b5664c795ce6ba9ca690654f02.png "KiCAD-tutorial")

到目前为止，我们一直使用 Eagle CAD 作为独家 PCB 设计和原理图布局工具。但是由于他的 KiCAD 教程，布莱恩激励我们尝试不同的东西。

KiCAD 是一个开源的印刷电路板设计工具。因为我们喜欢在 Hackaday 上展示 Linux，所以得到它很容易:

```
 sudo apt-get install kicad
```

Ubuntu 10.04 仓库中的版本有点旧，但似乎工作得很好。[Brian]直接进入我们在 Eagle 上最可怕的任务之一，设计你自己的零件。他知道一个很好的在线工具，用于自动生成 KiCAD 器件，并介绍了构建电压调节器并将其导入到您的个人库中的过程，然后开始为试验板 PSU 设计电源原理图。本课将继续介绍电路板层，以及用于为 PCB fab house 导出数据的流程。我们认为，如果你已经熟悉使用不同软件包的 PCB 布局，本教程会很好地工作，但如果这是你的第一次，它会移动得有点快。

KiCAD 看起来是一个不错的工具，这些年来我们已经从许多支持者的评论中听到了。期待我们的下一个 PCB 设计出现在 KiCAD 上，因为我们只需要在做出判断之前使用一段时间。
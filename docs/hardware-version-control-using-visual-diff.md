# 使用视觉差异的硬件版本控制

> 原文：<https://hackaday.com/2011/10/14/hardware-version-control-using-visual-diff/>

![](img/da5e3405487dccd26892c69f3673a3c9.png "hardware-version-control-visual-diff")

随着开源硬件运动的发展，与 Git 等用于软件项目的灵活框架相比，在硬件上协同工作的工具显然处于黑暗时代。我们最近已经阅读了相当多的这方面的内容，但是为 PCB 布局生成[视觉差异的想法是我们见过的更好的提议之一。](http://www.evilmadscientist.com/article.php/visdiff)

当然，当涉及到版本控制时，最大的区别是软件是文本，而硬件是图形的，只由计算机使用的文本来表示。很容易使用' diff '命令来显示什么文本在外面，什么文本在里面，但这并不能转换成原理图。[Windell]正在使用命令行实用程序生成一个示意图，该示意图的颜色会发生不同的变化，以便于视觉检测。这意味着将之前和之后的 schematics 导出为 PDF 文件或图像，然后使用 ImageMagick 对其进行处理。他还指出，有一个名为 [DiffPDF](http://www.qtrac.eu/diffpdf.html) 的包可以让你自动比较 PDF 文件的差异。

看看他在文章中说了些什么，并确保你深入了解他建议你可以提供帮助的方式。我们一致认为，将 visual diff 功能整合到用于硬件设计的开源软件包中，并将其集成到版本控制系统中应该不难。只是需要一些时间让这个概念扩散开来。
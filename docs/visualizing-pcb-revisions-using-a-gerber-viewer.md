# 使用 Gerber Viewer 可视化 PCB 版本

> 原文：<https://hackaday.com/2011/08/02/visualizing-pcb-revisions-using-a-gerber-viewer/>

![gerber_schematic_highlighting](img/239d3dff304689d2c2d4fb8e68e10a35.png "gerber_schematic_highlighting")

我们都知道鹰也有它的缺点。Instructables 用户[westfw]特别恼火的是，虽然 Eagle 保留了多达 10 个电路板修订版的副本，但如果不借助手动重命名，它就无法打开这些文件。更让他沮丧的是，你不能为了比较布局而用 Eagle 同时查看两个文件。这使得寻找变化变得相当乏味，所以他开始寻找更好的做事方法。

在使用他最喜欢的[开源 gerber viewer gerbv](http://gerbv.sourceforge.net/) 时，他注意到该应用程序允许他加载同一图层的多个副本，将 PCB 的颜色混合在一起。意识到通过一些聪明的颜色选择，他可以使用 gerbv 自动突出布局差异，他开始自动化这个过程。

最终的脚本可以在任何风格的*nix 上运行，并且在 cygwin 下的 Windows 中也可以很好地运行。该脚本通读 Eagle 备份文件，对它们进行重命名并调整颜色，以便当执行 xor 时，它们在 gerbv 中显示为亮红色区域。如果你碰巧做了很多 PCB 设计，这是一个简单而方便的工具。
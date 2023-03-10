# Kicad 符号生成脚本显示承诺

> 原文：<https://hackaday.com/2012/02/17/kicad-symbol-generating-script-shows-promise/>

![](img/f5aa4f082537ef48cdf90bf3491c3dfd.png "python-based-kicad-symbol-generator")

Kicad 是一款出色的 PCB 布局工具。我们认为使用 Kicad 创建零件在许多方面比使用 Eagle 更容易，但使用一些快捷方式也无妨。这是一种快速将零件放入原理图编辑器的新方法。这是一个从 XML 输入文件生成符号的 Python 脚本。您创建一个 XML 文件，其中列出了您的器件上的所有引脚及其功能。Python 脚本会将其格式化为一个库文件，可以由 Kicad 导入。

由于这个过程中的步骤太多，所以有点笨拙。但是可以使用电子表格程序中生成的 CSV 文件来创建脚本所需的 XML。我们自己已经使用了在线组件构建器，并且意识到大规模 pin 分配的可能性，而不是像 web 界面那样使用每个 pin 的下拉框。有一次，我们在命名过程中用了 20 个图钉，不小心刷新了页面…唉！

代码可以在他们的 git 库中找到，带有 XML 格式的描述，以及概述组件构建过程的 wiki 教程。在你尝试之后，我们很乐意在评论中听到你的想法。
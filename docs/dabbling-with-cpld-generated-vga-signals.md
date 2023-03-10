# 尝试用 CPLD 产生 VGA 信号

> 原文：<https://hackaday.com/2011/05/05/dabbling-with-cpld-generated-vga-signals/>

![](img/bc73bd4118f0268ab546aa55aab6ffed.png "vga-output-from-a-cpld")

似乎所有酷孩子都在零件箱里留下 8 位爱好微控制器，玩更高级的零件，如复杂的可编程逻辑器件。[Chris]也不例外，他开始使用一种结实的半导体来产生自己的 VGA 信号。

他似乎在他的帖子中使用了可互换的首字母缩写词 CPDL 和 FPGA，但根据零件列表，该设置使用了 Altera EPM7128SLC84-7N CPLD。为了生成 VGA 信号，他需要一种方法来将来自芯片的数字信号转换为视频标准中要求的模拟值。他选择使用电阻网络为 RGB 颜色值构建一个数模转换器，他使用 [PSpice](http://en.wikipedia.org/wiki/PSpice) 进行计算。拼图中的另一块是为 CPLD 提供时钟的 25.175 MHz 振荡器。正如你在休息后看到的，他的绕线原型完全按照设计工作。示例代码生成了上面看到的彩虹条，或者一个让人想起 DVD 播放器屏幕保护程序的弹跳框演示。

想了解更多关于 CPLDs 编程的知识吗？不久前，我们做了一个主题为的辅导。

[https://www.youtube.com/embed/Tc572ygU70o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Tc572ygU70o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
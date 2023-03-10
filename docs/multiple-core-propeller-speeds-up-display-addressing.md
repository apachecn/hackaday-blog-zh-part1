# 多核推进器加速显示寻址

> 原文：<https://hackaday.com/2010/10/21/multiple-core-propeller-speeds-up-display-addressing/>

Th

如果你想知道八核螺旋桨处理器能为你做什么，[Tom]找到了一个答案。他正在使用[多核来单独寻址串行显示器](http://mrt.id.au/index.php/2010/10/pinball-led-display-almost-done/)。他有六个显示模块，每个模块包含六个 8×8 LED 模块。这使得总共有 2304 个 led，因为它们是通过级联串行数据寻址的，这意味着有 2304 个字节被推送到显示器。如果你选择这种交流方式，你将会很慢。

这就是多核派上用场的地方。他没有在六个模块之间级联数据，而是给每个模块分配了不同的内核。现在，他可以同时处理六个显示器，将串行数据从每帧 2304 位减少到每帧 384 位。正如你在休息后的视频中看到的，以之前的六倍速度更新显示会产生奇妙的结果。

现在，如果你使用的处理器有 40 个这样的多核螺旋桨芯片，会怎么样？

这确实让我们想知道，在单核处理器上不能做同样的事情吗？八位器件需要一个周期来设置单个端口上的所有八位。那么，为什么不在同一个端口的六个位上连接六个串行连接呢？请在评论中加入你的想法。

[https://www.youtube.com/embed/o9Q9hVrrLS4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/o9Q9hVrrLS4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
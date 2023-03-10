# 俄罗斯方块代码理论解释

> 原文：<https://hackaday.com/2010/06/20/tetris-code-theory-explained/>

[Graham]设计了这个基于图片的俄罗斯方块游戏。硬件相当不错，但我们喜欢他对他使用的图形算法的解释。有了[从头开始编码的俄罗斯方块](http://hackaday.com/2010/01/14/avr-tetris/)，我们明白解释程序如何工作是多么困难。跟踪已经在棋盘上的棋子以及移动的棋子，确保旋转不会与另一个棋子发生碰撞或越界，以及寻找已完成的线，所有这些加起来都是一个令人头疼的问题。

[Graham]处理旋转的方法包括选择一个旋转点，测量它如何影响块中的每个像素，然后检查这些像素的重叠。这可能需要读几遍，但他已经做了出色的工作，使它可以理解。休息后有一个演示，顶部的链接会带你去看他关于俄罗斯方块的论文。[https://www.youtube.com/embed/WKE26TWLdaI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WKE26TWLdaI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# 一种光跟踪乒乓球游戏

> 原文：<https://hackaday.com/2011/09/13/a-light-following-pong-game/>

[![](img/b72ac49767e9e4be8ef78b57a41fc7f8.png "light_pong")](http://hackaday.com/2011/09/13/a-light-following-pong-game/light_pong/)

虽然并不是每个人都有能力像马塞洛一样制作一款黑客攻击的乒乓游戏，但更少有人有能力或创造力像他那样精心设计黑客攻击。他的游戏的基本前提是一个在带有 8×8 led 矩阵的试验板上玩的 pong 版本。控制器是这个黑客与众不同的地方。小手电筒被用来控制屏幕上的(LED 矩阵)拨片，而不是使用拨片控制器或普通开关。这是使用一系列光敏电阻和 PIC 处理器完成的。

尽管这本身很有创意，但[Marcelo]决定用 Flash 制作一个程序，在电脑上显示这个动作。通信是串行完成的，C#用于翻译一切，因为 Flash 本身不支持串行连接。

另一项创新是，每侧连接两个 led，通过脉宽调制供电。当一个玩家将要输的时候，灯光变暗。休息之后看看[马塞洛]的乒乓球比赛！

[https://www.youtube.com/embed/Jny5ZGEzBtw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Jny5ZGEzBtw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
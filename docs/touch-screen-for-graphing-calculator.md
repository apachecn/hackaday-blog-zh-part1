# 用于图形计算器的触摸屏

> 原文：<https://hackaday.com/2010/04/03/touch-screen-for-graphing-calculator/>

[https://www.youtube.com/embed/pyWIJFLbJZ0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pyWIJFLbJZ0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[欧文]在他的 TI-84 图形计算器上加了一个触摸屏。脏的部分是他写的把 linkport 当 UART 用的 z80 汇编代码(汇编总是让我们觉得反胃)。一旦成功，他就用 Arduino 实现了一些命令，然后连接了一个任天堂 ds 触摸屏。现在他有了这个概念验证视频，他在屏幕上绘图，输入由 Arduino 解释，命令通过 UART 发送，计算器程序在屏幕上绘图。[当你不得不竭尽全力让它工作起来的时候，给某个东西加上触摸屏](http://hackaday.com/2009/12/18/make-an-apple-tablet-before-apple-does/)会给人留下深刻的印象。干得好！
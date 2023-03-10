# 微控制器多任务处理的 c 位域结构

> 原文：<https://hackaday.com/2011/11/22/c-bit-field-structures-for-microcontroller-multitasking/>

![](img/ede38ab0e23447faeafbe0c2dc642d65.png "bit-field-tutorial")

所以你越来越擅长微控制器编程，现在你想同时做几件事？你应该知道，微控制器一次只能处理一件事。但是如果你聪明地使用你的编码，你可以实现一些行为就像几件事情同时发生一样的东西。最常见的方法是使用中断设置一个标志，然后使用主循环检查该标志。[S1axter]发布了一个关于这个主题的教程，其中[他使用位字段结构来帮助简化](http://www.mybitbox.com/2011/11/video-blog-time-and-bitfield-structs-in-micros/)时间敏感事件。

我们认为[S1axter]非常出色地清晰、快速地解释了这个中等难度的主题。在休息后的视频中，他开始解释[什么是位域](http://en.wikipedia.org/wiki/C_syntax#Bit_fields)以及如何定义它。基本上，你使用一个 C 结构来跟踪一个标志，只需要一点存储空间。这样，标志要么被设置，要么不被设置。我们建议您仔细注意他是如何将结构声明为 volatile 的，这样当您自己尝试时就不会出现意外的行为。

[https://www.youtube.com/embed/Voqg4Mx2Sg8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Voqg4Mx2Sg8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
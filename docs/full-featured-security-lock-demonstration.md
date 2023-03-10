# 全功能安全锁演示

> 原文：<https://hackaday.com/2011/11/26/full-featured-security-lock-demonstration/>

![](img/3c2e2ead18b9a28964434e5f645be724.png "code-lock-demonstartion")

[Arshad Pathan]让我们了解一下他的最新项目，[一种可以适应许多不同情况的模块化密码锁](http://ars2k6.blogspot.com/2011/11/electronic-security-code-lock-system.html)。

用户界面由一个字符 LCD 屏幕和一个 3×4 键盘组成。在这个例子中,[Arshad]使用步进电机作为锁定机构。当电路板第一次通电时，它在一个方向上运行步进器，直到接收到来自限位开关的输入。通过这种方式，微控制器自我校准以确保锁处于已知位置。从那里，它等待用户输入。按*键可以随时锁定未锁定的门。解锁需要输入正确的密码。密码可以通过输入 9999(提示时输入旧密码)来更改。

在休息后的视频中，Arshad 很好地展示了他编程的各种模式。这是独立的，但我们总是想知道更多的细节，所以我们问[Arshad]是否愿意分享原理图和源代码。如果我们收到他的回复，我们会更新这篇文章。

**更新:** [Arshad]发来了几张示意图，休息后可以找到。

[https://www.youtube.com/embed/pYyQfFyrrY8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pYyQfFyrrY8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

## 原理图:

[![](img/bde58864085462e62b4d60874607ba23.png "Lock_Atmega16_v.1.1_1") ](http://hackaday.com/wp-content/uploads/2011/11/lock_atmega16_v-1-1_1.jpg) [ ![](img/7a0160c5412cd7ea7becb62792d19da5.png "Lock_Atmega16_v.1.1_2")](http://hackaday.com/wp-content/uploads/2011/11/lock_atmega16_v-1-1_2.jpg)
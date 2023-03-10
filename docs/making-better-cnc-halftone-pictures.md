# 制作更好的 CNC 半色调图片

> 原文：<https://hackaday.com/2011/09/14/making-better-cnc-halftone-pictures/>

![](img/c3f4158bad8fcda26a5b5102b119ed33.png "small")

【杰森】正在[摆弄数控机床](http://jasondorie.com/page_cnc.html)并且想出了[他自己的](http://hackaday.com/wp-content/uploads/2011/09/full.png)半色调数控图片，这可能比我们之前看到的尝试有所改进。

【杰森】的灵感来自于[这个黑客一天发布的](http://hackaday.com/2011/07/28/creating-halftone-pictures-with-a-cnc-machine/)像默认的 Photoshop 插件或者[光栅化器](http://homokaasu.org/rasterbator/)一样转换图像半色调。结果非常好，但是一旦 JoesCNC 论坛上的一个用户问他如何才能让[制造出这些‘幻影’CNC 图片面板](http://www.interlam-design.com/Mirage_ProductList.cfm)，【杰森】知道他必须做什么。

他立刻认出了生成幻影面板的算法是基于格雷-斯科特反应扩散算法的。使用这种算法，深色区域看起来有点像指纹，这意味着 CNC 刳刨机的工具头可以在 X 和 Y 轴上切割，而不是使用传统半色调的简单孔图案。经过一点编码后，[Jason]有了一个应用程序，可以将图像转换为反应扩散半色调，然后可以转换为矢量并发送到路由器。

这是一个非常整洁的建筑，我们想象[杰森]的照片会比商业展板花费少一点。休息后，请观看视频，了解制作过程。

[https://www.youtube.com/embed/xoJDTPRqI6o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xoJDTPRqI6o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
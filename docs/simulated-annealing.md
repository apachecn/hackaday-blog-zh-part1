# 模拟退火

> 原文：<https://hackaday.com/2008/12/10/simulated-annealing/>

![annealing](img/ac238b3ec0f446346b1c99434676df4a.png "annealing")

这是我们之前关于基因编程的帖子的更新。改变的 Qualia 已经[发布了一个【罗恩·阿尔辛】想法的新实现](http://alteredqualia.com/visualization/evolve/ "Image evolution")。它从 50 个多边形开始，然后在每个优化步骤中随机改变一个参数。如果更改导致与目标图像的差异减少，它将被保留为新的最佳 DNA。这种搜索方法类似于[模拟退火](http://en.wikipedia.org/wiki/Simulated_Annealing "Simulated annealing - Wikipedia, the free encyclopedia")。上图是 35900 个可能的突变中 1500 个的结果。该实现允许您选择任何图像，但是图像越小意味着适合度计算越快。它是使用 [< canvas >](http://en.wikipedia.org/wiki/Canvas_(HTML_element) "Canvas (HTML element) - Wikipedia, the free encyclopedia") 环境用 JavaScript 编写的。使用[更新的浏览器版本](http://hackaday.com/2008/10/18/chrome-and-firefox-showing-javascript-improvements/ "Chrome and Firefox showing JavaScript improvements  - Hack a Day")，你肯定会获得更好的性能。

[原始图片由 R·史蒂文斯提供]

[via [蜡质](http://waxy.org/links "Links Miniblog")
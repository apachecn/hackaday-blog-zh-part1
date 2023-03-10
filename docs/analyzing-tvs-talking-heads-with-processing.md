# 电视谈话节目的加工分析

> 原文：<https://hackaday.com/2011/07/19/analyzing-tvs-talking-heads-with-processing/>

Nootropic Design 的[Michael]来信分享了他用公司销售的一种产品做的一个有趣的项目。这个小玩意是他们为 Arduino 设计的“视频实验者”防护罩。它通常用于通过叠加等方式处理复合视频流，但也可以用作视频分析器。

当用于视频分析时，该板允许您解码隐藏字幕数据，这正是[Michael]在这里所做的。他认为从各种节目和广告中搜集隐藏字幕信息来做一点内容分析会很有趣。

他使用 Arduino 上的处理草图，从有线电视盒中读取隐藏字幕，记录广播中提到的每个词。随着节目的进行，他的草图动态构建了一个云，显示视频中最常用的单词。

他得到的结果非常有趣，尤其是当他观看晚间新闻或其他有特定目标受众的广播时。我们认为在政治辩论中或者在好莱坞颁奖典礼上运行这个应用程序会很酷，可以发现哪一组演讲者是最乏味的。

如果你有兴趣了解更多关于解码过程的信息，[Michael]整理了一份关于如何从视频流中提取隐藏字幕数据的详细说明。对于那些只想看看解码器工作的人，请继续阅读，观看快速视频演示。

[https://www.youtube.com/embed/s_2zWhPJvW8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/s_2zWhPJvW8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
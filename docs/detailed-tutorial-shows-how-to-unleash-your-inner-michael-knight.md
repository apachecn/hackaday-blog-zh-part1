# 详细的教程展示了如何释放你的内心【迈克尔·奈特】

> 原文：<https://hackaday.com/2011/10/28/detailed-tutorial-shows-how-to-unleash-your-inner-michael-knight/>

![developing_a_larson_scanner](img/7802eab723decac917bcd447b59e8786.png "developing_a_larson_scanner")

我们自己的[Mike Szczys]最近坐下来整理了一个关于构建 Larson 扫描仪的很棒的教程。无处不在的电路通常是初露头角的黑客名单上最先建设的几个项目之一，因为[它们实在太有趣了。](http://hackaday.com/tag/larson-scanner/)

简单版本的扫描仪来回扫描发光二极管，它们之间没有任何过渡。《霹雳游侠》和《太空堡垒卡拉狄加》中我们最熟悉的配置稍微复杂一点，在扫描前缘后面有一条逐渐消失的光尾。[Mike]注意到，这种衰减通常是通过使用电容器来实现的，当动画扫过 LED 阵列时，电容器会导致光线逐渐衰减。他决定在他的电路中采用不同的路线，而是依靠 led 的 PWM 控制。

Mike 用 ATmega168，一些电阻，当然还有一排发光二极管组装了一个简单的电路。利用中断和 PWM，他能够准确地再现标志性的光扫描，而不使用任何电容器。他的设计除了减少元件数量之外，还有一个很大的好处是，他可以通过一些小的代码调整来轻松调整扫描速度和衰减属性。

一定要看看他的博客，在那里他分享了他的代码，一些电路图，以及更多关于他的扫描仪是如何建造的细节。与此同时，看看下面的视频，看看[迈克]的工作成果。

[https://www.youtube.com/embed/E2wsR8hgIjI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/E2wsR8hgIjI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
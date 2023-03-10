# 电表数据采集的另一种方法

> 原文：<https://hackaday.com/2010/09/21/another-approach-to-power-meter-data-harvesting/>

![](img/058542d0f372d5959d28f5eb87d58bd1.png "more-google-powermeter")

[Dodgy]写信来谈论他的电表数据收集计划。这使用了与我们周末看到的[黑客相同的硬件](http://hackaday.com/2010/09/18/smart-power-meter-interface-for-the-linux-crowd/)，但是【道奇的】实现是不同的。它分为两部分，第一部分是用 C 编写的 web 服务器，它收集数据并使其在网络上的某个地址可用，第二部分是用 Perl 编写的，用于格式化数据并上传到 Google PowerMeter。

C 程序在一个可配置的端口上提供数据，默认端口为 3090。通过加载 [http://127.0.0.1:3090](http://127.0.0.1:3090) ，可以在一行代码中访问所有的数据，或者单独访问/watts、/time 或/tempr 等子目录。从那里你可以对数据做你想做的事情。[道奇的]套件的第二部分是[，一个轮询 C 服务器并将数据发送到你的谷歌账户的 Perl 脚本。](http://www.linux-depot.com/?p=projects&s=googlepower)

我们感兴趣的一件事是他的评论，你应该能够为嵌入式设备编译服务器端 C 代码。这将是一个很好的节能，能够定期上传数据，而不是一台电脑不断运行。
# 使用并行端口作为逻辑嗅探器

> 原文：<https://hackaday.com/2012/03/02/using-the-parallel-port-as-a-logic-sniffer/>

![](img/7514282c86844cf52775311fca952c19.png "parallel-port-as-logic-sniffer")

[Fernando]来信分享了他对构建逻辑分析仪的看法。他正在[使用并行端口捕获数据](http://www.alfersoft.com.ar/blog/2012/02/23/parallel-port-sniffer-for-linux/)并将其输入到您选择的显示软件中。

该方法依赖于改变并行端口工作方式的自定义内核。他编译的内核包含了一种方法，可以截取来自硬件的信号，将数据传递给/dev/parport*，同时也向/dev/parportsnif*发送一份副本。它还创建一个日志文件，该文件采用 [OpenBench 逻辑嗅探器](http://hackaday.com/2010/02/28/open-source-logic-analyzer-2/)格式，便于与各种显示软件一起使用。

当然，这在 Linux 系统中最容易使用，但也可以在 Windows 下作为虚拟机运行。我们也计划在 Linux 中使用虚拟机，因为这是一个定制的内核，可能只会偶尔使用。
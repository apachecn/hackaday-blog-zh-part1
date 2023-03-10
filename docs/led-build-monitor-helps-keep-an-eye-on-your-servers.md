# LED 构建监视器有助于监控您的服务器

> 原文：<https://hackaday.com/2011/04/12/led-build-monitor-helps-keep-an-eye-on-your-servers/>

在他的工作中，Hackaday reader [Pedantite]经常需要全天监控几个持续集成服务器的构建状态。一天下午，他有了在办公室安装一组停车灯的想法，以便监控服务器的状态，但他将其作为一个“如果……会不会很酷”的项目存档。

过了一段时间后，他再次被这个想法困扰，决定[建造一个物理设备来显示他的建造过程的状态](http://bytecruft.blogspot.com/2011/04/build-system-status-monitor.html)。这一次，他进行了小规模的头脑风暴，结果就是你在上面看到的“起诉”。

他制作了一个简单的 LED 板，由四排四个 LED 组成，用来显示制作过程。根据项目的当前构件状态以及上一个构件的结果，不同的 led 会亮起。该板使用 ATmega88，并使用专为 AVR 微控制器设计的虚拟 USB 包与编译器看门狗应用程序接口。

最终的结果是一个简单而有用的状态板,“正常工作”。他目前似乎没有在他的网站上发布代码或图表，但我们很确定他会应要求分享它们。

如果你对[Pedantite]的工作感兴趣，看看他的[“美好时光”父母计时器](http://hackaday.com/2011/04/06/keep-fun-in-check-with-a-parental-count-down-timer/)，我们上周特别报道过。
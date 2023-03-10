# 初学者概念:所有关于 AVR 中断

> 原文：<https://hackaday.com/2010/09/27/beginner-concepts-all-about-avr-interrupts/>

![](img/24ab084e7c538888265f57019461dc74.png "avr-interrupts")

微控制器中断是我们嵌入式编程武库中的重要工具之一。它们让芯片监听特定的事件，一旦检测到，它们就停止正在做的事情，运行一组独立的代码，称为中断服务程序。我们已经看到了关于这个主题的两个相当新的教程，如果你还不是这个主题的大师，你应该看看。一个是[一个关于 ATmega168 外部中断](http://www.protostack.com/blog/2010/09/external-interrupts-on-an-atmega168/)的 ProtoShack 教程，另一个是[一个新手指南 AVR 中断](http://www.avrfreaks.net/index.php?name=PNphpBB2&file=viewtopic&t=89843)由【迪恩相机】(我们是他的教程的粉丝已经有一段时间了)。两者都涵盖了一系列主题，从什么是中断，到避免易变数据类型的常见问题和编译器优化警告。

你能用中断做什么？外部中断可以用来唤醒像[这种 LED 灯台](http://hackaday.com/2008/11/13/improved-led-menorah/)从睡眠模式的项目。中断可用于监控定时器的某个值或溢出，用于产生[脉宽调制](http://hackaday.com/2010/09/21/discussing-pulse-width-modulation/)信号。TI Launchpad 在像[这种从 AVR 芯片](http://hackaday.com/2010/08/13/porting-code-to-msp430/)移植过来的代码的项目中使用间隔定时器中断进行按钮去抖动。如果您想比较两者的不同之处，可以使用这两者的源代码。

中断是强大的。学习它们，爱它们，使用它们。
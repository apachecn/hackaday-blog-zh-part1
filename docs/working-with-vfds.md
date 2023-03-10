# 使用 VFD

> 原文：<https://hackaday.com/2008/12/25/working-with-vfds/>

![vfd](img/4325dea122ef083b264525162c756103.png "vfd")

我们喜欢旧的显示技术，比如[谢妮管](http://hackaday.com/?s=nixie "Hack a Day")，但是它们通常很难使用，因为它们需要比数字逻辑更高的电压。真空荧光显示器( [VFD](http://en.wikipedia.org/wiki/Vacuum_fluorescent_display "Vacuum fluorescent display - Wikipedia, the free encyclopedia") 就属于这一类。虽然不一定“古老”，但它们正变得远不如液晶显示器普遍。VFD 的主要优点是它实际上直接产生光；它不需要背光。你会在各种播放器和电器上发现这些显示器:CD、DVD、VCR、微波炉、炉子、汽车音响等等。

[Sprite_tm]已经取消了一些 VFD，但最近[以新的兴趣](http://spritesmods.com/?art=vfdcontroller&page=1 "Sprites mods - Simple VFD-controller - A whatnow?")重新访问了它们。他首先测试驱动显示器需要什么样的电压。灯丝需要 3V 外加 15V 来驱动栅极。有 VFD 控制器芯片可用，但他想用他手头的东西来工作。他有使用更老的 [40xx](http://en.wikipedia.org/wiki/4000_series "4000 series - Wikipedia, the free encyclopedia") 系列逻辑的经验，这种逻辑可以由比 5V [74xx](http://en.wikipedia.org/wiki/7400_series "7400 series - Wikipedia, the free encyclopedia") 高得多的电压供电。他的最终原理图有三个 4094 串行到并行芯片和一个 ATtiny2313 控制器。5V 电源通过二极管降至 3V 以驱动灯丝，而升压转换器将 4094 的电压升至 15V 以切换各段。虽然代码是特定于这个显示器的，但是它将是开始您自己的项目的一个很好的地方。
# PC 到 R/C 接口

> 原文：<https://hackaday.com/2006/02/27/pc-to-rc-interface/>

![futaba](img/18f1c158522d4c520a6bc857a9be769d.png)

Risto K？s [PC 到 R/C 接口](http://www.mh.ttu.ee/risto/rc/electronics/pc2rcv2.htm)让您连接到双叶无线电发射机。你可以用这个设备直接控制你的遥控项目:预先写好的轨迹，用户调用的宏，或者直接控制电脑操纵杆。他造了两个版本。最初的版本使用多个 D 锁存器。第二个版本试图减少组件的数量。它在微控制器软件中使用中断，而不是锁存器。这通常会导致大量抖动，但 Risto 在汇编中实现了中断。控制器可以处理多达 16 个通道。LCD 显示最后的脉冲宽度和通道。

[感谢[将](http://biobug.org/)

*   [永久链接](http://www.mh.ttu.ee/risto/rc/electronics/pc2rcv2.htm)
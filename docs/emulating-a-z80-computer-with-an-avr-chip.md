# 用 AVR 芯片模拟 Z80 计算机

> 原文：<https://hackaday.com/2010/04/27/emulating-a-z80-computer-with-an-avr-chip/>

![](img/7e685f07bfe9661c7fe208bc4e403755.png "z80-emulation-using-AVR")

[Sprite_tm]展示了他的组装技能，并使用 AVRatmega 88 成功模拟了 Z80 计算机。他使用 SD 卡代替软盘和 128 KB DRAM 芯片来处理模拟机器的内存。FT232 板为他提供了终端访问，用于输入和显示。如你所见，硬件比最初的的[要简单得多。他用复杂的固件来弥补这一点。最终，在他遵循](http://hackaday.com/2009/09/07/proto-board-z80-computer/) [Z80 Propeller 项目的想法](http://smarthome.viviti.com/propeller)将指令分成不同的模块并使用查找表来访问它们之后，仿真的内核占用了大约 2 KB 的编程空间。
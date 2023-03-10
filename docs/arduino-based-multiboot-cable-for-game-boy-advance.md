# 用于 Game Boy Advance 的基于 Arduino 的多重引导电缆

> 原文：<https://hackaday.com/2010/03/18/arduino-based-multiboot-cable-for-game-boy-advance/>

![](img/c02fa6e1e2dd0230e235e7dbc8c229ca.png "arduino-gba-cable")

[史蒂夫]想做一些 ARM 开发，并把他的目光放在 Game Boy Advance 上，作为一个开发包。为了把他的代码放到设备上，他制作了一条基于 Arduino 的通信电缆。由于 GBA 使用一种特殊的 16 位串行通信协议，因此有必要使用微控制器。这种电缆是几年前由[Matt Evans]开发的基于[8051 的电缆](http://axio.ms/projects/GBA/)的改进。[Steve 的]通过为 Arduino 移植 8051 汇编程序使其工作，但我们建议在他的硬件设置中添加一个电平转换器，以从 Arduino 的 5v 逻辑下降到 GBA 期望的 3.3v 逻辑。

他没有编接线图，但在代码注释中[Steve 的]按如下方式布置了连接:

```
Arduino 8 to GBA SO
Arduino 9 to GBA SI
Arduino 10 to GBA SD
Arduino 11 to GBA SC
```

就这样，按照他的源代码包中的自述文件，您就踏上了 ARM 开发之路。
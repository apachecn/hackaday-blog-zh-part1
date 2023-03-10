# u 盘推进器开发板

> 原文：<https://hackaday.com/2011/09/23/usb-stick-propeller-development-board/>

![](img/ef70fa086590736c03eeb3619f0b85bc.png "usb-propeller-development-board")

[Parker Dillmann]的螺旋桨开发板的原型制作过程即将结束。他想要一个工具，让他在不需要一堆设备的情况下进行项目工作，同时仍然保持必要时扩展硬件的能力。[他的最后一个开发板](http://hackaday.com/2011/03/29/propeller-proto-board-has-you-flying-in-no-time/)使用了一大块原型板来托管通孔组件，包括螺旋桨芯片、3.3V 和 5V 调节器、SD 读卡器和母引脚接头。这个版本从工厂迁移到 PCB，主要是表面贴装元件。

由于对 TI 的一些原型工具感到满意，他决定使用 u 盘设计。Parallax 品牌的开发板使用 FTDI 232RL 芯片来轻松编程，这也是他一直使用的芯片。选择 QFP 封装的 P8X32A 芯片比较小的 QFN 更容易焊接。船上还有一个 64kb 的 EEPROM，为您的旋转程序提供充足的空间。所有的引脚都是打破了 DIL 母头，并有一个对 USB 插头的一端电源头。[Parker]计划做一些测试，以确保低于 5Mhz 晶体足迹的信号路由没有问题。这一批原型来自 Seeed Studios Fusion PCB servcie——他总共花了 13 美元买了 10 多块电路板……这几乎令人难以置信。
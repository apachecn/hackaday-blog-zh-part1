# NES 控制器到 USB 游戏手柄

> 原文：<https://hackaday.com/2010/06/30/nes-controller-to-usb-gamepad/>

![](img/99ae4c9c9cf614b78ff0cd04b61e7be4.png "nes-arduino")

普通的黑客阅读器[Osgeld]又开始用这个 [USB 转换 NES 控制器](http://www.instructables.com/id/Convert-a-NES-gamepad-to-USB-with-Arduino)。这是一个无处不在的黑客，我们在很早就开始看到[，有时涉及](http://hackaday.com/2004/09/07/make-a-nintendo-controller-in-to-a-usb-joystick/)[一个适配器套件](http://hackaday.com/2008/06/14/universal-joystick-usb-interface/)，其他时候[包括像拇指驱动器和 USB 集线器](http://hackaday.com/2008/07/19/usb-nes-controller-plus/)这样的东西。但这一次是真正的基本版本。他使用的是 Arduino，但它实际上只是一个运行引导程序的 AVR ATmega168。我们敢打赌，用 ATmega8 也能轻松做到这一点。抓住几个二极管(当我们需要时，我们似乎从来没有 3.6v 齐纳二极管)，几个电容和电阻，一个晶体，你就开始工作了。黑客将每个按钮连接到一个引脚，并实现了一个键盘 HID，可以映射到任何你想要的目的。
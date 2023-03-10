# AVR 灯光控制器

> 原文：<https://hackaday.com/2009/01/30/avr-light-controller/>

![halogen](img/0a509bc957863481d5c5db18442190d3.png "halogen")

[马提亚斯]给了我们这个项目，他[制作了一个 AVR 灯光控制器](http://electronics.ringwald.ch/?n=Main.AvrLightController)。他有一个卤素自行车灯，但对它的铅酸电池不满意。他想使用锂聚合物电池，但发现由于电压问题，它们不能直接用于卤素灯。His 充满电产生 8.5 伏，不能放电到 5 伏以下。他需要一个新的功率控制器来降低灯的电压，灯的电压需要保持在 6-12 伏之间。

他用一个 ATtiny45 做 [PWM](http://en.wikipedia.org/wiki/Pulse-width_modulation) 来改变电压。他添加的其他一些很酷的功能是高低设置和一个 LED 状态灯警告。你可以在他的页面上找到图片、图表和源代码，以及大量的信息。干得好[马提亚斯]。
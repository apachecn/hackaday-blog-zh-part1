# 基于笔记本电脑触摸板的 LED 照明控制

> 原文：<https://hackaday.com/2011/03/24/laptop-touchpad-based-led-lighting-control/>

![touchpad_lighting](img/b7781428318da3db10995efaf05f5a17.png "touchpad_lighting")

[Dave]需要在他的桌子/工作台上方增加一些额外的照明，他决定安装一些 RGB LED 灯带来照亮这个地方。他不满足于使用标准开关来打开和关闭它们，经过一番头脑风暴后，他决定使用安装在项目箱中的一对铜管来构建一个电容触摸电路。就在他对他的开关进行最后的润色时，他在网上看到了一个项目，其中 Synaptics 触摸板与 Arduino 一起用于照明控制。铜管开关已经装好，他开始忙着操作他的 Arduino。

当连接到 Arduino 时，触摸板可以在两种模式下使用——相对和绝对。相对模式为大多数人所熟悉，因为它用于在笔记本电脑屏幕上引导鼠标光标。然而，绝对模式将坐标信息传回 Arduino，允许用户将 pad 的特定区域映射到特定功能。[Dave]使他的触摸板能够使用绝对模式，并在 Arduino 上映射了一些不同的功能。他现在可以让灯渐亮渐灭，或者用定时器点亮房间，还可以使用滑动功能来调节 led 的亮度。

这是一个简洁而简单的方法，也是重新利用旧笔记本触摸板的好方法。

继续阅读他整理的快速演示视频，如果你想看看他用来实现这一点的源代码，请访问他的网站。

[https://www.youtube.com/embed/ViBDuM0C-KM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ViBDuM0C-KM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
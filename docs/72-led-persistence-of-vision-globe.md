# 72 LED 视觉暂留地球仪

> 原文：<https://hackaday.com/2009/10/15/72-led-persistence-of-vision-globe/>

![HaD-pov-globe](img/6e551ad4880cd123927607a144fa89b0.png "HaD-pov-globe")

[本]昨天给我们讲了他的 POV 地球仪。我们看了一眼，只看到一张照片和代码，没有对他的项目进行真正的解释。他肯定开始通宵工作，现在我们看到了[所有我们在一个伟大的构建日志中寻找的好东西](http://hackaday.com/2009/09/19/how-to-make-your-project-an-internet-sensation/)。他甚至把 Hackaday 的标志扔了出来供我们欣赏。他的构建执行得很好，他找到了一些创造性的方法来解决这些项目中的常见问题。休息之后我们来仔细看看。

![pov-globe-overview](img/09de5247c339cdd6ea733b113ca0c8ff.png "pov-globe-overview")

[Ben]的设计看起来很像一个真实的地球仪，有一个底座，一个框架和一个旋转轴倾斜的旋转环([就像地球](http://en.wikipedia.org/wiki/Axial_tilt))。72 个表面安装发光二极管用于显示，一个移除了叶片的 PC 风扇提供旋转，一个簧片开关与一个磁铁一起用于使旋转与显示解析同步。

![leds-taped-and-placed](img/03a5106733077ece64ca60f154a33142.png "leds-taped-and-placed")

表面贴装元件是为了在电路板上放置和回流焊。对于自由形式的电路，它们通常被认为太小。[Ben]通过将所有 72 个 led 面朝下排列在一些胶带的粘性面上，使这一过程为他所用。这使得他更容易将微控制器接口所需的多路复用焊接在一起。你可以看到他使用的漆包线可以直接焊接，无需剥离。[Ben's]使用一片透明的 DVD-R 容器盖作为显示屏的旋转环。在上图的右边，你可以看到安装在这个透明环上的完整的 LED 多路复用器。

![pov-globe-headphone-jack](img/7c12b0fc461caf65d38ef94d65c8c896.png "pov-globe-headphone-jack")

为[视点显示器](http://hackaday.com/2009/06/13/persistence-of-vision-propeller-clock/)的旋转部分供电始终是一个需要考虑的问题。[Ben]尝试通过有刷电机连接，但遇到了断电的问题。他的下一个尝试包括使用耳机插孔和连接器作为支点。稳压电源和地通过两个连接，他在这个系统上取得了巨大的成功。上图中，您可以看到连接器在完全插入原型板上的插孔之前。

![pov-globe-reed-switch](img/d832bd634233f6c9dd9e18fc93e36610.png "pov-globe-reed-switch")

簧片开关粘在透明环上，当它通过框架上的条形磁铁时被启动。这允许微控制器测量环的旋转，并同步显示输出。

[本]在这里做得很好。他回收了很多零件，包括发光二极管。他选择了 Atmel AVR ATmega8 作为微控制器。这是一种廉价且易于获得的芯片，与功能更强大的 ATmega168 引脚兼容，因此如果需要动画或其他功能，需要更多的编程空间，则有可能在未来进行升级。我们建议在 uC 的电源引脚上使用去耦电容，以帮助滤除线路上的任何噪声，尤其是考虑到用于提供稳压电源的旋转连接。

我们想要一个！
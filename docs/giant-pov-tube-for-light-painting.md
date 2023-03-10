# 光绘用巨型 POV 管

> 原文：<https://hackaday.com/2011/06/28/giant-pov-tube-for-light-painting/>

![writing_in_the_night_with_the_light_scythe](img/122a7afb671816c8eae8723bb2aafe40.png "writing_in_the_night_with_the_light_scythe")

当你真的想让别人知道你的感受时，我们总是说越大越好。[加文·史密斯，又名机电一体化家伙]一定来自同一思想流派，因为他试图用他的最新项目表达的意思绝对不会被误解。

受我们不久前推出的 WiFi 信号画家的启发，LightScythe 是一个 2 米长的棒，由他从 Adafruit 购买的多色 LED 灯条组成。灯条由 Seeduino 微控制器控制，该控制器通过一对 XBee 单元从他的笔记本电脑接收指示。一旦他用 ImageMagic 从文本生成图像，Python 脚本就被用来匹配尽可能接近 RGB 颜色空间的颜色。然后，图像被转换为原始串行数据，以便在长柄大镰刀上播放。当他准备好要走的时候，他触发他的照相机进行 10-15 秒的曝光，在此期间，他走过画框，用光线描绘他的图像。

我们总是喜欢看到我们之前报道过的项目的创造性衍生，而 LightScythe 做得很好。他实际上制作了一对这样的装置，它们可以协同工作，也可以独立工作，我们想象这可以制作出一些非常棒的照片。

请务必查看他的 Flickr photostream 以获得更多 LightScythe 能做什么的例子。
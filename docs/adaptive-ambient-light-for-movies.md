# 用于电影的自适应环境光

> 原文：<https://hackaday.com/2006/07/10/adaptive-ambient-light-for-movies/>

Divxstation 的[RafkeP]创造了这个聪明的技术来克隆飞利浦电子公司[的流光溢彩](http://en.wikipedia.org/wiki/Ambilight)技术用于他们的平板电脑。流光溢彩是一种 RGB 背光，可以根据屏幕上的图像改变颜色。它应该让观看体验更舒适。 [MoMoLight](http://divxstation.com/article.asp?aId=151) 使用 directshow 滤镜计算屏幕顶部、左侧和右侧边框的平均颜色。它将这些信息发送到一个微控制器，该微控制器对红、绿、蓝三组独立的冷阴极进行 PWM 控制。可以使用发光二极管来代替。根据飞利浦的命名方案，监控顶部、左侧和右侧将被称为流光溢彩 3，这实际上还不存在。

[感谢马蒂亚斯 vdb]

*   [永久链接](http://divxstation.com/article.asp?aId=151)
# 遥控玻璃砖 led 矩阵

> 原文：<https://hackaday.com/2011/10/15/remote-controlled-glass-block-led-matrix/>

![hive13_remote_controlled_led_matrix](img/bd90f12a166aac92ceb96ed17253c4fd.png "hive13_remote_controlled_led_matrix")

在辛辛那提的黑客空间 Hive13，他们喜欢攻击任何东西，甚至是他们的浴室。浴室的一面墙面向街道，由厚厚的玻璃隐私块组成。几年前，他们认为在玻璃墙的背面安装一个 LED 矩阵会是一个很酷的想法，可以稍微装饰一下。经过几次反复之后，他们终于有了他们乐意展示的东西，但他们想让它更酷。

虽然运行 matrix 的 Arduino 和 ShiftBrite shield 可以通过串行连接进行控制，但他们希望使用 ProjectBlinkenlights 工具通过网络进行控制。虽然这并没有完全按照计划进行，但也不一定是徒劳的。虽然 Blinkenlights 控件是不可能的，但他们受到了启发，将 OSC 兼容性添加到处理草图中，这使他们可以使用适用于 Android 和 iOS 设备的应用程序来处理显示器。

结果相当光滑，正如你在下面的视频中看到的。现在他们需要做的就是让俄罗斯方块运行起来！

[https://player.vimeo.com/video/30413454](https://player.vimeo.com/video/30413454)
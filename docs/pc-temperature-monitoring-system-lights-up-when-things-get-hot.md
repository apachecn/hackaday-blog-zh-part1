# 当物体变热时，电脑温度监控系统会亮起

> 原文：<https://hackaday.com/2011/10/04/pc-temperature-monitoring-system-lights-up-when-things-get-hot/>

![gpu_overheating_warning_system](img/e71176d3f7cbeaa24a4052125a8123ab.png "gpu_overheating_warning_system")

[Taylor]在他的电脑中插入了一个新的显卡，但在他开始玩一轮游戏之前，他的显卡开始过热。他最终追踪到问题出在一个尺寸过小的电源上，但是将他的新 GPU 烤死的前景让他对如何监控系统的健康状况三思而行。

为了持续监控显卡的温度，他安装了一个小电路，如果温度过高，这个电路会提醒他。他在 GPU 附近的显卡上安装了一个小型温度传感器，将其连接到 Arduino。Arduino 监控他的视频卡，如果情况正常，就会点亮一个蓝色的 RGB LED。如果温度上升到 50C 以上，LED 变成红色，表示有问题。

我们知道，有各种各样的软件应用程序可以为您监控组件温度，但[泰勒的]系统的吸引力在于，它可以从房间的另一端轻松看到，而不是通过桌面。也就是说，我们认为他的系统可以利用他的电脑的风扇照明来发出更明显的警告，并且在他不在的时候，如果他的电脑过热，安装自动关机功能也不会有什么坏处。
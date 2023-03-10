# 使用音频文件为 Arduino 编程

> 原文：<https://hackaday.com/2011/12/30/programming-an-arduino-using-an-audio-file/>

![](img/f6f40ee569bf822a9dea67e7b37db79c.png "arduino-based-monotribe")

这个概念验证就等着你好好利用了。[Mike Tsao]写了一个 Arduino 草图，让他[解码输入的音频数据](https://github.com/sowbug/TribeDuino)，这些数据可用于对设备进行编程。他称这个项目为 TribeDuino，因为它解码了一个音频文件，这实际上是 Korg Monotribe 的固件更新。

本月早些时候,[Mike]阅读了我们关于一个项目的专题文章，该项目的[对 Korg 硬件的基于音频的固件更新](http://hackaday.com/2011/12/03/reverse-engineering-a-korg-monotribe/)进行了逆向工程。他想看看能否在自己的硬件上编写一些代码来读取该文件。只需要一个音频插孔和两根跳线就可以让 Arduino 准备好接收音频文件。他的固件在播放音频时读取二进制频移键控编码数据，然后回显一个校验和以证明它工作正常。

这将是对你自己项目的一个极好的补充。由于音频连接只需要单声道，所以只需要一个 Arduino 引脚来添加这个插孔(另一个是接地连接)。我们刚刚尝试了将数据推送到微控制器的其他方法，当我们有空的时候，我们可能会尝试一下。
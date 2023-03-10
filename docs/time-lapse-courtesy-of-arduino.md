# Arduino 的延时摄影

> 原文：<https://hackaday.com/2009/10/30/time-lapse-courtesy-of-arduino/>

![arduino-time-lapse](img/946036ffbcc75ad804dee5fa18442d02.png "arduino-time-lapse")

[罗斯]组装一个小的[包，用于延时摄影](http://blog.tinyenormous.com/2009/09/30/17-arduino-nikon-ir-intervalometer-code/)。他正在使用的尼康相机可以在收到红外命令时拍摄照片。[Ross']解决方案将一个红外 LED 连接到一个 Arduino 来产生该信号。帧之间的延迟由电位计设置，电位计通过 ADC 读取。这比我们看到的最后一个解决方案中的[要简单得多。](http://hackaday.com/2009/10/13/a-different-breed-of-camera-controllers/)

该单元由 Arduino 克隆、9v 电池和电缆上的 IR LED 组成，很容易放入相机包中。他发布了代码，休息后我们嵌入了他的工作示例。电位计周围的外壳和时间基准将完善这一方便的工具。
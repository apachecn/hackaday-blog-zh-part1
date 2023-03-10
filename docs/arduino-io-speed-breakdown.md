# Arduino I/O 速度故障

> 原文：<https://hackaday.com/2010/01/06/arduino-io-speed-breakdown/>

![](img/dc00c9011dcce16d1d85565af82aeb5f.png "IMG_0166")

[ [Jee Labs](http://news.jeelabs.org/) ]已经计算出一个 [Arduino 执行各种 I/O 操作需要多长时间](http://news.jeelabs.org/2010/01/06/pin-io-performance/)。可以预见， [analogRead()](http://arduino.cc/en/Reference/AnalogRead) 耗时最长，其次是 [analogWrite()](http://arduino.cc/en/Reference/AnalogWrite) 。Arduino 在数字引脚 I/O 方面确实落后: [digitalWrite()](http://arduino.cc/en/Reference/DigitalWrite) 比直接向端口寄存器写入位要多花 50 倍的时间！当你想用 Arduino 做一些强大的 I/O 时，这是需要考虑的事情。也许这种 I/O 性能将在未来用 Arduino 1.0 解决。
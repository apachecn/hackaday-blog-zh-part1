# ATTiny Hacks:在 ATTiny 上运行您的 Arduino 项目！

> 原文：<https://hackaday.com/2011/09/13/attiny-hacks-run-your-arduino-project-on-an-attiny/>

![](img/5f674cf2d4b94faba5f6b413d805f657.png)

![](img/f6868ab1831a82599625e1f1d17d2e17.png "bigdreams")

没错。我们都经历过。你把一个非常复杂的 Arduino 项目放在一起，它只需要几个引脚，比 Arduino 的原生微控制器要少得多。恐怕不行，[撒切尔]已经通过在 Arduino IDE 中添加一些 ATTtiny 内核解决了这个问题。[他的](http://toasterbotics.blogspot.com/2011/08/using-arduino-with-attinys.html) [博客](http://toasterbotics.blogspot.com/2011/08/programming-attiny85-arduino-style.html)详细描述了从抓取麻省理工学院开发的[核心文件](http://hlt.media.mit.edu/wiki/pmwiki.php?n=Main.ArduinoATtiny4585)并加载到你的 Arduino 软件目录中的过程。修改看起来很简单，虽然[Thatcher]在 Mac 上展示了整个过程，但它只涉及解压缩文件并将其放入一个文件夹。由于 ATTiny 芯片每个只有几美元，这对于那些简单的软件驱动的黑客来说是完美的，不需要将整个 Uno 导管粘在外壳的外面。干得好[撒切尔]！
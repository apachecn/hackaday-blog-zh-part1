# MindWave 是开发者友好的精神控制

> 原文：<https://hackaday.com/2011/04/22/mindwave-is-developer-read-hacker-friendly-mind-control/>

![](img/f4014a4f89f26680986afe0bc9b4ef14.png "mindwave-arduino-interface")

这里有一个用你的头脑控制伺服电机的设置。[丹尼·伯特纳]通过将一个 [MindWave 耳机](http://store.neurosky.com/products/mindwave-1)与一个 Arduino 接口，使这个项目得以实现。你可能想知道这有什么大不了的，因为我们已经报道了相当多的以这种方式工作的[精神控制黑客](http://hackaday.com/2011/03/08/controlling-fire-with-your-mind-and-your-thumb/)？到目前为止，这些黑客中的大多数都使用了 Mindflex 玩具(公平地说，也有几个[使用了 Force Trainer](http://hackaday.com/2010/05/18/composing-music-with-the-force-trainer/) )，它依赖于负责 MindWave 的公司制造的芯片。Mindflex 和 Force Trainer 都经过了逆向工程，可以访问来自 EEG 传感器的数据流。但是 NeuroSky 正通过提供开发者工具来迎合弄乱他们产品的冲动。

[Danny]利用这些资源，使用公司自己的[指南与 Arduino](http://developer.neurosky.com/docs/lib/exe/fetch.php?media=mindwave_arduino_and_leds.pdf) (PDF)接口。休息后的快速剪辑显示了他完成的项目，从耳机附带的 USB 加密狗中抓取数据，将其转换为 Arduino 所需的电平，然后处理信号以显示在 LED 条形图上。

我们不禁窃笑 PDF 指南顶部的保修无效免责声明。

【维梅奥 http://vimeo.com/22634724 w = 470】
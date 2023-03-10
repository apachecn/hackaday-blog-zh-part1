# 使用 RFID 保护您的 Keurig

> 原文：<https://hackaday.com/2012/01/04/securing-your-keurig-with-rfid/>

![keurig-hacking](img/1ffefcc1b28392f11d50a5f55c7e9784.png "keurig-hacking")

[安德鲁·罗宾逊]和他的同事们很幸运，他们的办公室里有一台 Keurig 咖啡机，尽管他们很难记住谁欠了社区咖啡基金多少钱。由于 K 杯咖啡比散装咖啡更贵，[Andrew]认为他们需要一种更好的方法来记录每个人的饮酒习惯，以便知道谁在月底需要支付最多的现金。

他首先拆下 Keurig B40，记下里面的各种 PCB，同时确定破解该设备的最佳方式。咖啡机是由 PIC 控制的，他没有试图从下往上重新设计，而是原封不动地保留了机器的核心，专注于控制面板。

他从控制板上断开了该装置的所有按钮，在将它们重新连接到机器之前，将它们通过 Arduino 路由。这基本上使得机器无法操作，除非由 Arduino 触发，让[Andrew]控制酿造过程。他连接了 SparkFun 的 RFID 阅读器，然后[忙于编写](http://andrewbrobinson.com/2011/12/31/hacking-the-keurig-b40-coffee-maker-%E2%80%93-part-2-%E2%80%93-software/)他的安全/库存系统。现在，当有人想要咖啡时，他们只需要在机器上刷一下他们的办公室门禁卡，就可以使用它的控制面板。

正如你在下面的视频中看到的，这个系统似乎工作得很好。如果我们要提供一些建设性的批评，我们会建议放弃笔记本电脑，转而将 RFID 读取/验证功能放入 Arduino 中——除此之外，我们认为这很棒。

[https://www.youtube.com/embed/jI1n5lJCzHs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/jI1n5lJCzHs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
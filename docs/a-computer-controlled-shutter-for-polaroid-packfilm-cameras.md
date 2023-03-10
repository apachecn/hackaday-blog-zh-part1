# 宝丽来包装胶片照相机的计算机控制快门

> 原文：<https://hackaday.com/2011/05/19/a-computer-controlled-shutter-for-polaroid-packfilm-cameras/>

![](img/e124b7e63017433086e14a9bb49069ca.png "thumb")

[Georg]想改装他的旧宝丽来陆地相机，这样他就可以控制曝光时间。如果我们自己这么说的话，由此产生的项目是一个整洁的黑客。

宝丽来 100 系列包装胶片相机中的电子元件是一台简单的模拟计算机，通过光敏电阻集成电流。这是一个简单的，低技术含量的方法来确保曝光时间是正确的。通常的方法是用一个电位计代替光敏电阻，但是[Georg]的这种改进几乎没有成功。在拆除了相机的旧部件后，[Georg]用 PIC 微控制器取代了古老的电子设备，现在能够以低至 1/512 秒的增量控制快门。

快门时序由带 BCD 编码器的 PIC12F629 μC 读取。[Georg]保留了快门磁铁设置，还增加了一个“灯泡”程序，只要按下按钮，快门就会打开。测试照片非常好，即使是来自 20 世纪 60 年代的宝丽来陆地相机。休息之后，看看[Georg]运行快门设置的视频。

 [https://www.youtube.com/embed/YlRZHvAusEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YlRZHvAusEo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# 为旧的台式工具增加 USB 连接

> 原文：<https://hackaday.com/2011/07/25/adding-usb-connectivity-to-old-benchtop-tools/>

![frequency_counter_hacked_for_usb_connectivity](img/59e39d88ab0d67bc4af739449e4ce31a.png "frequency_counter_hacked_for_usb_connectivity")

[Scott]最近得到了一个频率计数器，一旦他把它带回家，他就开始考虑如何让它变得更好。虽然计数器工作正常，但他想找到一种方法来记录相当长一段时间内的数据读数。他认为把它和他的电脑连接起来是最好的方法，但是他必须先找到连接设备的方法。

他开始在频率计里摸索，当仔细查看显示板时，偶然发现了一个可能的数据源。他发现他可以在频率数据被写入显示器时读取数据，并将数据发送到他的计算机。他使用 ATMega48 截取来自 V-USB 项目的数据和代码，通过 USB 将数据存储到他的 PC 上。

现在，他在频率计上看到的任何东西都可以很容易地在他的电脑上收集和绘制出来。

留下来看看他的黑客行动的快速视频演示。

[https://www.youtube.com/embed/c6uFN52LGnc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/c6uFN52LGnc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# 从电阻式触摸屏读取数据的基础知识

> 原文：<https://hackaday.com/2011/10/28/the-basics-of-reading-data-from-resistive-touchscreens/>

![](img/a049672f4842d04d26c2da5f76aace4d.png "basics-of-resistive-touchscreens")

[Chris]刚刚发布了他的最新教程，向您展示了如何从电阻式触摸屏上读取位置数据。这些设备相当简单，因为它们被用于许多消费电子产品中，你只需花几美元就可以买到一台。这看起来像是一个旧的掌上设备积压。

接口很简单，覆盖层顶部的标签上只有四根导线。但连接到这些是一个有点问题，因为你不能真正直接焊接到他们。[Chris]最后用透明胶带把电线固定住，用回形针把它们压在导体上。这些导线成对使用，X 轴和 Y 轴有一个正极引线和一个负极引线。要进行测量，您需要使用 I/O 引脚连接电压和地，然后使用 ADC 读取使其接地的电压。这是因为屏幕上被按压的点充当了电路的可变电阻。两个轴的数据必须分别读取，这样正电压才不会相互干扰。

好的一面是，一旦你让它在小屏幕上工作，它很容易被放大。事实上，[这个 Android 黑客](http://hackaday.com/2011/10/10/how-to-build-a-23-android-tablet/)使用的 23″触摸屏只是另一个 4 线电阻设备。

休息后，您可以看到嵌入的[Chris']测试装备的视频演示。

[https://www.youtube.com/embed/sXsW0tSgfWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sXsW0tSgfWY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
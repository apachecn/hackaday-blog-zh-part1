# 廉价简易的逻辑信号发生器

> 原文：<https://hackaday.com/2012/02/27/cheap-and-easy-logic-signal-generator/>

虽然函数发生器或模拟信号发生器在它们的应用中无处不在，但我们在 Hack a Day 上并没有看到多少逻辑函数发生器。幸运的是，[Dilshan]送来了一个非常整洁的 [8 通道信号注入器](http://jayakody2000lk.blogspot.com/2012/02/kidogo-8-channel-usb-digital-signal.html)，它非常简单，并且带有一个很棒的前端，可以从你的计算机上编辑模式。

构建中的[硬件](https://github.com/dilshan/Kidogo/raw/master/Design/kidpcb.jpg)部分保持最少，PIC18F 芯片、USB 插座和插头引脚是唯一的主要组件。该板用作 Kidogo 软件的硬件输出。这个软件提供了一个[非常好的界面](http://hackaday.com/wp-content/uploads/2012/02/kidogo.png)来产生 8 个独立通道上的 5 伏逻辑信号，这将极大地帮助探索你的数字世界。

凭借出色的界面和非常容易构建的硬件，我们可以很容易地看到 Kidogo 硬件在世界各地的工作台上找到了自己的路。我们很想使用 AVR 来构建自己的版本，但是我们不想破坏这样一个简单而有用的工具。
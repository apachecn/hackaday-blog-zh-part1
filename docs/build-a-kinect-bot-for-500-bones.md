# 为 500 块骨头造一个 Kinect 机器人

> 原文：<https://hackaday.com/2011/11/09/build-a-kinect-bot-for-500-bones/>

![](img/945b721347c139f54c725b28b60157c0.png "kinect")

[Eric]发来了他的教程，内容是花 500 美元制作一个基于 Kinect 的机器人，这是一个低成本的解决方案，可以帮助认为丈夫在机器人上花费太多的妻子。

作为构建的基础，[Eric]使用了一个 iRobot Create，这是 Roomba 的衍生产品，专为一些硬件黑客打造。对于机器人的命令和控制，EEE 上网本从 Kinect 获取数据，并通过串行连接发送给 iRobot。

建造本身非常简单:两块角铝连接到机器人上，一个塑料牛奶箱用拉链安装。Kinect 位于塑料箱的顶部，上网本舒适地放在里面。

几周前，[Eric]发布了 Kinect 的[历史和开源软件的摘要，其中涵盖了 Libfreenect 驱动程序的开发。[Eric]为他的机器人使用了同样的驱动程序。目前，机器人配置为两种模式。第一种模式让机器人移动到离自己最远的地方。第二种模式指示机器人跟随离自己最近的东西——走在机器人前面，它就变成了一个咬脚踝者。](http://buildsmartrobots.ning.com/profiles/blogs/one-year-anniversary-for-the-kinect-over-10-million-units-shipped)

Kinect 有一个限制,[Eric]正试图解决这个问题。距离 Kinect 不到 19 英寸的物体看起来非常远。这导致了许多碰壁，但他计划增加一些超声波传感器来填补传感器数据的空白。对于一个非常便宜的自主机器人来说还不错。
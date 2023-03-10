# 为视障人士绘制数据

> 原文：<https://hackaday.com/2010/10/18/data-plotting-for-the-visually-impaired/>

![](img/29f676b92779eda6f12afdeb29f59964.png "visually-impaired-scatterplots.jpg")

这种设置有助于以有意义的方式为视障人士呈现数据。它使用物理对象的组合来表示数据簇，并在操作这些对象时使用音频反馈。在休息后的视频中，您将看到立方体可以调整自己的方向来表示数据集群。桌面就像一个绘图区，带有纹理的边框作为用户的参考。安装在透明表面下的照相机允许图像处理软件计算立方体的位置。每个立方体都是电动的，包含一个 Arduino 和 ZigBee 模块，侦听来自进行视频处理的计算机的定位信息。一旦就位，用户可以移动立方体，用调制噪声来衡量它们离每个数据簇的中心有多近。

该小组计划对这种交互式数据对象的有用性进行进一步研究。我们当然看到了黑客攻击的可能性，因为它使用了既便宜又容易找到的现成组件。这无疑让我们想起了添加了物理令牌的多点触摸显示屏。

[https://www.youtube.com/embed/ibnz3poa9RU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ibnz3poa9RU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[感谢 UrsusExplorans]
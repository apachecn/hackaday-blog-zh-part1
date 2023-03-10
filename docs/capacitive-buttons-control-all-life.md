# 电容式按钮控制生活

> 原文：<https://hackaday.com/2009/09/28/capacitive-buttons-control-all-life/>

![capacitive_game_of_life](img/517e7d3c5fa05e166995d8e17f28295c.png "capacitive_game_of_life")

涉及康威的《生命的游戏》和使用诺基亚 3310 屏幕的项目很受电子爱好者的欢迎。[Droky]将这两者结合在一起，并通过添加[电容传感器来控制生活游戏](http://radikaldesig.blogspot.com/2009/09/juego-de-la-vida-game-of-life-conway.html)而更进一步。他的工作是如何使用 Atmel QTouch 电容传感器的一个很好的例子( [QT100a 数据手册](http://www.atmel.com/dyn/resources/prod_documents/doc9531.pdf))。这种芯片完成了我们在[其他触摸感应解决方案](http://hackaday.com/2009/09/18/touch-sensitive-keypad/)中看到的繁重工作。它的工作电压为 2V-5.5V，只需要三个电容和一个电阻，具有一个引脚的高电平有效输出，少量出售的价格约为 1 美元。[Droky]在电路板布局中忽略的一件事是 WSON6 芯片底部的接地焊盘。他能够通过掩盖芯片下的走线来使其工作，但您可能希望在自己的设计中改变布局。

如果您之前使用过 QT100a，我们希望了解您的体验，并了解该芯片是否需要按钮去抖处理。请在评论中告诉我们。休息之后你可以看到一段视频。

[https://player.vimeo.com/video/6791696](https://player.vimeo.com/video/6791696)
# 康威的生命墙和白板商场

> 原文：<https://hackaday.com/2011/01/27/conways-wall-of-life-and-whiteboard-emporium/>

![](img/b0bc481685f4aacbac1015098a12be38.png "conways-wall-of-life")

白板胜过粉笔板，LED 字幕胜过白板，LED 白板胜过所有白板。

这个混合体可以让你用干擦笔在表面上画画，而康威的生活游戏在下面进行。[伯特]给我们发来这个提示后，看到[昨天的办公室字幕](http://hackaday.com/2011/01/26/12-led-display-keeps-your-office-informed/)。这个版本在外观上很相似，但内在却大不相同。在里面，你会发现一个视差 SX28 微控制器做繁重的工作。显示器是多路复用的，但他们没有普通的 595 移位寄存器，而是一个更强大的 [MAX6979 LED 驱动器](http://www.maxim-ic.com/datasheet/index.mvp/id/4909)。我们对这款器件不太熟悉，但它确实有很多不错的特性，比如恒流，以及串行数据停止超过 1 秒时自动关断。这是低端驱动器，因此晶体管用于将电压连接到行；与我们昨天看到的设置相反。这是几年前建造的，尽管它永久的家是一个试验板，但仍然工作得很好。源代码可以在本页找到[。](http://www.seanhillmeyer.com/portfolio/wallolife.php)
# NBA Hangtime 弹球展示

> 原文：<https://hackaday.com/2011/03/12/nba-hangtime-pinball-display/>

![](img/dfd5ae6d3498e9e1e19739eea4e8ab0f.png "nba hangtime pinball display")

[埃德·扎里克]继续他的 NBA Hangtime 弹球机的工作，完成记分牌和后玻璃。你应该记得这个项目，因为我们已经介绍过[他为系统](http://hackaday.com/2011/02/27/layering-pinball-audio-using-parallel-wav-shields/)开发的层音频。现在，他证明了自己是一个原型板大师，使用点对点技术构建了一对两位半数字的 LED 显示屏，用于显示团队得分，以及击球计时器和其他状态指示器。

控制这一切的照明板通过 i2c 协议发出命令，就像三个音频模块一样。它使用移位寄存器和 MOSFETs，并且[Ed]花时间为电路板互连添加引脚接头和插座。与音频系统一样，一个 Arduino Mega 充当 i2c 总线上的主机，您会在休息后的视频中注意到，显示器与音效完美协调。

我们迫不及待地想看看他为游戏领域带来了什么！

[https://www.youtube.com/embed/1aa-4a376jE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1aa-4a376jE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
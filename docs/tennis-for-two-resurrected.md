# 双人网球复活

> 原文：<https://hackaday.com/2008/07/16/tennis-for-two-resurrected/>

第一个电子游戏被归功于物理学家威利·海金博塞姆。[双人网球](http://en.wikipedia.org/wiki/Tennis_for_Two)使用两个控制器在示波器上进行。每一个都有一个控制轨迹的旋钮和一个击球按钮。邪恶疯狂科学家实验室的优秀人员[重新制作了这个游戏，所以你可以在任何示波器上玩这个游戏](http://www.evilmadscientist.com/article.php/tennis)。ATmega168 用来控制一切。它从拨片接收用户输入，并输出示波器的 X 和 Y 模拟信号。一个 [R-2R](http://hyperphysics.phy-astr.gsu.edu/hbase/electronic/dac.html#c3) 型 DAC 用于输出级，提供 256×256 分辨率。一切都是建立在他们的名片大小的项目板之上的——这真的显示了这样一个简单的板是多么有用。源代码是免费的，文章中包含了大量的细节。我们很想看看人们想出了什么修改，因为基本游戏甚至没有得分。下面嵌入了 EMSL 系统的视频。

<http://www.youtube.com/v/ZlY0PuJeYjo&amp;hl=en&amp;fs=1&amp;rel=0&amp;color1=0x3a3a3a&amp;color2=0x999999>



*   [永久链接](http://www.evilmadscientist.com/article.php/tennis)
# 红外控制音乐闹钟

> 原文：<https://hackaday.com/2011/02/15/ir-controlled-musical-alarm-clock/>

![Music-Playing-Alarm-Clock](img/6e19b7272a138f5b9b8991a356be475d.png "Music-Playing-Alarm-Clock")

论坛用户[Frank]与我们分享了他最近的项目，[一个音乐闹钟](http://forums.hackaday.com/viewtopic.php?f=3&t=261&sid=bd071c894cd448a1dcbc5e0cdf87443c)。他的发明不仅仅是一个简单的闹钟，它允许用户将音乐加载到一个微型 SD 卡上，每周每天都有闹钟设置，最重要的是，可以使用红外遥控器进行控制。他使用 Teensy++来控制时钟的大部分功能，包括显示，将计时委托给 DS1307 实时时钟。所有的音频回放都由安装在分线板上的独立音乐解码器处理。

他的 Instructables 文章非常详细，提供了大量注释、图片、图表和源代码。他详细介绍了每一个步骤，对于那些希望开始 AVR 编程的人来说，这是一个很好的学习指南。

他的最后陈述是一个关于回收利用的很好的教训，尽管不幸的是有点黯淡，因为时钟被包装在一个旧的 SparkFun 纸板盒子里。他确实提到最后有一些时间限制，这可能解释了这个选择——很高兴看到这个时钟的修订版包装在一个漂亮的 plexi 盒子里。
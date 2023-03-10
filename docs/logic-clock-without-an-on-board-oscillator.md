# 无板载振荡器的逻辑时钟

> 原文：<https://hackaday.com/2010/04/07/logic-clock-without-an-on-board-oscillator/>

![](img/e6f0a07fe57bb10e09f27b12f8551aea.png "logic-clock-with-AC-frequency-counter")

[lucassignlo 21]在没有使用晶体振荡器或谐振器的情况下开发了这个逻辑时钟。相反，他让输入的电流为他计时。电源为 50 Hz 交流电源，因此他使用一些 4017 十进制分频器将其降至 1 Hz 信号。从那里它记录滴答，就像[我们看到的最后一个数字逻辑时钟](http://hackaday.com/2010/04/03/clock-sans-microcontroller/)。

如果您在项目中使用交流线路频率作为时钟源，我们希望了解一下。给我们发一个小贴士并确保你的文章中包括一个原理图。我们特别感兴趣的是，看看是否有人有一个好方法来使用这种方法与廉价的微控制器。
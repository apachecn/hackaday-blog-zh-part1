# 节奏组合锁

> 原文：<https://hackaday.com/2009/12/22/rhythmic-combo-lock/>

[MusashiAharon]宿舍的门几乎是乞求被黑的。已经有一个电子冲击板，以及由导管连接的内外接线盒。在这里看到一些[和其他](http://hackaday.com/2009/11/17/rfid-door-lock-the-right-way/) [的门锁黑客](http://hackaday.com/2009/07/06/automated-dorm-room-door/)后，他赶时髦建造了一个使用节奏组合的门锁。

外部的控制面板是一个空白面板，有两个按钮和一个状态 LED。这些电线连接到一个插孔，并通过导管连接到门内侧的试验板。看到一个大的试验板挂在插座盖上有点滑稽，但它确实有用。从那里， [Teensy](http://www.pjrc.com/teensy/) 微控制器等待代码，如果正确，通过继电器驱动冲击板。

这把锁的节奏性让我们想起了[基于敲击的系统](http://hackaday.com/2009/11/04/knock-detecting-lock/)。一个按钮表示代码的开始和结束，另一个用于输入节奏序列。这看起来更谨慎一些，我们可以想象很难偷听正确的组合。
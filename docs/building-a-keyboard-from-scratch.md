# 从头开始构建键盘

> 原文：<https://hackaday.com/2012/02/15/building-a-keyboard-from-scratch/>

经过一年多的工作，[dmw]几乎完成了他那简陋的黑客键盘。这种键盘受到了一些漂亮的[疯狂外观设计](http://humblehacker.com/keyboard/design/Influences(3C616352).html)的影响，但满足了[dmw]对紧凑、面向程序员、易于输入的按键布局的所有需求。

[dmw]在 geekhack 键盘论坛上发布了一个[伪构建日志](http://geekhack.org/showwiki.php?title=Island:6292)。这个键盘的每一个部分都是定制的。键帽由[招牌塑料](http://www.signatureplastics.com/profile.html)制作，外壳由 [Shapeways](http://www.shapeways.com/) 制作，按键开关的定制 PCB 直接来自 Express PCB。按键开关是蓝色 Alps 滑块(最好的按键开关之一)，带有几个取自旧苹果键盘的白色 Alps 开关。

在焊接了一百个二极管和开关之后，[dmw]安装了一个 [Teensy++](http://www.pjrc.com/store/teensypp.html) 来将关闭的按键开关转换成他的计算机可以理解的东西。这被证明是一个完美的少年，因为 USB 外设库已经存在。来源是 github 上的[，所以如果你曾经想用更符合人体工程学的东西替换你的 M 型，这是你的机会。](https://github.com/humblehacker/keyboard)
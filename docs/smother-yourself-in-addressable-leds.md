# 让自己沉浸在可寻址的发光二极管中

> 原文：<https://hackaday.com/2011/12/15/smother-yourself-in-addressable-leds/>

![](img/a9497c2872fc4808d8d83ef2d76e8322.png "burning-man-led-suit")

猜猜这家伙穿着五颜六色的西装要去哪里？如果你说燃烧的人，拍拍你自己的背。在 2010 年为电影节做了一件不太用心的 EL 套装后，桑德决定今年要更进一步。他[买了 200 个 LED 模块贴在这套衣服](http://projects.dehaan.net/2011/12/burning-man-rgb-led-suit/)上，这样他就可以点亮夜晚。

它们被安装在一个网格中，为了保持变化的模式有序，他用一个二维数组在他的代码中绘制了每个模式的物理位置。控制器使用 Arduino nano 通过 SPI 将模式推送到阵列。

[Sander]为控制器提供了几种不同的视觉效果。当一个人和别人握手时，他从右袖口开始选通西装。还有一个音频频谱分析仪芯片和麦克风，让他可以随着音乐脉动灯光。你可以在上面的图像中看到这个东西有多亮，但要获得完整的效果不应该在休息后跳过视频。

他已经把这个项目加入了[全光谱激光切割机赠品](http://www.buildlounge.com/2011/10/07/buildlounge-and-full-spectrum-lasers-are-giving-away-a-laser-cutter/)。如果他赢了，我们期待明年的节日激光切割善良！

[vimeo http://vimeo.com/29552399 w=470]

[通过[建立休息室](http://www.buildlounge.com/2011/12/14/contest-entry-rgb-led-suit/)
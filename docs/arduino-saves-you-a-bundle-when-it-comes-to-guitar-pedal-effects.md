# 当谈到吉他踏板效果时，Arduino 为您节省了一大笔钱

> 原文：<https://hackaday.com/2012/02/16/arduino-saves-you-a-bundle-when-it-comes-to-guitar-pedal-effects/>

![](img/2705510e30f6b942cf70ca00a8cffa95.png "guitar-pedal-effects")

[Deadbird]想要重现一些他在音乐视频中听到的吉他踏板效果。问题是，除非你像他一样狡猾，否则你可能会在硬件上花很多钱。他拿了一个 Whammy 4 踏板，但决定放弃使用 125 美元的 MIDI 控制器，而是选择了 Arduino 来执行基于 MIDI 的更改。

选择 Whammy 4 是因为它能够执行他想要的声音处理，也因为它可以是 MIDI 控制器。通过将 Arduino 连接到该端口(如上图所示),他能够对仅用踏板很难或不可能实现的变化进行编程。例如，[Deadbird]说明了一个命令，它从效果的最低设置跳到最高设置，而不会碰到中间的任何值。在此基础上，他开始对变化循环进行编程，其间存在延迟。最棒的是，你只受限于你把 MIDI 命令写成 Arduino 代码的能力。
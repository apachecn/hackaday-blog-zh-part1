# 自动手电筒标签损坏传感器

> 原文：<https://hackaday.com/2011/12/20/automatic-flashlight-tag-damage-sensor/>

![](img/d1319bc01a5665789ae86fac7a12fc9c.png "Flashlight-tag")

你在晚上出去玩热闹的手电筒游戏。但是你怎么知道你是否被对手的光束伤害到了呢？[Kenyer]通过建立一个由每个参与者佩戴的手电筒标签损坏传感器解决了这个问题。它增加了一点与激光标签一起使用的高科技设备，同时保持了低技术价格标签。

当手电筒的光束穿过圆窗时，传感器依靠光敏电阻来记录击中情况。它只会在三秒钟内记录一次点击。在游戏结束时，记录的总点击次数可以用一个机载 LED 闪回，看看谁是胜利者。休息之后，您可以在视频中看到该功能的演示。

[Kenyer]从使用 Arduino 作为驱动器的试验板原型开始。显然，每位玩家购买一台 Arduino 的成本有点荒谬。他缩小了项目规模，在 ATtiny 微控制器上运行 Arduino 代码。T3[https://www.youtube.com/embed/xLx87CKwnLw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xLx87CKwnLw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
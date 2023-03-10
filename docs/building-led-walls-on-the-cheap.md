# 廉价建造 LED 墙

> 原文：<https://hackaday.com/2012/02/06/building-led-walls-on-the-cheap/>

![](img/14e4ff05ffd1322fef6d07d0ecf5cbc1.png "leds")

大约在去年的这个时候，[KopfKopfKopfAffe]被招募为布景设计师，并被告知为电子音乐派对制作某种灯光效果。该项目的预算不多，只有 200 欧元，但他确实设法建造了体面的 5×5 RGB LED 矩阵，完全由计算机控制。

【KopfKopfKopfAffe】没有时间和金钱去等待制造出来的 PCB，于是一堆 perfboard 被放在一个 CNC 轧机里，用一支笔充当绘图仪。所有需要焊接的线路都由工厂绘制，这一壮举可能节省了在将焊料焊接到铁上之前查看设计的几个小时。

总共制造了五块[板](http://hackedfrompieces.files.wordpress.com/2012/02/pcbs.jpg)，每块板能够控制五个 RGB LEDs。每个板都可以通过 RS-232 串行连接进行简单链接，以便进一步扩展。控制矩阵唯一需要的是 17 位，包括每个 LED 的地址和 RGB 颜色数据。该系统每个节点的成本仅为 10 欧元，但我们认为，如果省去 Molex 和 DB-9 连接器，成本可能会大幅降低。[Kopf]项目结果非常好，休息后检查一下。

[https://www.youtube.com/embed/bMQmOK47rjc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bMQmOK47rjc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
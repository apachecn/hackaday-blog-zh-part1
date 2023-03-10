# 给游戏机添加 MIDI 输入

> 原文：<https://hackaday.com/2011/08/11/adding-a-midi-input-to-a-game-boy/>

[Sprite_tm]又回来了，他的作品总能给人留下深刻印象。他的最新项目是一款 [Game Boy Advance MIDI synth](http://spritesmods.com/?art=gbamidi&page=1) ，它从键盘或音序器获取 MIDI 数据，并将其映射到 Game Boy 声道。

因为他似乎从来没有以正常的方式[做过](http://spritesmods.com/?art=macsearm&page=3)[任何事情](http://hackaday.com/2011/05/27/adding-persistent-memory-and-ethernet-to-vintage-arcade-machines/)，【Sprite_tm】决定不用墨盒运行 Game Boy。[我们在](http://hackaday.com/2010/08/16/gameboy-analog-meter/)之前见过这种情况；GBA 通过多引导连接电缆启动 synth 软件。

[Sprite_tm]围绕一个 ATMega168 设计了一个电路，引导 Game Boy，接收 MIDI 消息，然后翻译并通过 link 端口发送。主要的 Game Boy 代码也有一个简单的界面在屏幕上显示图形和一个音序器，允许他将 MIDI 消息记录到 8 个不同的轨道上。我们认为能够用键盘对 Game Boy chiptunes 进行排序是对小声音 DJ 的巨大改进。

[Sprite_tm]坦率地承认他不是最好的键盘手，他把他的 GBA 合成器给了一个音乐家朋友。由此产生的歌曲是一个名副其实的 8 位芯片曲调的洪水。这种构建背后的电子设备非常简单(可以放在 MIDI 电缆中)，所以我们准备为这一个打破铁。所有相关代码都发布在[Sprite_tm]的构建页面上。下面还有一个视频展示了他的作品的特点。

[https://www.youtube.com/embed/scgBbHuNVAE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/scgBbHuNVAE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
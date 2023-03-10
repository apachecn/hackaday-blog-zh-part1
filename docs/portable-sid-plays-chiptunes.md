# 便携式 SID 播放芯片曲调

> 原文：<https://hackaday.com/2011/06/03/portable-sid-plays-chiptunes/>

![](img/5fa24c9b36280ddac3dfff091cf6580f.png "SID")

[Markus]在 DangerousPrototypes 论坛上开发了一个很棒的 SID 播放器。

[SID](http://en.wikipedia.org/wiki/MOS_Technology_SID) 是(是？)Commodore 64 内部令人敬畏的声音生成芯片，以及 Game Boys 和 NESs 为 chiptune 场景奠定了基础。我们很高兴终于看到一个小的 SID 播放器，它不依赖于 SID 仿真或者相对大的 [MIDIbox](http://www.ucapps.de/midibox_sid.html) 。

SID 播放器本身是 CUI32 PIC 开发板上的一个屏蔽。PIC32 模拟了 Commodore 64 中的 6510 和 6526 CPU 和 CIA 芯片。一个小的 USB 记忆棒存储[高电压 SID 采集](http://www.hvsc.c64.org/)，文件系统通过有机发光二极管屏幕导航。[Markus]说玩家消耗 370 mA，所以他从一个小壁球上消耗。尽管如此，我们想知道是否有可能用一个带有 [SwinSID](http://www.swinkels.tvtom.pl/swinsid/) 的 SD 卡来运行这个，这样就可以降低功耗，实现一个完全便携的 SID 播放器。

我们现在有点怀念 chiptune 和 demoscene 音乐，所以我们现在要听一些~~【妮莉·费塔朵】~~【Janne Suni】，但你可以在休息后看看视频演示[Markus]。


[https://www.youtube.com/embed/gw-TQaskkQ8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gw-TQaskkQ8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
# LaunchPad MIDI Synth

> 原文：<https://hackaday.com/2011/02/13/launchpad-midi-synth/>

![launchpad_midi_synth](img/dc660e8ed337462cdfcb79f17594725a.png "launchpad_midi_synth")

[NatureTM]提交了一篇关于他最近使用 TI LaunchPad 构建的 MIDI 合成器的文章。整体结构非常简单，仅由 MSP430、几个电阻和一个光电隔离器组成。当然，需要一个 MIDI 控制器，但他手头已经有了。

从光隔离器中读取 MIDI 数据后，他的代码会处理其余的事情，调整方波声音发生器以获得正确的音符。他确实提到，由于合成器是单声道的，所以要特别注意确保同步音符得到正确处理。你可以将所有声音发送到一个扬声器，但他使用光隔离器将声音数据发送到多个发射台，从而产生了一个有趣的 MIDI 五重奏。

他在自己的网站上提供了代码和大量视频，但请继续阅读，以便先睹为快。

[https://www.youtube.com/embed/0KzKj_vKYCU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0KzKj_vKYCU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[https://www.youtube.com/embed/HYqZNmr8zfo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HYqZNmr8zfo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
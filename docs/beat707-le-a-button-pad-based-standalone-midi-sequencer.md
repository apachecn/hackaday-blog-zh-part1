# Beat707 LE:基于按钮板的独立 MIDI 音序器

> 原文：<https://hackaday.com/2011/07/20/beat707-le-a-button-pad-based-standalone-midi-sequencer/>

![sparkfun_button_pad_midi_controller](img/5b53b8dbde245aa55483549345ad6967.png "sparkfun_button_pad_midi_controller")

[古伊列梅]拿起一个 SparkFun 按钮板，正在仔细查看这个设备时，他注意到它是基于 ATMega328 微控制器的。由于他喜欢使用 MIDI，他认为按钮垫将会成为一个[光滑而紧凑的独立 MIDI 控制器](http://www.beat707.com/forum/viewtopic.php?f=2&t=72)。

由于他的最终目标是创造一个除了电源插头和 MIDI 接口之外的完全独立的控制器，这迫使他与 ATMega 芯片密切合作。他和他的合作伙伴花了大量时间解决一些串行通信问题，以便在操作过程中不阻塞 led 或 MIDI 块计时器。当你在构建一个 MIDI 定时器时，确保 Arduino 不会阻塞任何其他功能显然是很重要的，看起来[古伊列梅]在他的探索中成功了。

正如你在下面的视频中看到的，MIDI 控制器工作得非常好，干得好！

[https://www.youtube.com/embed/G3KBr0tJkug?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G3KBr0tJkug?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[https://www.youtube.com/embed/x4dpsLtee7k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/x4dpsLtee7k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) [https://www.youtube.com/embed/eESTo3ySTPk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eESTo3ySTPk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
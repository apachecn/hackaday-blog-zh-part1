# 罗兰 808 同步到 MIDI

> 原文：<https://hackaday.com/2011/09/20/roland-808-synced-to-midi/>

![](img/26598e13d1eeb6d51d5aff70124743aa.png "808")

在阅读本周的 ATtiny 主题建筑时，[Thomas]想起了他最酷的建筑之一。他的 [midi808](http://www.stepinfusion.com/projects/midi808/) 项目使用 ATtiny2313 将一台老式罗兰 808 鼓机同步到他的逻辑工作站。

尽管 MIDI 在 808 诞生的几年前就已经出现了，但 808 的 CPU 还不能完全胜任处理 MIDI 的任务。相反，808 使用了一个被称为 [DIN Sync](http://machines.hyperreal.org/features/before-midi.html#sync) 的接口，该接口旨在保持 808、707 和 303 相互同步。MIDI 到 DIN 同步盒 ~~do~~ 确实存在，但即使是使用 an 808 的辅助设备也越来越难找到。

构建采用 MIDI 信号，并根据 MIDI 规范将其通过光隔离器。微控制器读取 MIDI 信号，并通过 DIN 同步端口将其传递出去。DIN 同步协议是每季度仅 24 个脉冲，带 TTL 电压的音符输出，[项目代码](http://www.stepinfusion.com/projects/midi808/midi.c)很容易理解。对于有史以来最伟大的鼓机之一来说，这是一个很好的构造。休息之后，听听[托马斯]用他的新设备制作的一首歌曲。

[https://w.soundcloud.com/player/?url=http%3A%2F%2Fsoundcloud.com%2Fuser8245903%2Fmidi808&width=false&height=false&auto_play=false&hide_related=false&visual=false&show_comments=false&color=false&show_user=false&show_reposts=false](https://w.soundcloud.com/player/?url=http%3A%2F%2Fsoundcloud.com%2Fuser8245903%2Fmidi808&width=false&height=false&auto_play=false&hide_related=false&visual=false&show_comments=false&color=false&show_user=false&show_reposts=false)
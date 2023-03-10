# MIDI Synth Arduino 盾

> 原文：<https://hackaday.com/2011/12/17/midi-synth-arduino-shield/>

![](img/1f46bbefe3a368bb063ba419d937e480.png "synt")

使用 MIDI 和 Arduino 有无数种方法。让一个 duino 向 MIDI 键盘吐出一个音阶，或者甚至响应 SysEx 消息来改变一个灯光或效果装置都是微不足道的。不过，有一件事一直困扰着 MIDI-duino 的开发者:用 DIY 盾实现一个 MIDI 合成器。那么，[基思]为他的[AvecSynth](http://www.kickstarter.com/projects/24311020/avecsynth-an-arduino-form-factor-midi-music-synthe)项目提供 Kickstarter 是一件好事。

[Keith]的 AvecSynth 基于 [Dream.fr SAM2195](http://www.dream.fr/pdf/Serie2000/SAM_Datasheets/SAM2195.pdf) 单芯片 MIDI 合成器。这是一个整洁的小 IC，从音序器或键盘接收 MIDI 信息，并输出立体声音频。AvecSynth 采用这种 IC，并将其放在标准的 Arduino 大小的封装中，因此建造一架巨大的灯光，脚动钢琴现在是周末焊接爱好者的视野之内。

虽然 SAM2195 和 AvecSynth 没有花哨的减法或 FM 合成，但它拥有通用 MIDI 规范中的全套 128 种声部。玩 MIDI 是一个很棒的项目，DIY 套件的价格正好符合我们的胃口。

编辑:[Keith]将他的 Kickstarter 的 20 美元奖励改为 PCB *或*两个 SAM2195 芯片
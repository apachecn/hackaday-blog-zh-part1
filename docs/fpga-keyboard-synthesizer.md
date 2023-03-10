# FPGA 键盘合成器

> 原文：<https://hackaday.com/2010/01/01/fpga-keyboard-synthesizer/>

![](img/4ab22f86ed9f839ac51a3532a41e2ae4.png "fpga-keyboard-synth")

[该合成器](http://instruct1.cit.cornell.edu/courses/ece576/FinalProjects/f2009/csm44_jck46/index.html)仅依靠 FPGA 进行按键检测和声音合成。[Chris]和[Joe]为他们在康奈尔大学的最终项目建造了它。硬件实现包括按键的速度感测。静止时，每个键接触一条铜箔。当按键被按下时，匹配的箔条接触按键。通过检测键何时离开静止状态并到达按下状态来推断速度数据。声音合成在硬件中使用[卡普勒斯-强弦合成](http://en.wikipedia.org/wiki/Karplus-Strong_string_synthesis)方法进行处理。如果你想听听它听起来像什么，他们已经[发布了一个视频](http://instruct1.cit.cornell.edu/courses/ece576/FinalProjects/f2009/csm44_jck46/KeyboardSynth1.MP4) (MP4)来展示这个创作。对我们来说它听起来像一架电子钢琴，所以任务完成了。
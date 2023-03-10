# 更新:Arduino 移位寄存器 PWM 获得速度提升

> 原文：<https://hackaday.com/2011/07/26/update-arduino-shift-register-pwm-gets-speed-boost/>

![](img/97ae669da780f95a1ada2d4568dd6c9b.png "768-pwm-from-arduino-now faster")

社区协作是一件伟大的事情。以移位寄存器的 Arduino PWM 库为例。Arduino 论坛上的一些人参与进来，通过使用循环进位指令帮助[Elco]削减了许多时钟周期。现在，他已经将每个移位寄存器的开销从 108 减少到仅仅 43。到目前为止，这并不意味着更多可能的输出——768 仍然很多——但当使用最大输出时，这是否意味着更好的精度。这有效地将 768 个 led 的亮度从 16 个增加到 32 个。

我们不知道该链接到哪里。[Elco]为图书馆设计了新的一页。有最初的[论坛帖子](http://arduino.cc/forum/index.php/topic,66988.30.html)，但是我们没有看到太多的兴趣。我们在[这篇 Reddit 帖子](http://www.reddit.com/r/electronics/comments/iycpf/thanks_for_your_input_shiftpwm_is_now_more_than/)的评论中发现了一些东西。当然，如果你不知道我们在谈论什么，回过头来读读最初的专题。
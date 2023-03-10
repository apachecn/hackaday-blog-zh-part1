# 第三次是一个魅力——512 LED 立方体用 RGB LEDs 将其提升了一个档次

> 原文：<https://hackaday.com/2011/03/20/third-times-a-charm-512-led-cube-kicks-it-up-a-notch-with-rgb-leds/>

![rgb_led_cube](img/d51769d61f22117683dd6101edbda7be.png "rgb_led_cube")

在我们前几天的 512 LED 立方体帖子的评论部分，一些人建议将该项目提升一个档次，使用 RGB LEDS 构建一个类似的立方体是下一个合乎逻辑的步骤。看起来一天一次的读者[vespine] [走在了曲线的前面](http://vespine.com/p/8x8x8-rgb-led-cube.html)，因为他在[的另一个故事](http://hackaday.com/2011/03/18/512-led-cube-again/)发表后不久就给我们发来了他的 8x8x8 RGB 立方体的构建细节。

他的立方体于今年早些时候完成，使用了 512 个 10 毫米 RGB LEDs，排列在一个简单的高架支架上。支架隐藏了他用来控制立方体的所有电路，其中的核心是 PIC32 MCU。十几个 TLC5940 16 通道 PWM 驱动器与 PIC 一起使用，以调整 led 的颜色输出，每个 led 都可以单独寻址和着色。

最终的结果会和你想象的一样惊人。他创作了几个快速演示动画，你可以在下面的视频中看到。一定要去他的网站看看他所有的建造细节——那里有很多。

[https://www.youtube.com/embed/6nO3STwoFjY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/6nO3STwoFjY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
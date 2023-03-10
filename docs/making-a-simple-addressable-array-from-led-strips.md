# 用 LED 条制作简单的可寻址阵列

> 原文：<https://hackaday.com/2011/09/28/making-a-simple-addressable-array-from-led-strips/>

![led_array_from_led_strips](img/b4f8a4c5632ecaf87f8819ed121fdf96.png "led_array_from_led_strips")

[Patrick]正在为他心中的一些未来项目做准备，为此他需要一个简单的可寻址发光二极管 2D 阵列。虽然他当然有可能构建自己的 LED 阵列和控制硬件，但他想尝试一些现成的产品，看看是否有适合他的需求。

他从 Adafruit 拿起一条可寻址的 RGB LEDs，虽然它们工作得很好，但对于他知道他需要的 led 数量来说，它们有点太贵了。他拿起一条没有内置 PWM 功能的类似 LED，旋转了一下——它们工作得足够好，所以他开始构建他的 LED 阵列。

虽然 LED 灯条可能不是制作 LED 阵列的最佳方式，但如果你焊接几根电线来连接不连贯的灯条，它们可以很容易地切割和重新排列，不会有任何问题。[Patrick]就是这么做的，并编写了一个小的 Arduino 库，允许轻松控制网格。

我们不确定他是否计划将这些阵列扩展到 8×8 以上，但我们绝对有兴趣看看他为这些阵列准备了什么。

看看下面他的 LED 阵列的快速视频。

[https://www.youtube.com/embed/ZU8kQ_tv0C4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZU8kQ_tv0C4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
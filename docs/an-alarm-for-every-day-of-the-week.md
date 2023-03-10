# 一周中每一天的闹钟

> 原文：<https://hackaday.com/2011/05/19/an-alarm-for-every-day-of-the-week/>

![](img/2ed049be9f3fdece385e12dc83b62731.png "alarm-for-every-day-of-the-week")

如果你没有一份朝九晚五的工作，你可能会发现自己会随着日程安排的变化而不断调整闹钟。[卢卡斯]终于厌倦了每晚的例行公事，决定打造自己的[闹钟，它对一周的每一天都有独特的设置](http://elcoyotequesuelda.blogspot.com/2011/04/despertador-v2-mucho-mucho-mejor.html) ( [翻译](http://translate.google.com/translate?js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&sl=auto&tl=en&u=http%3A%2F%2Felcoyotequesuelda.blogspot.com%2F2011%2F04%2Fdespertador-v2-mucho-mucho-mejor.html))。

显示器本身是一个 LM044L 20×4 字符显示器。这提供了大约 3”x1”的观看区域，并且由于它是 HD44780 兼容的 LCD 屏幕，因此与图形 LCD 相比，向其写入数据花费很少的精力(和 RAM)。PIC 18F2550 驱动该设备，从六个按钮接收输入，驱动显示器，并在起床时间到来时打开内置的蜂鸣器。有一个备用电池，断电时可以保持设置。每日闹铃、当前时间和背光亮度都可以从构成设置菜单的四个屏幕中进行调整。它唯一缺少的是一个精确的计时器，但应该很容易通过测量电源频率或使用 RTC 芯片来添加。
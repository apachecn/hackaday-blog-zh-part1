# 为寒冷黑暗的冬天早晨准备的日出钟

> 原文：<https://hackaday.com/2011/10/01/a-sunrise-clock-for-those-cold-dark-winter-mornings/>

![sunrise_alarm_clock](img/20b0ffc33537a8448d53a48b1dad6eb3.png "sunrise_alarm_clock")

对于大多数职场人士来说，北半球秋冬季的到来意味着一件事——在太阳升起之前早早醒来，开始一天的工作。来自亚特兰大 Freeside 的 Brent 非常了解这一规律，他决定给自己做一个日出闹钟，试图在黑暗的早晨让自己更自然地醒来。

他买了各种不同颜色的发光二极管，包括蓝色、红色、黄色和白色，还有一些紫外线二极管。他用这种 led 阵列的目的是模拟日出的自然颜色，而不是简单地慢慢照亮房间。该时钟使用 DS1307 RTC 来记录时间，Arduino 的任务是在[Brent]起床前大约 25 分钟点亮 led。

他说这看起来很有效，在收音机闹钟响起之前轻轻唤醒他的身体。它肯定比响亮的蜂鸣器强！
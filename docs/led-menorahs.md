# LED 烛台

> 原文：<https://hackaday.com/2008/11/09/led-menorahs/>

万圣节刚过，人们已经在设计下一款基于 LED 的节日装饰品了。对于光明节， [Gizmodo](http://www.mahalo.com/Gizmodo "Gizmodo - Mahalo") 指出了上图中的 [PCB 烛台](http://gizmodo.com/5081302/led-motherboard-menorah-is-hanukkah-20 "LED Motherboard Menorah Is Hanukkah 2.0")。它使用一组 DIP 开关来控制哪些 led 被点亮。几年前，邪恶疯狂科学家实验室为[制作一个更小的 LED 烛台](http://www.evilmadscientist.com/article.php/ledholiday "Evil Mad Scientist Laboratories - How to make high-tech LED decorations for the holidays")编写了一个教程。九个 led 中的每一个都直接焊接到 ATtiny2313 微控制器的引脚上。每次打开设备电源时，都会有一个额外的 LED 灯亮起。[Ori]喜欢这个项目，决定采用[稍微不同的方法](http://www.diyhappy.com/led-menorah-2/ "happy » LED Menorah")。他使用了 LM3914 DIP18 LED 条形驱动器。电位计控制发光二极管的点亮数量。
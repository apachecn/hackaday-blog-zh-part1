# 电子喷壶

> 原文：<https://hackaday.com/2011/02/07/electronic-watering-can/>

![](img/5b543d75cbd61e1b82b4f5e590c771a6.png "collage")

当[Deddies lab]想要给他们的(相当大的)天琴树适当浇水时，他们遵循他们的座右铭，在上面插上一个微控制器，并迅速制造出一个电子喷壶。

整个事情从电源开始，电源由传统的机械灯定时器每天打开一次，持续 15 分钟，并连接到 atmega8 微控制器，该微控制器在 1MHz 下运行，使计数器递增 1。当计数器达到 7 时，泵上的巨型开关打开，每周从桶式蓄水池中拿出大约半升水来浇灌植物，根据文章的计算，这应该持续大约 4 个月。

为了确保水泵不会缺水，一只橡皮鸭被系在一根细绳上，另一端被系在一个微型开关上，当水位过低时，细绳被拉动，将微型控制器的一个引脚切换到低电平。

虽然我们同意它可以使用一个低水指标，这是微不足道的，总的来说，该项目代表了一个伟大的黑客在一个星期天使用现有的零件和材料。休息之后，请加入我们，观看一个快速视频！

[https://www.youtube.com/embed/x0YKamxX-mE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/x0YKamxX-mE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
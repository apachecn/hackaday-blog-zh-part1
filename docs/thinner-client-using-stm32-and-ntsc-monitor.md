# 使用 STM32 和 NTSC 监视器的瘦客户机

> 原文：<https://hackaday.com/2010/09/29/thinner-client-using-stm32-and-ntsc-monitor/>

![](img/4b8bce77ae7d5694fa94ed21755064ea.png "Back Camera")

在(马克斯·洛博夫斯基)的帮助下，[设法建立了一个瘦客户机](http://www.davidcranor.com/David_Cranor/Projects/Entries/2010/8/31_Thinner_Client.html#6)，它使用 NTSC 电视作为显示器，价格仅为 6 美元。这是他第一次涉足 ARM 架构领域，他发誓再也不会使用 AVR。强大的小芯片使用定时器来管理同步和 DMA，以将完整的 480×240 帧缓冲区传输到屏幕。80 MHz 的超频在这个小主板上有很大的潜力，他计划在他的下一个技巧中接受全彩色显示器的挑战。
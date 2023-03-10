# 悬赏总线盗版功能，获得免费的 V2 印刷电路板

> 原文：<https://hackaday.com/2009/03/25/bounty-on-bus-pirate-features-get-a-free-v2-pcb/>

![bpv2](img/82feb979278b90e86bedd0e0b818625d.png "bpv2")

我们悬赏两个高优先级的[巴士海盗](http://buspirate.com/)功能。你可以通过写一点代码为即将到来的巴士海盗 V2 获得一个免费的 PCB。Hack a Day 拥有各种各样才华横溢的读者群，我们知道有人有经验以最小的困难做出这些改变。

*   最新的代码集成了 PIC24F bootloader，无需程序员即可轻松更新。我们想添加一个协议监听器，但这需要中断。然而，使用引导装载程序，中断被重新定位，我们还没有完全掌握它是如何工作的。我们将向第一个修改代码的人发送 PCB 和 PIC 24F，以演示 UART、SPI 或引导加载程序的更改通知中断。Microchip 的 24F bootloader app note 在[这里](http://www.microchip.com/stellent/idcplg?IdcService=SS_GET_PAGE&nodeId=1824&appnote=en533906)有。**完成**。

*   当前频率测量功能是一个使用计数器和定时器的黑客。成为第一个实现输入捕获外设的人，并获得免费 PCB。参见 *base.c* 中的函数 *bpFreq(void)* 。 **完成。**

最新的总线盗版代码和编译的固件可以从[谷歌代码 SVN](http://code.google.com/p/the-bus-pirate/) 中查看。通过下面的评论或者 buspirate@hackaday.com[提交你的代码。](mailto:buspirate@hackaday.com)

更新:两个问题都已解决。谢谢你的建议。
# AVR 高压救援屏蔽

> 原文：<https://hackaday.com/2009/03/13/avr-hv-rescue-shield/>

![rescueshield](img/62d5cbac476d36ad032740838a8bce48.png "rescueshield")

在玩 ATmega168 时，[Jeff]对 [RSTDISBL 熔丝位](http://mightyohm.com/blog/2008/09/i-programmed-the-rstdisbl-fuse/)进行了编程。这使得芯片在大多数情况下都没有用。[杰夫]不想放弃它，所以[他建立了一个系统，使用很少使用的高电压并行编程模式](http://mightyohm.com/blog/2009/03/introducing-the-avr-hv-rescue-shield/)对它进行编程。他用了一个 Arduino，几行代码和几个备件来制作它。在与一些程序员同事分享了这个想法后，他决定专门为此制作一个 Arduino 盾牌。你可以用它来重置几乎所有的保险丝来拯救芯片。如果你是一个死忠 AVR 的人，从来没有开始使用 Arduino 代替， [STK500](http://hackaday.com/2009/03/08/stk500-as-an-arduino/) 实际上有这个内置。
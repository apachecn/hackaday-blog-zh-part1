# AVR RFID 标签

> 原文：<https://hackaday.com/2009/06/27/avr-rfid-tag/>

[pc486]在他的黑客中发送说[使用 ATtiny85 来充当 EM4102，一种用于 RFID 标签的芯片](http://scanlime.org/2008/09/using-an-avr-as-an-rfid-tag/)。最低限度，所有需要的是 AVR 和一个线圈，但他建议一些滤波电容。根据线圈的大小，可以获得不同的频率和范围。这个项目实际上包括几个黑客，如使用线圈不仅为电力，但一个时钟信号。由于连接引脚上的箝位二极管，线圈实际上能够在不连接到电源引脚的情况下为芯片供电。固件很短，但是可以在 [subversion](http://svn.navi.cx/misc/trunk/avrfid/) 上获得。

相关:[刮刮卡 RFID 标签](http://hackaday.com/2008/11/11/scratch-built-rfid-tags/)
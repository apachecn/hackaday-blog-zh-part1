# 价值 10 美元零件的频率计数器

> 原文：<https://hackaday.com/2011/03/14/frequency-counter-for-10-worth-of-parts/>

[Scott] [用不到 10 美元的零件制造了这个频率计数器](http://www.swharden.com/blog/2011-03-14-frequency-counter-finished/)。它被设置为以兆赫计的频率，这是合适的，因为他计划将其用于[的无线电硬件实验](http://hackaday.com/2010/11/27/barcode-challenge-for-radio-operators/)。但我们会发现它也很有用，因为我们廉价的万用表只能读取 4 MHz 左右的频率。

他用的是手头的 ATmega16，但它的功能远远超出了该设备的规格。他推测阿提尼 2313 将很容易取代它的位置。微控制器主要用于从他正在使用的 74LV8154 计数器芯片读取频率值后驱动多路复用 7 段显示器。他没有该装置的完整原理图，但有一张使用频率计数器的手绘示意图；剩下的应该很容易拼凑起来。看一下这个电路，我们不认为让它成为一个手动范围频率计数器会太难，这样可以让你更好地利用这个专用器件。查看文件夹下方嵌入的[Scott 的]演示视频。

[https://www.youtube.com/embed/KduEGjvXaeY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KduEGjvXaeY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
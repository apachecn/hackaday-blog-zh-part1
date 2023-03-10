# AVR 微控制器上输出引脚的硬件 XOR

> 原文：<https://hackaday.com/2011/07/09/hardware-xor-for-output-pins-on-avr-microcontrollers/>

您知道吗，就输出引脚的逻辑电平而言，大多数 AVR 芯片都有一种硬件异或(XOR)选项。如果你查看数据手册(上图是 ATtiny13 数据手册的截图)，你会发现一个关于切换引脚的章节。事实证明，如果将一个端口设置为输出，将逻辑 1 写入相应的引脚寄存器将会切换该输出的逻辑电平。如果你是用 C 语言写的，这很容易被忽略，但是我一直在学习汇编语言，并且发现这非常有用。休息后继续阅读，我会告诉你我是如何得到这个信息的，以及它有什么好处。

首先，让我们来谈谈为什么如果你是用 C 代码写的话，这并不重要。通常，如果您想切换某些输出引脚，只需编写一行代码，用位掩码进行异或运算:

```
PORTB ^= 0xFF;
```

这有点像 C 语言的简写(从我的教程系列中了解更多关于 T0 的内容)，它对当前的输出电平执行 XOR 运算，并将结果写回端口。但是通过将位掩码写入 PINB 寄存器，同样的事情可以在硬件中完成:

```
PINB = 0xFF;
```

你不会真的在乎，因为这只是一行代码。事实上，对 PORTB 进行 XOR 可能更容易，因为它在概念上更有意义。但是编译器最终使用的周期可能会比写入 PIN 寄存器时多。

我偶然发现了这个功能，因为我正在闪烁一些 led 作为学习汇编程序的一种方式。我在一个中断服务例程中有这样一段混乱的代码:

```
ldi myReg, 0xFF
in intReg, PORTB
eor intReg, myReg
out PORTB, intReg
```

它将一个位掩码加载到一个寄存器中，将当前逻辑从 PORTB 加载到另一个寄存器中，对两者执行 XOR 运算，并将结果写回 PORTB。这需要四个周期，并需要两个寄存器。切换位是如此基本的操作，以至于我很惊讶竟然没有直接异或位的命令，所以我开始四处搜索。[我在 AVR Freaks 上看到了这篇文章](http://www.avrfreaks.net/index.php?name=PNphpBB2&file=viewtopic&t=83904&start=0),这篇文章让我了解了位切换功能。现在，我可以将我的汇编代码简化如下:

```
ldi intReg2, 0xFF	;temporarity use intReg2 as a bit mask
out PINB, intReg2	;writing to PINB effectivley does an Exclusive OR on PORTB
```

这导致相同的切换效果，但只需要两个周期，并且只需要使用一个寄存器。

我发现最有趣的是，无论我用了多少 AVR 芯片，数据手册中总有惊喜等着我去发现。
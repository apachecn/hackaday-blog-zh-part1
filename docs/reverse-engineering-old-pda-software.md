# 逆向工程老 PDA 软件

> 原文：<https://hackaday.com/2012/03/13/reverse-engineering-old-pda-software/>

![](img/a2eb9144fe2792b75f03037faddf0f68.png "reverse-engineering-old-pdas")

[Troy Wright]购买了 20 台损坏的戴尔 Axim PDAs。这种类型的硬件在十年前非常流行，但与现代手机相比就显得过时了。这就是为什么他能以低价买到它们。经过一点工作，他设法复活了八个单位，但沮丧地发现没有公开的方法来控制软件的背光。出于某种原因，这对他的项目来说是一个障碍。但他知道这是可能的，因为有一些应用程序可以设置背光等级。于是他[通过对软件](http://people.sdev-group.com/twright/?p=26)进行逆向工程，发现了如何做到这一点。

诀窍是掌握代码。因为它不是开源的[Troy]使用了 [IDA](http://www.hex-rays.com/products/ida/index.shtml) ，一个图形化的反汇编和调试套件。他知道自己在寻找什么，因为 Windows CE 开发人员文档确实提到了一种独立于显示驱动程序直接控制图形硬件的方法。几个小时的汇编语言摸索、断点设置和测试最终让他找到了解决方案。
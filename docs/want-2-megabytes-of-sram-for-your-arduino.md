# 想要 2 兆的 SRAM 给你的 Arduino？

> 原文：<https://hackaday.com/2011/09/07/want-2-megabytes-of-sram-for-your-arduino/>

![](img/91b56444d6c973c125fbc5257d1ba96c.png "cpld-adds-sram-to-arduino")

你到底需要多大的内存？我们认为我们真的没有资格评判你如何在你的项目中滥用内存。但是我们确实很欣赏[Eric Rogers]使用的干净有序的技术来[向一个 Arduino](http://majolsurf.net/wordpress/?page_id=1001)添加多个 SPI SRAM 芯片。

重物的提升是通过一个叫做 [Amani 64](http://majolsurf.net/wordpress/?page_id=368) 的 CPLD 防护罩来完成的。它拦截从 Arduino 到 SRAM 芯片的 SPI 调用，并转换地址信息以在 23K256 个器件的集合中找到适当的数据。这些芯片价格低廉，使用多个芯片比选择单个 SPI 可寻址芯片和更大的存储器尺寸节省成本。

最棒的是，CPLD 的灵活性允许[Eric]设计一个寻址系统，利用 Arduino 的 SPI 数据传输功能中未使用的位。当使用单个 23K256 芯片时，有四个写功能，总共浪费六位。他设计了一种方法，将寻址数据注入这些未使用的位，使他能够寻址多达 64 个不同的存储芯片，潜在的存储容量为 2 MB。CPLD 取出注入的地址，随后写入或读取 SRAM 芯片库。

寻找其他 SRAM 升级选项？这是另一个使用[多路复用来减少添加内存](http://hackaday.com/2011/09/05/upgrading-ram-in-an-arduino-mega/)所需的地址线的例子。
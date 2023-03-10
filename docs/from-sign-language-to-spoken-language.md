# 从手语到口语

> 原文：<https://hackaday.com/2010/10/04/from-sign-language-to-spoken-language/>

作为一个生物医学工程班的高级设计项目的一部分，[Kendall Lowrey]在一个团队中开发了一种将美国手语翻译成英语口语的设备。想要超越在他们之前的[基于手套的设备](http://hackaday.com/2010/05/10/more-glove-based-interfaces/)，这个团队开始从严格的拼写单词转向将手势与普通手势相结合。该项目基于 Arduino Mega，由于初始编程空间的限制，仅限于字母表和大约十个单词。当五个柔性传感器和三个加速度计值记录了两秒钟的静止状态时，设备读取读数并在表格中查找最可能的单词或字母。然后它输出到[一个语音屏蔽](http://www.sparkfun.com/commerce/product_info.php?products_id=9799)把单词或字母翻译成语音。
# 双电压电源

> 原文：<https://hackaday.com/2009/09/14/dual-voltage-power-supply/>

![dual_regualted_power](img/554990d5b1ac00a6ba0e320cb3ecc2f7.png "dual_regualted_power")

[Melanie]这个周末有时间，所以她用手头的零件做了一个双电压电源。这种设计直接插入试验板，不像[我们看到的最后一个试验板电源](http://hackaday.com/2009/08/25/regulated-breadboard-psu/)，一次提供两个电压。5v 电压输送到一条电源总线，而 3.3v 电压输送到另一条总线。她的设计使用来自 [LF00 系列](http://www.st.com/stonline/books/pdf/docs/2574.pdf) (PDF 数据手册)的两个线性低压降稳压器来实现这一点。干得好！
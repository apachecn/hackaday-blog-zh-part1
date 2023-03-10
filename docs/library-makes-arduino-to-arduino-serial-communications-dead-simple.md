# 库使得 Arduino 到 Arduino 串行通信非常简单

> 原文：<https://hackaday.com/2011/05/31/library-makes-arduino-to-arduino-serial-communications-dead-simple/>

当[比尔·波特]从事一个项目时，他说他通常会编写自己的 NMEA 标准通信协议来适应手头的工作。虽然这使得故障诊断变得容易，但他承认他的定制协议既浪费处理器时间又浪费带宽。另一方面，二进制通信更有效，但管理起来有点棘手。

为了方便普通用户，[他编写了一个名为 EasyTransfer](http://www.billporter.info/easytransfer-arduino-library/) 的库，它抽象了两个 Arduino 板之间的打包串行通信。这个过程非常简单——你所要做的就是在两个 Arduino 板上定义一个数据结构，这样它们就知道什么样的数据通过线路传输，剩下的由 EasyTransfer 处理。这使得用户更少担心通信协议或传输错误，而是专注于他们的项目。

如果你正在做一个项目，并且正在寻找一个简单的方法让一对 Arduinos 说话，那么请访问他的网站并使用这个库。不会变得更容易。
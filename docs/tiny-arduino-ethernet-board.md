# 微型 Arduino 以太网板

> 原文：<https://hackaday.com/2008/10/17/tiny-arduino-ethernet-board/>

![](img/e1aff2b42ce02b2f3464556ce8e41cf4.png "tiny")

[sgk]制造了这个[微型以太网板](http://www.switch-science.com/trac/wiki/W5100-SPI-en "W5100-SPI-en – スイッチサイエンス – Trac")用于 Arduino。它基于一个 [WIZnet W5100](http://www.wiznet.co.kr/en/) 芯片。芯片处理所有的 TCP/IP 通信，你通过 SPI 与它对话。它兼容标准的 Arduino [以太网库](http://arduino.cc/en/Reference/Ethernet "Arduino - Ethernet")。[sgk]手工焊接这些电路板，包括 80 引脚 LQFP 主芯片。他的下一个项目是将 AVR 和 W5100 全部[放在同一块板子](http://www.switch-science.com/trac/wiki/AVR-W5100 "AVR-W5100 – スイッチサイエンス – Trac")上。虽然听起来他会使用大于 1005 的组件。
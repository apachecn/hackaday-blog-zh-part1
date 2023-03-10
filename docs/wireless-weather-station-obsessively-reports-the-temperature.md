# 无线气象站痴迷地报告温度

> 原文：<https://hackaday.com/2011/03/15/wireless-weather-station-obsessively-reports-the-temperature/>

![obsessive_weather_station](img/7f19a2c69a4dadef8bc29c04f71cd80d.png "obsessive_weather_station")

[努米奥]一直在努力建立一个推特气象站，他最近才开始运作。气象站由三个主要组件组成，一台用于数据存储和发布的 Linux PC，一个主要的气象传感器单元和一个远程单元。

远程单元位于室外，包括压力和湿度/温度传感器。传感器每 20 秒轮询一次，通过 434 MHz 射频收发器向主机报告数据。遥感器还记录周围的光线水平和剩余的电池电压，将数据发送到主单元进行良好的测量。

主单元位于他的房子内部，并记录与外部单元相同的温度和湿度数据。主单元将其数据添加到远程单元发送的数据包中，并通过 USB 将其传输到 PC。PC 计算过去 12 小时和 24 小时的最低和最高温度，然后将数据发送回主设备，并显示在其 LCD 面板上。每隔 10 分钟，电脑还会在推特上发布天气数据。

如果你想建立自己的气象站，[numio]已经在他的网页上提供了他的项目的所有源代码。然而，他确实承认他太懒了，没有画出一个示意图，所以在那个部门你只能靠你自己了。
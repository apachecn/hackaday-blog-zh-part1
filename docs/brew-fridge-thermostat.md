# 酿造冰箱恒温器

> 原文：<https://hackaday.com/2009/03/22/brew-fridge-thermostat/>

![thermostat-1](img/80fd4eea1b8e6fb6ab13b53aa4a9182a.png "thermostat-1")

读者[Will R]为他的 brew 冰箱发送了一个[恒温器模型。他的朋友发现了一个非常好的酒吧冰箱，想把它重新用于酿造啤酒。之前的一批微酿啤酒被澳大利亚的高温烤坏了，所以他们想要一些能保持完美温度的东西。冰箱的内置恒温器不会升到 5 度以上，所以他们必须自己制造。[威尔]用 10K NTC 热敏电阻测量温度。它连接到 ATtiny25 微控制器，该微控制器进行比较并确定是否打开压缩机。他参考了 SparkFun 的](http://aliask.googlepages.com/fridgethermostat "aliask - thermostat")[接力教程](http://hackaday.com/2008/12/05/working-with-relays/ "Working with relays  - Hack a Day")的切换端。虽然他没有为这个项目蚀刻电路板，但设计文件和所有代码都包含在项目网站上。
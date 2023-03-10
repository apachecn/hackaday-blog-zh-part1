# I2C Arduino 全球定位系统盾

> 原文：<https://hackaday.com/2011/05/24/i2c-arduino-gps-shield/>

![i2c_gps_shield](img/a69f8459ff7d36b40984f9ee735c199e.png "i2c_gps_shield")

[Wayne]写来分享他刚刚完成的一个项目，[一个用于 Arduino](http://www.dsscircuits.com/articles/i2c-gps-shield.html) 的 I ² C GPS 防护罩。虽然其他 GPS 解决方案已经存在了一段时间，但他的解决方案由于其功能列表而引起了我们的注意。

该盾牌消除了与解析来自传统 GPS 插件的原始 NMEA 数据相关的麻烦。虽然您可以选择通过串行与 GPS 模块通信以获取原始数据，但使用 I ² C 接口可以轻松获取最常用的 GPS 数据。GPS 模块本身可以设置为以 1 到 10 赫兹的频率更新，Wayne 说 I ² C 总线破坏了常用的 9600 波特串行接口。虽然 I ² C 主要用于接收数据，但它也可以通过其控制寄存器来配置 GPS，允许即时调整设置。

虽然[Wayne]确实以有竞争力的价格出售预组装的单元，但他也提供了完整的原理图，一旦您找到合适的组件，这将是一个轻松的下午项目。
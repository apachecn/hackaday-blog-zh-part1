# 电容传感器指南(AD7746)

> 原文：<https://hackaday.com/2009/07/18/capacitance-sensor-guide-ad7746/>

![capacitive_sensor](img/16046e959d07718bcc5b1cd8c0d05ea7.png "capacitive_sensor")

[Marcus]写下了他使用 AD7746 电容传感器的[体验。他将](http://interactive-matter.org/2009/07/arduino-ad7746/ "Arduino & AD7746 | Interactive Matter") [SparkFun 分线板](http://www.sparkfun.com/commerce/product_info.php?products_id=7918)与 Arduino 结合使用。现有的 Arduino 代码不是很好，所以他重写了代码以便更容易理解。AD7746 是一款 I2C 器件，可以连续读取，但这与布线库不太匹配。此外，数据手册中的校准程序很难理解。他包括了他使用的所有代码，加上一个处理草图，以帮助可视化的输入，这将有望使你的芯片体验更加顺畅。
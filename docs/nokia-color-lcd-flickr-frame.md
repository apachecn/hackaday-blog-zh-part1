# 诺基亚彩色液晶 Flickr 相框

> 原文：<https://hackaday.com/2008/06/16/nokia-color-lcd-flickr-frame/>

Tinkerlog 从 SparkFun 那里得到了一个[彩色液晶显示器，并将其设置为](http://www.sparkfun.com/commerce/product_info.php?products_id=569)[接收来自 Flickr](http://tinkerlog.com/2008/06/14/flickr-images-on-a-nokia-lcd/) 的图像。这些彩色液晶显示器为 128×128 像素，包括一个分线板，带有独立的背光电源。通信通过三线式 SPI 总线和复位线进行。[Alex]使用 ATmega48 进行控制，使用 RS232 转 USB 转换器连接到计算机。接线示意图这里是[这里是](http://www.flickr.com/photos/8123185@N02/2576938951/)。

对于软件方面的事情，他将 Sparkfun 的示例 ATmega8 代码用于微控制器(他无法让 Arduino 代码工作)。Beej 的 Python Flickr API 被用来抓取图像。 [Python 映像库](http://www.pythonware.com/products/pil/)对它们进行转换，最后使用 [pySerial](http://pyserial.sourceforge.net/) 发送到显示器。SparkFun 提供这些展示已经有一段时间了；很高兴看到一个正在使用的高质量的文章。

[通过[创建 Flickr 池](http://www.flickr.com/groups/make/pool/)

*   [永久链接](http://tinkerlog.com/2008/06/14/flickr-images-on-a-nokia-lcd/)
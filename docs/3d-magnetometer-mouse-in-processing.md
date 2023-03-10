# 3D 磁力计鼠标正在处理中

> 原文：<https://hackaday.com/2009/10/18/3d-magnetometer-mouse-in-processing/>

![FFB4SV5G0SD7J7G_MEDIUM](img/0a603a9d0a83f32ecb2747e5856c6cfc.png "FFB4SV5G0SD7J7G_MEDIUM")

[etgalim]在 Solidworks 中工作广泛，想要一种更直观的方式在屏幕上旋转对象。为了做到这一点，他[创造了一种能对旋转做出反应的鼠标](http://www.sparkfun.com/commerce/product_info.php?products_id=8656)。他将一个 3D [罗盘模块](http://www.sparkfun.com/commerce/product_info.php?products_id=8656)放入一只旧鼠标中，并将其连接到 Arduino 上。Arduino 然后将 I2C 传感器数据转发给计算机。到目前为止，他有一个使用鼠标旋转立方体的处理脚本，但最终他想编写一个 Solidworks 插件。这有点不稳定，我们认为如果他使用像 [jedipad](http://hackaday.com/2007/12/23/the-jedipad-aka-uber-gyro-mouse/) 那样的[陀螺仪](http://www.sparkfun.com/commerce/product_info.php?products_id=9373)，会更平稳(也更便宜)。跳跃后的视频。

[https://www.youtube.com/embed/4PgvRAeuIrk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/4PgvRAeuIrk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
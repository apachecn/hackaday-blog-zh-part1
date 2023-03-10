# Wii MotionPlus + Arduino

> 原文：<https://hackaday.com/2009/06/23/wii-motionplus-arduino/>

![wiimoteplus](img/5394f3d549bddd2472bd76ff80a4316e.png "wiimoteplus")

[knuckles904]能够通过 Arduino 使用新的 [Wii MotionPlus](http://www.mahalo.com/wii-motionplus) 。为了更好地检测控制器的运动，任天堂发布了 WM+。Wiimote 只能检测加速度，而 WM+可以检测沿 3 个轴的旋转。Arduino 通过 I2C 与它通信，双截棍使用的是同样的协议。为了连接这两个设备，他使用了跳线，但也可以使用[分线点](http://www.hvwtech.com/products_view.asp?ProductID=1081) [板](http://store.fungizmos.com/index.php?main_page=product_info&cPath=69&products_id=212)。在 wiibrew.org[的帮助下，他能够创建一些](http://wiibrew.org/wiki/Wiimote/Extension_Controllers#Wii_Motion_Plus)[示例代码](http://randomhacksofboredom.blogspot.com/2009/06/wii-motion-plus-arduino-love.html)。当与包含三轴加速度计的双截棍配对时，你可以以不到 40 美元的价格拥有一个 6 自由度的 IMU，非常适合用于控制机器人的 [或记录数据的](http://hackaday.com/2008/12/17/wii-nunchuck-controlled-servo-bot/)。

[途径 [adafruit](http://www.adafruit.com/blog/2009/06/23/wii-motion-plus-arduino-love/)
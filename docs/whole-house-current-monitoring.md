# 全屋电流监控

> 原文：<https://hackaday.com/2010/07/07/whole-house-current-monitoring/>

[https://www.youtube.com/embed/HlRBrTTLQFU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HlRBrTTLQFU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[Debraj Deb]组装了一个电流监控设备，与他家的电路盒连接。该系统由 PIC 18F4520 控制，使用 LM358 运算放大器对交流信号进行整流，并使用 MCP6S21 进行范围调整，以检测高或低电流负载。字符 LCD 上显示的数据包括平均值、 [RMS](http://en.wikipedia.org/wiki/Root_mean_square) 和峰值电流。目前，数据保存在 EEPROM 中，可以通过串行连接转储，但[Debraj]计划添加一个 GSM 调制解调器，这样他就可以将能源使用数据发送到他的手机上。

[谢谢加内什]
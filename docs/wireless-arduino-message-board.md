# 无线 Arduino 留言板

> 原文：<https://hackaday.com/2011/02/08/wireless-arduino-message-board/>

![arduino_message_board](img/8124777dd4dc919b265a631f3e6bf2e1.png "arduino_message_board")

[uhclem]正在寻找一种新颖而简单的方法来提醒他的孩子做家务，他没有使用一系列的便利贴，而是构建了一个漂亮的[无线 Arduino 供电的留言板](http://www.instructables.com/id/A-Wirelessly-Controlled-Arduino-Powered-Message-B/)。留言板由 Arduino Pro 供电，并通过一对 1 系列 Xbee 无线电与他的计算机通信，这些无线电将一系列录音信息转发到连接的 VFD。他将所有组件安装在一个旧雪茄盒中，并将其安装在墙上，形成一个不错的整体展示。

信息的编程不需要任何特殊的软件，因为用户界面由 Arduino 处理并通过标准的终端会话访问。[uhclem]提到，his 代码在运行时几乎消耗了设备的所有 RAM，因此他在 Arduino 的闪存中保存了一些固定信息，以便在需要时调用。可选的 EEPROM 也允许将消息流式传输到器件。
# 有没有想过很酷的互动博物馆展品来自哪里？

> 原文：<https://hackaday.com/2011/08/09/ever-wonder-where-cool-interactive-museum-exhibits-come-from/>

![](img/166ab2a1c5bdaa8b5818ba1a190cbd28.png "building-interactive-museum-displays")

[Victor]的女朋友在一家博物馆工作，利用他的专业知识为参观博物馆的孩子们设计了一款互动侦探游戏。愿景是让孩子们发现电话号码，他们可以打电话寻求线索。最初他计划在字符 LCD 上显示线索，但显然在电话听筒里听到线索更简洁。

很快，Victor 放弃了 ATtiny2313，用 Xmega 芯片重新开始——事实上，是我们最近的 Xmega 帖子启发了他记录他的项目。微控制器负责许多事情。它扫描输入的按键矩阵，模拟 DTMF 按键音，从 SD 卡上的 FAT 文件系统中读取音频文件，并通过手机的扬声器播放它们。由于大部分硬件已经内置在手机中，所以将他的附加设备安装在外壳中并不困难。一个简单的音频放大器电路与微控制器相连，微控制器与键盘的行和列相连。休息后看看视频，看看这个设备的运行情况。

【维梅奥 http://vimeo.com/27451012 w = 470】
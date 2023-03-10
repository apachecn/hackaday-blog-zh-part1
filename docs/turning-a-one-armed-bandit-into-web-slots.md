# 把独臂强盗变成吃角子老虎

> 原文：<https://hackaday.com/2011/01/12/turning-a-one-armed-bandit-into-web-slots/>

![](img/cdfcab08beb00fccd9da675ea981682b.png "real-slot-machine-arduino")

[Kyle Kroskey]刚刚完成了他的第一个 Arduino 项目，[为老虎机](http://757labs.org/wiki/Projects/inetslotmachine)添加 web 控件。他以 IGT S+模型开始，这种模型多年来在拉斯维加斯和大西洋城赌场非常流行，但现在正被更现代的版本所取代。他的伟大想法是修改机器，使其可以从个人电脑上控制，然后释放一个直播流，使互联网可以播放。

事实证明这并不太难，他只是在 Arduino 上安装了几个控件；用于最大化赌注金额的按钮，以及测量硬币投入和支出的传感器。为了保持和平，他断开了扬声器，但将音频重新路由到 PC，以便可以通过流媒体播放。这确保了房间里的安静，而不牺牲在线乐趣。PC 运行 Ubuntu 并控制视频馈送，这是一个在机器上方详细显示头奖数据的屏幕，并便于将网页播放器请求传递给 Arduino 以控制机器。

另一个有趣的吃角子老虎机黑客，看看这个[游戏设备变成酒保](http://hackaday.com/2010/10/07/nyc-resistor-takes-on-the-machine/)。
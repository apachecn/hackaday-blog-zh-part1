# 理光相机的快门遥控器

> 原文：<https://hackaday.com/2010/12/31/shutter-remote-for-ricoh-cameras/>

![](img/82cf874576d6d83b7c3d4a5ebbabc7e0.png "shutter-remote-for-ricoh-cameras")

[Toby]想为他的理光 GR III 相机安装一个遥控快门触发器。这个品牌没有用于远程操作的专用端口，但是一点点[的研究让他可以建造自己的触发器](http://infar.be/index.php?/archives/765-Arduino-as-a-remote-shutter-release-for-RICOH-cameras.html)。相机的 USB 端口用于触发，但不使用 USB 协议。相反，5V 线路上的脉冲模式识别快门按钮的半按下、全按下和释放状态。从那时起，它只是一个围绕 Arduino 的电路问题，这为扩展到像[照片自动化](http://hackaday.com/2010/09/24/full-featured-avr-time-lapse/)这样的领域留下了空间。
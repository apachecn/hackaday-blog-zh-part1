# Wii 双截棍控制的 Pleo

> 原文：<https://hackaday.com/2009/04/24/wii-nunchuck-controlled-pleo/>

[https://www.youtube.com/embed/1pcAsEUOW9Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1pcAsEUOW9Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[Andy]来信向我们展示了他如何黑掉他的 Pleo，让它被 Wii 双截棍控制。他安装了 Xbee 单元进行通信，并编写了一个“短剧”，允许 Pleo 只是站在那里等待命令。他使用 Arduino 来解释 Nunchuck 输入并将其发送到 Pleo。这是一个非常酷的概念验证，但是响应时间非常慢。这可能是由于 Arduino 的串行通信速度较慢。是的，我们说过你可能不想黑他们，因为他们的[即将灭绝](http://hackaday.com/2009/04/21/ugobe-files-for-bankruptcy/)，但是你期望我们坚持这一点吗？如果你要钻研一个，你可能也会对[如何破解 Pleo 进行人脸识别和远程控制](http://hackaday.com/2008/08/07/hacking-pleo-for-face-recognition-and-remote-control/)感兴趣。
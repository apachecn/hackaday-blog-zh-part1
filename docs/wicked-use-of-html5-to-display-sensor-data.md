# 恶意使用 HTML5 显示传感器数据

> 原文：<https://hackaday.com/2011/10/25/wicked-use-of-html5-to-display-sensor-data/>

这个项目向您展示了一种可能的方式来使用 HTML5 将来自微控制器的传感器数据完全集成到我们的技术生活中。现在，当我们通过收件箱看到这个提示时，我们认为这将是一个值得学习的有趣例子，但是我们还没有准备好这个设置有多酷。休息后看一下视频，你会看到扫描项目框上的二维码将立即开始 10 毫秒分辨率的加速度计数据直播。此外，手机加载的浏览器页面允许您只需轻触一个按钮，就可以将当前正在查看的内容发送到另一台计算机上运行的浏览器的主框架中。通过这种方式，您可以构建一个流式传感器数据的仪表板。谈论家庭自动化的未来。想象一下，你的恒温器上有一个二维码，只需拍一张照片，你就可以访问你家的暖气、空调、加湿器和热水器的性能和控制？天空是这一个的限制，所以通过留下评论让我们知道你将使用它做什么。

在这种情况下，mbed 微控制器处理数据采集，并使用 [WebSockets 库](http://mbed.org/cookbook/Websockets)通过 WiFly 模块将其推送到服务器。这些数据以 JSON 包的形式推送，由服务器以数据流的形式分发。客户端可以通过浏览器访问使用 JavaScript 的页面。

[https://www.youtube.com/embed/JlLfKJ6ZLmw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JlLfKJ6ZLmw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢西蒙]
# 短信远程启动为您的旧智能手机注入新的活力

> 原文：<https://hackaday.com/2011/12/18/sms-remote-start-gives-new-life-to-your-old-smartphone/>

![iphone-sms-remote-start](img/347f2069f0fa56161a7e746afc9ef831.png "iphone-sms-remote-start")

Hack a Day 校友(Will O'Brien)最近升级了他的手机，并试图为他的旧手机找到一种用途。他一直想为他的斯巴鲁 Outback 远程启动器，但没有兴趣支付现成的套件。由于他有这部旧智能手机，他认为这将是一个由短信触发的远程启动系统的完美起点。

他从破解他的手机开始，这允许他运行一些 Perl 脚本来监听输入的文本。他使用 Sparkfun 的 PodBreakout mini 将手机连接到 Arduino，Arduino 负责触发汽车的点火。现在，一条包含启动命令和密码的简单短信就可以在世界任何地方启动他的汽车。

虽然[Will]对他的设置非常满意，但他已经有了改进的想法，包括 Arduino 通过短信向他发送消息，确认汽车已经成功启动。他正在考虑为其他人组装一个工具包，为他们自己的汽车添加相同的功能，所以一定要定期查看他的网站，了解项目更新。
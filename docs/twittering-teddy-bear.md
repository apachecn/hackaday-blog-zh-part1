# 叽叽喳喳泰迪熊

> 原文：<https://hackaday.com/2008/06/16/twittering-teddy-bear/>

这可能是杀死[纳巴兹塔格](http://www.mahalo.com/Nabaztag)的致命一击:使用文本到语音转换软件，这只[电子熊大声并实时地说出一条推特流](http://2pointhome.com/diys/steps/45620)。

我家 2.0 的大师们用一个加载了定制软件的 Arduino 取代了它的集成电路板，让熊说话了。添加了蓝牙音频适配器作为熊的声音通道，并添加了带有 H 桥芯片的电路来解决电源问题。Arduino 将输入的音频信号转换为动作。从那里，该过程转移到给熊提供音频数据的计算机，他们解析 Twitter 流，并使用 OSX 内置的“说”命令来生成语音流，通过蓝牙发送给熊。

*   [永久链接](http://2pointhome.com/diys/steps/45620)
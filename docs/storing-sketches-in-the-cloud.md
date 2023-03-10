# 在云端存储草图

> 原文：<https://hackaday.com/2012/03/16/storing-sketches-in-the-cloud/>

![](img/d6a7b69ed72338f23cc743f4823ee4b0.png "Git")

解决不存在的问题和解决在找到解决方案之前没有人认识到的问题之间只有一线之隔。前者出现在深夜电视购物节目中兜售的家庭用品上，而后者被[亨利·福特]总结为:“如果我问人们想要什么，他们会说是更快的马。”[Dave]将微控制器代码存储在云端的方法绝对属于“有用”一类。

[戴夫]第一次意识到这个问题是在他挖掘视频玩具实验室的时候，他发现了一个孤儿项目，一个芭比信用卡刷卡器。[Dave]不知道这个项目的固件是否保存在服务器上，甚至不知道当前版本是否可用。解决这个问题的一个方法是将源文件的副本刻录到板上的 Flash 或 EEPROM 中。

不过，这种想法有一个问题:将源代码存储在 Arduino 的内存中会占用空间。横向思考，[Dave]意识到编辑源代码发生在计算机上，计算机连接到互联网，所以为什么不把源代码保存在“云中？”

[Dave]的解决方案是将源代码放在 GitHub 上，并将每段代码绑定到一个电路板的唯一 USB 序列号上。这给了每个 Arduno 一个唯一的 ID，允许版本控制和多个文件的库。

This very clever addition to the Arduino IDE is [up on GitHub](https://github.com/davidvondle/Upload-And-Retrieve-Source), ready to be added to any Arduino installation. Why the Arduino IDE doesn’t already have this feature is beyond us, but that’s what you get when you want a faster horse.
# 用 Steak 测试开源 PID 控制器

> 原文：<https://hackaday.com/2012/03/12/testing-an-open-source-pid-controller-with-steak/>

![](img/258a5ce25616ab95bf30312a6c5f0391.png "PID")

Sous vide 炊具并不是什么新东西，但[Phil]想用 osPID 建造第一个 [sous vide，这是上个月刚刚发布的开源 PID 控制器。](http://www.unmaintained.com/index.php/ospid-sous-vide-open-source-high-tech-cooking-on-a-budget/)

该构建使用了我们上周看到的 osPID 开源 PID 控制器，它带有热电偶输入和一对能够切换热板或浸没式加热器的继电器。osPID 基于 Arduino，由 [Arduino PID 库](http://arduino.cc/playground/Code/PIDLibrary)的作者【Brett Beauregard】创建。

为了得到建筑的肉和土豆，[Phil]将一个 300 瓦的浸入式加热器连接到 osPID 上，并将加热器放入一碗水中。一块看起来很美味的牛里脊肉被塞进一个自封袋，在一碗温水中悬浮几个小时。将加热器和热电偶连接到 osPID，温度设置为 130°F，并将整个器件放置几个小时。看着[菲尔]的柠檬欧芹黄油里脊食谱刺激了我们的味蕾，所以我们希望[菲尔]的晚餐做得不错。
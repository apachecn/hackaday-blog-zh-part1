# 无线 Arduino 猫粮分配器

> 原文：<https://hackaday.com/2009/06/24/wireless-arduino-cat-food-dispenser/>

![catfooddispenser](img/76b71e48a78e8d1c2064a8032330238e.png "catfooddispenser")

读者[Andres Leon]有两只可爱的猫，它们有非常特殊的饮食需求。他没有改变自己的时间表，而是戴上了他的帽子，设计了一个非常坚固的猫粮分配器。分配器由一个带槽的旋转滚筒和一个 PVC 管 Y 形配件组成，用于均匀分配食物。这台机器的大脑是一个 Arduino Deumillanove 和一个 XBee 模块。该单元可以通过网络界面控制，也可以完全独立运行。[安德烈斯]遇到了一个问题，鼓的转动阻力根据里面有多少食物而变化。他用一个聪明的激光位置指示器解决了这个问题。一块胶合板与顶部的插槽对齐，这样每当插槽朝上时，它都可以防止激光照射到光敏电阻上。猫起初害怕伺服噪音，但现在它们一听到就跑向它们的碗。
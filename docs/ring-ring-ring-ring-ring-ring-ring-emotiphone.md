# 铃声响铃声响铃声响手机！

> 原文：<https://hackaday.com/2011/06/25/ring-ring-ring-ring-ring-ring-ring-emotiphone/>

![emotiphone](img/d24e63233fd1b6f20474e1b1c648c246.png "emotiphone")

Instructables 用户[zvizvi]正在为他的工业设计学校申请整理一个文件夹，他认为将曾经属于他祖母的一部旧旋转电话重新利用起来会很棒。

他最初对这款手机有着非常崇高的目标，但最终缩减了他的愿景，将单向通信纳入 Twitter。在拆除了手机不必要的部件后，他忙着在拨号器的指孔后面安装发光二极管。这些 led 连接到一个 MCP23017 I/O 扩展器，它从他塞进手机外壳的 Arduino 接收方向。

当接收器从支架上提起时，Arduino 会通过他安装的 WiFly 盾启动与互联网的连接。一旦他拨了一个号码，Arduino 就会把这个数字翻译成一个预定义的表情符号，发布到他的 Twitter 页面上。虽然这些表情符号不像我们本周早些时候报道的 Roomba 发来的信息那样具有描述性，但它们很好地传达了他的心情。

这是一个有趣的项目，而且它恰巧让[zvizvi]进入了他申请的设计学校，所以我们不能要求更多。
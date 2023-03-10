# 自动水族箱化学分配器非常精确

> 原文：<https://hackaday.com/2011/08/14/automated-aquarium-chemical-dispenser-is-extremely-precise/>

![precision_doser_nano_doser_espresso_pump](img/ff3f458e7f24f235c3c53bf33837f594.png "precision_doser_nano_doser_espresso_pump")

[Robovergne]为自己在家中建立的美丽珊瑚礁水族馆感到自豪。由于活珊瑚对矿物质的需求，这些种类的水显示器需要不断的维护。与其手动添加矿物质溶液，他决定[用浓缩咖啡机泵](http://www.robovergne.com/fr/electro/guiguidoseur/) ( [谷歌翻译](http://translate.google.com/translate?js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&sl=fr&tl=en&u=http%3A%2F%2Fwww.robovergne.com%2Ffr%2Felectro%2Fguiguidoseur%2F))制造一个纳米剂量器。

这些振动泵依靠电源电压运行，所以他有几个选择来控制它们。使用继电器可能会使事情变得非常嘈杂，所以他选择使用过零检测电路来精确控制泵的占空比和输出。

他的设置使用 PIC 来控制从过零电路到液晶显示器的一切。通过安装在控制箱前部的几个按钮输入产品数量和配送时间，让 PIC 来完成繁重的工作。它将根据几个因素计算运行泵的适当时间长度，包括流体粘度和释放高度。

这确实是一个令人印象深刻的系统，虽然他的需求非常精确，但我们想象这种设置在构建不太复杂的分配器时会非常有用，例如在自动化酒吧中发现的那些。

继续阅读，看看他的纳米剂量器的几个视频。

[https://www.youtube.com/embed/Kzyzu_yyVp8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Kzyzu_yyVp8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[https://www.youtube.com/embed/k4KfTLjnx9U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/k4KfTLjnx9U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)
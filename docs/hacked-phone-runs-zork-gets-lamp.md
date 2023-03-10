# 被黑的电话运行 Zork，得到灯

> 原文：<https://hackaday.com/2011/05/25/hacked-phone-runs-zork-gets-lamp/>

![](img/c76107fb7358a478062d0dd5f59f8a17.png "grue")

几个月前，[Ulysses]想到了一个在 TDD 上运行 Zork 的项目。尽管为湾区创客节及时准备好这个项目有点困难，但附带的 [build 博客](http://dial-a-grue.com/gory/)告诉我们这是值得努力的。

在将手机的内部连接到 Arduino Pro 后，调制解调器被修改，以便声学耦合的 TDD 可以被接口。虽然 TDD 显示器只有一行，但[尤利西斯]仅以 45.5 波特的速度传输文本，因此即使最慢的读者也能跟上故事的进度。为了运行实际代码，最初尝试使用 Arduino Pro，后来又使用 Arduino Mega，但由于这些 AVR 中 sram 的限制，这些尝试都没有成功。在放弃了在 Arduino 上运行 Zork 的想法后，这个项目用安装在手机内部的单板 FitPC 计算机完成。

该项目的代码在[的一个端口上运行](http://ifarchive.org/indexes/if-archiveXinfocomXinterpretersXzip.html)[Zork](http://en.wikipedia.org/wiki/Zork)Infocom Z-code 解释程序，或 ZIP。许多交互式文本冒险以 Z-code 格式发布，所以我们猜测让这个项目运行*火卫一的皮革女神*或令人惊叹的[银河系漫游指南](http://www.douglasadams.com/creations/infocomjava.html)会是微不足道的。这是一个非常好的项目，我们可以很容易地看到自己在这个项目中坐下来，在周六晚上喝一瓶两升的 Shasta，听一盘 all-Rush 混音带。
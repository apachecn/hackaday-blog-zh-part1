# 防御战第一天——迷失在翻译中——克里斯蒂安·格罗托夫

> 原文：<https://hackaday.com/2005/07/29/defcon-day-1-lost-in-translation-christian-grothoff/>

隐写术是一种在众目睽睽之下隐藏东西的艺术。当操作正确时，观察者不应该能够分辨出有隐藏的信息，这与密码学相反，在密码学中很明显有东西被隐藏了。为了使用文本做到这一点，你通常需要一大块原始材料；说出莎士比亚所有的作品。由于这些作品为大多数人所知，因此通常可以使用统计分析来破解。

Christian 的解决方案是使用机器翻译(MT)文本作为源材料。很难让计算机生成语义和修辞一致的正确文本，模仿原文是非常困难的。这里介绍的技术使用机器翻译文本，因为翻译错误是意料之中的，也是常见的。

对于这种技术，源文本甚至不必是秘密的。它首先通过几个机器翻译引擎(即 Babelfish)运行文本。为了增加可能的翻译数量，每一个都要经过另一种算法，这种算法使用单词替换和其他技术来创建更多的排列。然后逐句检查这些文本，以确定它们在统计上是否仍然接近原始译文，以确保译文看起来是可能的。

此时，使用霍夫曼树编码对消息进行编码。一旦完成，可以应用一些后处理错误插入。这利用了通常出现在机器翻译中的错误:误用的冠词、介词和不翻译不太常见的单词。甚至还有“语义替换”的技术，这里有一个例子:将一个单词从英语(en)翻译成德语(DE)，然后将该单词翻译成 en，然后再翻译回 DE，如果这个 DE 单词是原始 EN 单词的可能翻译，他们将使用 DE 单词。对于统计分析来说，这种迂回的转换不如一对一的替换那样清晰。

这种隐写方法有几个缺点:比特率低，而且你必须传输源文本和翻译文本。也有一些攻击暴露了这种方法。如果同一个句子在一篇文章中出现两次，并被翻译成两种不同的方式，这将引发一个危险信号。同样，如果机器错误不一致:在一个地方用“foots ”,在另一个地方用“feets”。如果有人开发了所有机器翻译系统的大型统计模型，很容易看出隐写术不符合模型，但隐写术也可以使用该模型来确保它符合模型(军备竞赛)。

如果你想玩的话，网站上有一个发电机。

*   [永久链接](http://www.cs.purdue.edu/homes/rstutsma/stego)
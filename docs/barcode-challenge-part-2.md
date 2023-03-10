# 条形码挑战–第 2 部分

> 原文：<https://hackaday.com/2009/10/08/barcode-challenge-part-2/>

![HaD_barcode](img/24d1442ae54b197af4cf2eb56426c86b.png "HaD_barcode")

昨天，我们发布了[条形码挑战赛](http://hackaday.com/2009/10/07/barcode-challenge/)，以纪念条形码的诞生。祝贺[ [号]赢得这次挑战。](http://www.wtfmoogle.com/)[他的提交材料](http://hackaday.com/2009/10/07/barcode-challenge/#comment-99457)非常详细地解释了他是如何使用 Photoshop、OpenOffice Calc 和一些网络资源解决这个难题的。休息之后我们会有详细的报道。

荣誉奖颁给了推出 Java 解决方案的[nex]和展示 Python 解决方案的[和](http://www.jwmaag.org/)[的](http://hackaday.com/2009/10/07/barcode-challenge/#comment-99743)。最后，向所有以这样或那样的方式使用 CueCat 解码字符串的人致敬。只要有一个还在身边就很恐怖了。

由于条形码扫描仪和在线图像翻译程序无处不在，这个挑战可能有点太容易了。你认为你准备好迎接更大的挑战了吗？[下载新条形码](http://hackaday.com/files/2009/10/barcode_challenge_part_2.jpg)并开始工作。这个应该更难破译。再一次，留下包括条形码中存储的信息的评论。请记住，只有解决难题并包括完整过程描述的条目才会被考虑。祝你好运，让比赛开始吧。

**更新:**[仅用了【JP】19 分钟就发布了新条形码的正确解决方案](http://hackaday.com/2009/10/08/barcode-challenge-part-2/#comment-99776)。干得好！

[[Moogle 的](http://www.wtfmoogle.com/)获奖方案:

![pattern_counting_binary](img/035abd98198fbe82e072c78aeb55a0ba.png "pattern_counting_binary")

首先，[Moogle]在 Photoshop 中打开条形码，放大，并在下面添加一个线条网格，以帮助读取二进制代码。红色标记用于帮助划分数据块。

![open_office_calc_binary](img/bb34468ffb921534c0bbbb14d661b356.png "open_office_calc_binary")

然后将图像放入电子表格程序(在这种情况下是 OpenOffice Calc ),并用手读出每个块的二进制代码。

![the_solution](img/c37631058df66d3b3f775c4d38a24fc4.png "the_solution")

他格式化了二进制文件，以确保他没有出错，然后使用一个查找表来查找[代码 128](http://en.wikipedia.org/wiki/Code_128) 以从每个数据块中生成字符。

干得好！这个解决方案是用每个人都有的并且知道如何使用的工具来执行的。
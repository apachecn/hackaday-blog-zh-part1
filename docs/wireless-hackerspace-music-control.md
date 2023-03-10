# 无线黑客空间音乐控制

> 原文：<https://hackaday.com/2011/10/12/wireless-hackerspace-music-control/>

![skipbutton_bitlair.nl](img/674e6327026e3284aa9ba7f3f2df8942.png "skipbutton_bitlair.nl")

总部位于荷兰的 Bitlair hackerspace [的工作人员热爱他们的音乐](https://wiki.bitlair.nl/Pages/Skipbutton)，并使用 mpd 和 fookebox 为他们的工作室设置了一个数字点唱机。一群不同的人在一个地方工作，你会遇到的一个问题是，每个人对音乐都有自己独特的品味。Dubstep 有节奏的“wub wub wub wub”可能对一些人来说很棒，而其他人则试图在捂着耳朵的同时焊接。为了确保每个人都能不时地行使音乐否决权(就像洛杉矶帝国唱片公司)，他们建立了一个 Skipbutton，允许成员改变正在播放的内容。

该按钮允许用户跳到队列中的下一首歌曲。以及控制空间音响系统的音量。它使用 Arduino pro mini 来运行节目，使用 433 MHz 发射机向 mpd 守护程序发送信号。Bitlair 相当大，他们经常花时间在户外，所以他们必须确保 Skipbutton 无论在哪里都能工作。为了做到这一点，他们在接收端建造了一个八木天线，以确保无论从哪里触发按钮，按钮都可以正常工作。

如果你有兴趣为你的家或黑客空间制作一个类似的系统，可以看看他们的 wiki 所有的代码和原理图都可供使用。
# 示波器钢琴调音 101

> 原文：<https://hackaday.com/2011/04/17/oscilloscope-piano-tuning-101/>

[![fft on scope](img/37a6b8415f93bb19a8b061bf8b7d2be3.png "scope fft")](http://hackaday.com/2011/04/17/oscilloscope-piano-tuning-101/scope-fft-custom/)

[Todd Harrison]最近写信告诉我们他提交给泰克示波器大赛的参赛作品-[使用示波器调音钢琴](http://mytektronixscope.com/videos/?bcpid=782299138001&bckey=AQ~~,AAAArH1tTNE~,ee1_EMk3RMrmNYoZtYY_3PLuqzUzvk8X&bclid=790226492001&bctid=877505509001)。在他的视频中，他演示了如何使用快速傅立叶变换来确定正在演奏的音符的基频。这是确定该键是否在调上，以及如果不在调上，它离期望频率有多远以及在哪个方向上的一种快速且容易的方法。

他继续解释说，示波器只能作为一个开始的参考点，因为在钢琴上“数学上正确”的调音听起来不太对人的耳朵。事实证明，当受到撞击时，钢琴中被拉伸的金属丝表现得并不理想。就钢琴而言，泛音(示波器上显示的频率高于基频的其他峰值)实际上比基频的预期谐波整数倍略高(频率更高)。因此，每个八度音程的频率范围必须被“拉伸”,以适应这种情况，并在多个音符跨八度音程一起演奏时声音正确。

典型地，只有 A4 键实际上被调谐到其正确的频率 440Hz，而所有其他键都被手动调谐偏离该基线。应用于每个八度音程的必要拉伸量随着您在两个方向上远离该初始参考点而增加，并且对于每个乐器都是独特的，因此没有能够完美调音的通用设备。虽然[Todd]承认他不会尝试用这种技术自己调音整架钢琴，但他发现这是一种方便的方法，可以在专业调音之间保持钢琴最重的中央部分更接近真实。

如果您对 Techtronix 示波器有任何有趣或独特的用途，您可以在此参加竞赛[。别忘了](http://mytektronixscope.com/)[也给我们](http://hackaday.com/contact-hack-a-day/)通风报信！谢谢[托德]！
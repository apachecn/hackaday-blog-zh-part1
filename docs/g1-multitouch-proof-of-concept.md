# G1 多点触控概念验证

> 原文：<https://hackaday.com/2008/11/23/g1-multitouch-proof-of-concept/>

[https://www.youtube.com/embed/pSBYqmWVqeM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pSBYqmWVqeM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[RyeBrye]一直试图让基于安卓系统的[T-Mobile G1](http://www.mahalo.com/G1_Hacks "T Mobile G1 - Mahalo")上的[多点触摸](http://hackaday.com/tag/multitouch/)工作。他入侵了 Synaptics 触摸屏驱动程序，这样它就会[将原始事件信息转储到角色设备](http://www.ryebrye.com/blog/2008/11/22/g1-multitouch-proof-of-concept-video/ "G1 Multitouch Proof-of-Concept Video")。上面的演示使用了来自 Google 的 fingerpaint 程序的示例代码。轮询设备不是最快的方法，但[RyeBrye]只是想得到一个演示来证明这是可行的。
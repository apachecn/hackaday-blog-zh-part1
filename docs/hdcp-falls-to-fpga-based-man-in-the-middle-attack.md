# HDCP 遭遇基于 FPGA 的中间人攻击

> 原文：<https://hackaday.com/2011/11/30/hdcp-falls-to-fpga-based-man-in-the-middle-attack/>

![fpga-hdcp-maninthemiddle-attack](img/706892532d59ae0b43020396d50fd5ec.png "fpga-hdcp-maninthemiddle-attack")

我们在这里谈论 HDCP 已经有一段时间了，但是数字内容保护领域最近的发展非常有趣。

你可能还记得去年 HDCP 加密的[主密钥被泄露，就在英特尔宣布](http://hackaday.com/2010/09/24/the-hdcp-master-key/)[保护被破解后不久。](http://hackaday.com/2010/09/18/intel-high-bandwidth-digital-content-protection-cracked/)虽然英特尔承认 HDCP 遭到破坏，但他们对这些信息可能被用来拦截 HDCP 数据流的说法不屑一顾，因为他们声称这样做需要专用处理器。英特尔称，制造这样一个组件的过程成本极其高昂，希望以此来平息人们对这一主题的兴趣，但事情并没有按照他们的计划发展。

德国的研究人员似乎已经设计出一种方法，可以在极其合理的预算下制造出这样的处理器。为了实时实现 HDCP 解密，研究人员使用了标准的现成 Digilent Atlys Spartan-6 FPGA 开发板，该开发板配有 HDMI 输入/输出端口，可以轻松访问相关视频流。虽然不像我们几年前报道的这种 HDCP 变通方法那么便宜，但他们的解决方案应该比将 HDMI 电缆硬连接到电视机主板上灵活得多。

该团队声称，尽管他们的中间人攻击有效且不可检测，但对海盗来说几乎没有实际用途。虽然我们知道 HDMI 数据流会产生大量数据，但这种绝对化的说法会让我们发笑，因为从长远来看，它往往会适得其反。

[通过[汤姆的硬件](http://www.tomshardware.com/news/Blu-ray-HDMI-HDCP-Digilent-FPGA,14105.html)
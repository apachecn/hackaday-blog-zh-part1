# 易于使用的自动二维码生成器

> 原文：<https://hackaday.com/2011/10/16/easy-to-use-automatic-qr-code-generator/>

![custom_qr_code_generator](img/ecef51313a140d55aa3d3965cba36ad5.png "custom_qr_code_generator")

不管你喜不喜欢，世界上有很多人每天都在使用二维码。由于 hack aday reader[fall dear]认为它们非常棒，所以他认为组装一个自动二维码生成器用于网站会很酷。

受我们自己的【Brian bench off】完成的自定义 [QR 徽标嵌入工作的启发，他的动态 QR 码生成器允许您做同样的事情，但工作量要少得多。该代码要求您在服务器上安装 PHP 和 GD 库，但除此之外，他的代码会完成其他工作。](http://hackaday.com/2011/08/11/how-to-put-your-logo-in-a-qr-code/)

你所需要做的就是调用页面并传递一个 URL、可选的标题文本、可选的图像覆盖(将你的徽标添加到代码的中心)，以及一个可选的用于跟踪流量来源的散列代码。该页面提供了一个 png 图像，可以单独使用，也可以嵌入到博客中，这正是[fall dear]计划使用它的目的。

如果二维码是你的东西，一定要拿一份他的代码，这肯定会是一个方便的工具。
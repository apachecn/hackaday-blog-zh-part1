# 从命令行发微博

> 原文：<https://hackaday.com/2008/05/22/twittering-from-the-command-line/>

![](img/712de2a4f4168ec035067b6eb3c457ba.png)[Twitter](http://www.mahalo.com/Twitter) users often have trouble explaining just exactly what the service is for. The site specifically asks “What are you doing right now?” A simple interface and multiple ways to update means people have started hooking it to different real world objects… objects that aren’t reporting [what they had for lunch](http://foodfeed.us/). After the break, we’ll cover a couple devices that have interfaced Twitter to the real world and how you can update from your command line.

贾斯汀·威克特正在寻找一种通过手机控制房间灯光的方法。通过使用鲍勃·鲍韦的 iLink INSTEON 软件和 Twitter，他能够控制基本功能。现在，他可以发送类似“卧室关灯”这样的短信，软件会执行他的命令。当然，在发送和处理这个请求的时间里，你可以很容易地走过去关灯。我们确信他正在计划更多的功能。

![](img/5f3541c529503e61f593aa4e35c4d92f.png)

Adafruit Industries 正在出售一种叫做[botanicals Twitter kit](http://www.adafruit.com/index.php?main_page=product_info&cPath=25&products_id=93)的有趣设备。当你的植物需要水时，它会直接发布到 Twitter 上。使用湿度传感器和内置以太网端口，只需要一些基本的焊接就可以开始了。

![](img/caf52d2ee86f569fe28e2985afbbae55.png)
上图是 Ninja Networks 在 Defcon 上的喊话墙(图: [pinguino](http://flickr.com/photos/pinguino/1029128312/in/set-72157601257941651/) )。它接收和显示直接短信和 Twitter 更新。它还在躲避球上进行反向数字查找，以获得用户图标。使用带有数据线的爱立信 T39m，因为它提供了简单的 SMS 接口。把它带到一个聚会上，你的服务提供商肯定会奇怪你是如何在一个周末收到 4000 条入站 txt 消息的。

`curl --basic --user "$user:$pass" --data-ascii
"status=testing123" [http://twitter.com/statuses/update.json](http://twitter.com/statuses/update.json)`

If you want to strap twitter to your own project, it’s probably best to learn how to update from the command line. Dave Thomas with Linux Journal posted [how to do it using cURL](http://www.linuxjournal.com/content/twittering-command-line). It’s definitely an easy way to get your feet wet with the [Twitter API](http://twitter.com/help/api).

*   [永久链接](http://www.linuxjournal.com/content/twittering-command-line)
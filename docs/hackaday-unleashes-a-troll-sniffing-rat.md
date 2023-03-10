# 黑客日放出巨魔嗅鼠

> 原文：<https://hackaday.com/2010/12/19/hackaday-unleashes-a-troll-sniffing-rat/>

![](img/4728ce5b2b99ad8ab8655226e551cc42.png "troll-sniffing-rat")

有时候，我们喜欢从休闲日抽出几分钟时间和家人在一起。但是，就在你把目光从新来的评论上移开的时候，[巨魔](http://en.wikipedia.org/wiki/Troll_(Internet))一定会发起攻击。嗯，我和[Caleb]找到了一个解决问题的方法，那就是巨魔嗅鼠。这只小眼睛害虫坐在我的桌子上等着。当检测到一个拖拽评论时，它的眼睛会发出红光，并发出警报。休息之后加入我们，了解更多关于这个愚蠢项目的信息。

## 软件

要完成这件事，我需要做几件事。首先，一种解析我们收到的评论的方法。这很简单，我们使用 WordPress 作为我们的内容管理系统，这意味着已经有了一个全球评论的 RSS 源。我只需要获取这些数据，并遍历评论作者中已知的巨魔(没有被禁止)。使用 Python 脚本并不难做到这一点，尤其是如果您利用了净化和导航 HTML 和 XML 的[漂亮的汤模块](http://www.crummy.com/software/BeautifulSoup/)。我的脚本每两分钟检查一次提要，存储标识每个评论的编号以避免出现重复的警报，并根据评论的作者做出决定。一个简单的用户名列表被用来搜索巨魔，但它也可以被用来在你最喜欢的读者发表评论时发出通知。然后，脚本在标准输出上记录一条消息，并通过串行连接发送一条编码命令。

终端输出如下所示:

![](img/e18a4205ea75d8126abd6f68cc033a8b.png "troll-terminal")

这是 Python 脚本:

```
#!/usr/bin/python

trolls = [ 'Mike Szczys' , 'Caleb Kraft' ]
signalAllComments = True
signalAllAudibly = False

import urllib2, time, serial
from BeautifulSoup import BeautifulSoup

#start a list of comments to prevent duplicate alerts
dupe = []

#setup Arduino communications
ser = serial.Serial('/dev/ttyUSB0', 9600)

time.sleep(5)

#get list of comment identifiers
while True:

  #Reset Arduino from the last trigger
  ser.write('z');

  #Get the comments
  html = urllib2.urlopen(&quot;http://hackaday.com/comments/feed&quot;).read()
  soup = BeautifulSoup(html)

  #Check each one
  for item in soup('item'):
      thisID = item('guid')[0].string.split('comment-')[1]

      if thisID not in dupe:
              #Add to the duplicate list for next time
              dupe.append(thisID)

              #Convert post time to local time
              postT = item('pubdate')[0].string
              parsedT = time.strptime(postT, &quot;%a, %d %b %Y %H:%M:%S +0000&quot;)
              offsetT = time.mktime(parsedT) - time.timezone
              localPostTime = time.strftime(&quot;%m/%d/%y %H:%M:%S&quot;, time.localtime(offsetT))

              #Check if this is a post we're watching
              author = item('dc:creator')[0].string
              if author in trolls:
                  print &quot;(&quot; + localPostTime + &quot;) Troll Alert: &quot; + author + &quot; just posted a comment&quot;
                  print &quot;    &quot; + item('guid')[0].string
                  print
                  ser.write('a')
                  time.sleep(1)
              elif signalAllComments:
                  print &quot;(&quot; + localPostTime + &quot;) New Comment from: &quot; + author
                  print &quot;    &quot; + item('guid')[0].string
                  print
                  #audible signal?
                  if (signalAllAudibly):
                    ser.write('b')
                  time.sleep(1)

  time.sleep(120)
```

## 五金器具

接下来，我需要一种方法在解析脚本识别出巨魔时发出警报。在我看来，开发连接到计算机的硬件的最简单/最快的方法是使用通过 USB 连接的 Arduino。我有一个 Arduino，我从来没有在项目中使用过，所以我认为这将是一个很好的开始。我找出一个压电蜂鸣器和一些发光二极管，开始四处寻找可以重新利用的代码示例。

![](img/6a4e90bdb3244dc89c33c6f8f7b59ac6.png "troll-hardware")

我发现[有一个关于使用压电蜂鸣器](http://www.arduino.cc/cgi-bin/yabb2/YaBB.pl?num=1241248988)制作音乐的帖子，所以我修改了代码来制作我想要的声音。我还查看了 Arduino IDE 附带的串行通信示例，以启动和运行通信。就像我上面提到的，我通过串行连接从我的 Python 脚本发送一个 ASCII 字符。下面的草图只是寻找这些字符，并相应地采取行动。我可以让硬件点亮发光二极管，并在接收到“A”时播放不好的声音。当“B”出现时，它可以播放很好的声音，但对 led 没有任何影响。任何其他字母都会关闭 led，这是 Python 脚本在最后一个 troll 警报两分钟后重置 led 的原因。

```

//Piezo code from:
//http://www.arduino.cc/cgi-bin/yabb2/YaBB.pl?num=1241248988

void setup() {
  pinMode(7, OUTPUT);
  pinMode(8, OUTPUT);
  Serial.begin(9600);
}

#define PIEZO_PIN 8
// defines for the frequency of the notes (.5 x freq of mid C)
#define AN    220     // 440 Hz
#define AS    233     // 466 Hz
#define BN    247     // 493 Hz
#define CN    261     // 523 Hz
#define CS    277     // 554 Hz
#define DN    294     // 588 Hz
#define DS    311     // 622 Hz
#define EN    330     // 658 Hz
#define FN    349     // 698 Hz
#define FS    370     // 740 Hz
#define GN    392     // 784 Hz
#define GS    415     // 830 Hz
// defines for the duration of the notes (in ms)
#define wh    1024
#define h      512
#define dq     448
#define q      256
#define qt     170
#define de     192
#define e      128
#define et      85
#define oo7      1    // 007 jingle

/////////////////////////////////////////////////////////////

void play_tune(int tune){               // play a tune . . .
  switch (tune) {                       // a case for each tune
  case 1:
    for (unsigned char i=0; i&lt;4; i++)
    {
      ToneOut(FS*4,et);
      ToneOut(CN*4,et);
    }
    break;
  case 2:
    ToneOut(CN*8,e);
    delay(16);
    ToneOut(CN*8,e);
  }
}

void ToneOut(int pitch, int duration){  // pitch in Hz, duration in ms
  int delayPeriod;
  long cycles, i;

  //pinMode(PIEZO_PIN, OUTPUT);           // turn on output pin
  delayPeriod = (500000 / pitch) - 7;   // calc 1/2 period in us -7 for overhead
  cycles = ((long)pitch * (long)duration) / 1000; // calc. number of cycles for loop

  for (i=0; i&lt;= cycles; i++){           // play note for duration ms
    digitalWrite(PIEZO_PIN, HIGH);
    delayMicroseconds(delayPeriod);
    digitalWrite(PIEZO_PIN, LOW);
    delayMicroseconds(delayPeriod - 1); // - 1 to make up for digitaWrite overhead
  }
  //pinMode(PIEZO_PIN, INPUT);            // shut off pin to avoid noise from other operations
}

void loop() {

  if (Serial.available() &gt; 0) {
    int inByte = Serial.read();
    // do something different depending on the character received.
    // The switch statement expects single number values for each case;
    // in this exmaple, though, you're using single quotes to tell
    // the controller to get the ASCII value for the character.  For
    // example 'a' = 97, 'b' = 98, and so forth:

    switch (inByte) {
    case 'a':
      digitalWrite(7, HIGH);
      play_tune(1);
      break;
    case 'b':
      play_tune(2);
      break;
    default:
      digitalWrite(7, LOW);
    }
  }
}

```

拼图的最后一块是把两个红色发光二极管放在我们放在房子周围的一只长毛绒老鼠里面。眼睛是刺绣的，所以我把 LED 引线夹在一个角度，让它足够锋利，可以穿透到里面。我用 Dremel 打磨鼓使透明的 LED 封装变得模糊，并刮掉大部分多余的塑料。然后，我用我身边的几根 KK 连接器跳线连接到鼠头内部的导线上。在把填充物从身体里取出后，我把连接器一直推下去，然后把导线弯到连接器上。下面有这个的图片，但是没有弯曲的引线。

![](img/961d9e43e9b8e3c260ae37ac50017d24.png "troll-led-connection")

我给老鼠重新装上填料，并把我为了工作而切开的那条缝钉好。我喜欢这个结果。整个房子都能清晰地听到，我一路上都很开心。

事实证明，一个 8 美元的网络摄像头和一个 Ubuntu 盒子并不能构成一个很好的视频设置。但是如果你一定要看演示，这里就是:

[https://www.youtube.com/embed/eUNlzNo9tr8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/eUNlzNo9tr8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

## 在 Twitter 上关注我
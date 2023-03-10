# Arduino Arcade Rom Dumper

> 原文：<https://hackaday.com/2011/05/18/arduino-arcade-rom-dumper/>

![](img/0f6bd401689cb4fa660689daa15fb7a3.png "IMAGE_011")

[Vincenzo]想读一些 82S129 双极 proms，为什么不呢，它们在 20 世纪 80 年代的街机场景中非常常见。问题是，它现在是一个奇怪的球部分，通常只有(甚至)更昂贵的 EPROM 程序员可以读取它们。Arduino、试验板和一些快速脚本很快解决了这个 Arcade Rom 阅读器的问题。

你把 prom 插在你的试验板上，把它连接到 Arduino 的适当的端口和管脚上，Arduino 的位撞击 prom，并通过 Arduino 的串行连接返回结果。使用 pc 端的终端程序，您捕获文本，并使用脚本将 ascii 值转换为二进制半字节格式，并保存为十六进制格式。

这让我们更容易从旧的街机主板上扔掉 rom，因为你永远不知道你下次去废品站或废品场时会不会碰到旧的波利比乌斯街机主板。

休息后请加入我们，了解所有细节和一如既往的评论！

> ```
> 82S129 bipolar proms are very common in '80 Arcade Jamma boards. Unluckly, only more expensive EPROM programmers can read them. I used an Arduino Duemilanove to dump 82S129 contents to PC for backup use.
> 
> I used a breadboard to connect 82S129 pins to Arduino. Please follow this schematic:
> 
> 
> 
> Arduino pins  ------>  82S129 pin    (function)
> 
> +5v                    16              Vcc
> 
> GND                     8              GND
> 
> Digital 2               5              A0
> 
> Digital 3               6              A1
> 
> Digital 4               7              A2
> 
> Digital 5               4              A3
> 
> Digital 6               3              A4
> 
> Digital 7               2              A5
> 
> Digital 8               1              A6
> 
> Digital 9              15              A7
> 
> Digital 10             12              O1
> 
> Digital 11             11              O2
> 
> Digital 12             10              O3
> 
> Digital 13              9              O4
> 
> GND                    13              CE1
> 
> GND                    14              CE2
> 
> 
> 
> Here is pde program to send in Arduino:
> 
> 
> 
> 
> ```
> 
> 
> Begin pde program
> 
> ------------------------------------------------
> 
> /*
> 
>   82s129 Arduino reader
> 
>   By Vincenzo Femia (enzofemia@gmail.com)
> 
>  */
> 
> byte indirizzo=0;//&quot;indirizzo&quot; is Italian for &quot;address&quot; :-)
> 
> boolean a0=0;//address bits
> 
> boolean a1=0;
> 
> boolean a2=0;
> 
> boolean a3=0;
> 
> boolean a4=0;
> 
> boolean a5=0;
> 
> boolean a6=0;
> 
> boolean a7=0;
> 
> //
> 
> boolean o0=0;//data bits
> 
> boolean o1=0;
> 
> boolean o2=0;
> 
> boolean o3=0;
> 
> byte output=0;
> 
> void setup()
> 
> {
> 
> //pin0 &amp; pin1 reserved for serial communication
> 
>   pinMode(2,OUTPUT);//set pins for address
> 
>   pinMode(3,OUTPUT);
> 
>   pinMode(4,OUTPUT);
> 
>   pinMode(5,OUTPUT);
> 
>   pinMode(6,OUTPUT);
> 
>   pinMode(7,OUTPUT);
> 
>   pinMode(8,OUTPUT);
> 
>   pinMode(9,OUTPUT);
> 
>   pinMode(10,INPUT);//set pins for data (it's a nibble)
> 
>   pinMode(11,INPUT);
> 
>   pinMode(12,INPUT);
> 
>   pinMode(13,INPUT);
> 
> 
> 
> }
> 
> 
> 
> void loop()
> 
> {
> 
> 
> 
>     for (indirizzo=0; indirizzo&lt;256; indirizzo++)// from 00 to FF address
> 
>    {
> 
>     a0=bitRead(indirizzo,0);//read status bit of address...
> 
>     a1=bitRead(indirizzo,1);
> 
>     a2=bitRead(indirizzo,2);
> 
>     a3=bitRead(indirizzo,3);
> 
>     a4=bitRead(indirizzo,4);
> 
>     a5=bitRead(indirizzo,5);
> 
>     a6=bitRead(indirizzo,6);
> 
>     a7=bitRead(indirizzo,7);
> 
> 
> 
>     //...and set output
> 
>     if (a0==1) {digitalWrite(2,HIGH);}
> 
>     else {digitalWrite(2,LOW);}
> 
> 
> 
>     if (a1==1) {digitalWrite(3,HIGH);}
> 
>     else {digitalWrite(3,LOW);}
> 
> 
> 
>     if (a2==1) {digitalWrite(4,HIGH);}
> 
>     else {digitalWrite(4,LOW);}
> 
> 
> 
>     if (a3==1) {digitalWrite(5,HIGH);}
> 
>     else {digitalWrite(5,LOW);}
> 
> 
> 
>     if (a4==1) {digitalWrite(6,HIGH);}
> 
>     else {digitalWrite(6,LOW);}
> 
> 
> 
>     if (a5==1) {digitalWrite(7,HIGH);}
> 
>     else {digitalWrite(7,LOW);}
> 
> 
> 
>     if (a6==1) {digitalWrite(8,HIGH);}
> 
>     else {digitalWrite(8,LOW);}
> 
> 
> 
>     if (a7==1) {digitalWrite(9,HIGH);}
> 
>     else {digitalWrite(9,LOW);}
> 
> 
> 
>     //Wait so outputs can be set by 82S129
> 
>     delay (50);
> 
> 
> 
>     o0=digitalRead(10);//read bit from data outputs
> 
>     o1=digitalRead(11);
> 
>     o2=digitalRead(12);
> 
>     o3=digitalRead(13);
> 
> Serial.begin(9600);//Setting serial communication
> 
> //Write in binary ASCII address read and &quot;-&gt;&quot;
> 
>      if (a7==0) {Serial.print(&quot;0&quot;);}
> 
>      else {Serial.print(&quot;1&quot;);}
> 
>      if (a6==0) {Serial.print(&quot;0&quot;);}
> 
>      else {Serial.print(&quot;1&quot;);}
> 
>      if (a5==0) {Serial.print(&quot;0&quot;);}
> 
>      else {Serial.print(&quot;1&quot;);}
> 
>      if (a4==0) {Serial.print(&quot;0&quot;);}
> 
>      else {Serial.print(&quot;1&quot;);}
> 
>      if (a3==0) {Serial.print(&quot;0&quot;);}
> 
>      else {Serial.print(&quot;1&quot;);}
> 
>      if (a2==0) {Serial.print(&quot;0&quot;);}
> 
>      else {Serial.print(&quot;1&quot;);}
> 
>      if (a1==0) {Serial.print(&quot;0&quot;);}
> 
>      else {Serial.print(&quot;1&quot;);}
> 
>      if (a0==0) {Serial.print(&quot;0 -&gt; &quot;);}
> 
>      else {Serial.print(&quot;1 -&gt; &quot;);}   
> 
> 
> 
> //Write in binary ASCII output nibble
> 
> 
> 
>     if (o3==0) {Serial.print(&quot;0&quot;);}
> 
>       else {Serial.print(&quot;1&quot;);}
> 
> 
> 
>     if (o2==0) {Serial.print(&quot;0&quot;);}
> 
>       else {Serial.print(&quot;1&quot;);}
> 
> 
> 
>     if (o1==0) {Serial.print(&quot;0&quot;);}
> 
>       else {Serial.print(&quot;1&quot;);}
> 
> 
> 
>     if (o0==0) {Serial.println(&quot;0&quot;);}
> 
>       else {Serial.println(&quot;1&quot;);}
> 
> 
> 
>     if (indirizzo==255) {Serial.println(&quot;ROM has been read&quot;);}
> 
>     Serial.end();
> 
>     }
> 
> }
> 
> -----------------------------------------
> 
> END pde program
> 
> 
> 
> 
> ```
> 
>   Using Minicom or similar program, you can record serial data on your PC. 
>  Now use the editor to correct the log file so that the first line is 
>  0000000-> XXXX   and the last line is 
>  111111-> XXXX  . Please verify that the file contains only one read (256 lines).   Now we have to convert this ASCII code. Txt files in binary files. As I use Linux, I wrote a small program in Gambas programming language ( [http://gambas.sourceforge.net/](http://gambas.sourceforge.net/) ) to complete this conversion. 
>  However, Windows users can port it with Visual Basic or other languages. 
>  Simply put, it reads nibble bits, establishes nibble values (00-0F), and writes binary values in the output. Hexadecimal file. 
>  The source is as follows:  
> 
> ```
> 
> 
> Begin of Gambas program
> 
> --------------------------------------------------
> 
> PUBLIC SUB Main()
> 
> DIM ingresso AS Stream
> 
> DIM uscita AS Stream
> 
> DIM stringa AS String
> 
> DIM o0 AS String
> 
> DIM o1 AS String
> 
> DIM o2 AS String
> 
> DIM o3 AS String
> 
> DIM valore AS Byte
> 
> ingresso = OPEN &quot;/home/enzo/temp/datafile.txt&quot; FOR INPUT
> 
> uscita = OPEN &quot;/home/enzo/temp/datafile.hex&quot; FOR OUTPUT CREATE
> 
> WHILE NOT Eof(ingresso)
> 
> LINE INPUT #ingresso, stringa
> 
> o3 = Mid$(stringa, 13, 1)
> 
> o2 = Mid$(stringa, 14, 1)
> 
> o1 = Mid$(stringa, 15, 1)
> 
> o0 = Mid$(stringa, 16, 1)
> 
> valore = 1 * Val(o0) + 2 * Val(o1) + 4 * Val(o2) + 8 * Val(o3)
> 
> PRINT #uscita, Chr$(valore);
> 
> WEND
> 
> CLOSE ingresso
> 
> CLOSE uscita
> 
> END
> 
> -------------------------------------------------------------
> 
> End of Gambas program
> 
> 
> 
> 
> ```
> 
>   If you have any questions, please contact me: 
>  Vincenzo Femia 
>  enzofemia@gmail.com 
>  Reggio Calabria.  
> ```
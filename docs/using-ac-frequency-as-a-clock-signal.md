# 使用交流频率作为时钟信号

> 原文：<https://hackaday.com/2010/04/30/using-ac-frequency-as-a-clock-signal/>

前阵子[我们看到一个逻辑时钟](http://hackaday.com/2010/04/07/logic-clock-without-an-on-board-oscillator/)使用来自电网的交流频率来计时。我们询问了您使用这种方法的项目信息，我们得到了许多评论和提示。今天我们分享道格·杰克森在[他的单词钟](http://hackaday.com/2009/09/27/word-clock-tell-the-time-with-words/)中使用的方法。

上方的[示意图来自那个项目，我们用绿色标出了重要部分。[Doug]在信号到达桥式整流器之前，从 9V 交流电源中提取信号，使用 100K 电阻和齐纳二极管来保护微控制器引脚。该项目的代码以十六进制文件的形式出现，但他发给我们的是与这个计时电路相关的 C 代码。它是为 PIC 编写的，但是你可以很容易地将它应用到其他微控制器系列。休息之后看一下。](http://www.instructables.com/id/A-Word-Clock/step6/PCB-layout-Overlay-and-Schematic-files/)

```

//  Set the frequency of the local mains - MUST BE SET OR THE CLOCK WILL BE USELESS

//#define MAINS_FREQ 50      // the local mains supply frequency for Australia
#define MAINS_FREQ 60    // the local mains supply frequency for the USA

T1CON   =   0b00000011;   // Timer 1 control
//    Prescale - 00 - 1:1,   Oscilator disabled,  External Clock,  Timer Enebled

void incrementtime(void){
// increment the time counters keeping care to rollover as required
 sec=0;
 if (++min &gt;= 60) {
       min=0;
       if (++hour == 13) {
            hour=1;            }
     }
}
                                    void interrupt my_isr(void){
      // test to see if it was a Timer 1 interrupt - External mains source
      if ((TMR1IE) &amp;&amp; (TMR1IF) &amp;&amp; (mode==0)){
           sec++; // increment the seconds counter
          TMR1IF=0;
          TMR1H=0xff;
          TMR1L=MAINS_DLY;    // reset TMR1H and TMR1L to go off in the
                              // appropriate number of cycles based on the local
                              // supply frequency
          }

}

void main(void)
{
  init();  // initialise the hardware
  testleds(); // test the LED array
  version();  // Display the version number of the software

  displaytime(); // display the current time

  TMR1H=0xff;
  TMR1L=MAINS_DLY;    // reset TMR1H and TMR1L to go off in the number of
                      // mains cycles based on the local mains frequency
    ei();
  while (1) {
            //test to see if we need to increment the time counters
          if (sec==60)
          {
              incrementtime();
              displaytime();
          }

          ....... etc etc etc - do the display of the time as required.....
   }
}

```
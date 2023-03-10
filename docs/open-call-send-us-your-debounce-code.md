# 开放式呼叫:将您的去抖代码发送给我们

> 原文：<https://hackaday.com/2010/10/13/open-call-send-us-your-debounce-code/>

![](img/6621ff49e5cda3f6417b7b503fc03543.png "debounce-waveform")

如果你曾经设计过至少有一个按钮的嵌入式系统，你就必须处理按钮去抖的问题。这也被称为[触点反弹](http://en.wikipedia.org/wiki/Debounce#Contact_bounce)，这是一种如果处理不当，一次按钮按压可能会被记录为多次按钮按压的现象。解决这一问题的一种方法是利用电阻电容设置构建硬件滤波器，或者使用几个与非门。我们发现[杰克·甘斯勒]对接触反弹做了最全面和最平易近人的介绍，如果你想了解更多，你应该通读一下。

我们对去抖动按钮的软件解决方案感兴趣。这似乎是[最常见的论坛问题之一](http://www.avrfreaks.net/index.php?name=PNphpBB2&file=viewtopic&t=33821),但是很难找到可靠代码示例形式的答案。您是否有每个应用程序都依赖的去抖代码？你愿意与世界分享吗？我们希望收集尽可能多的例子，并在“一帖定天下”中发布。

## 将你的去抖代码发送到:[debounce@hackaday.com](mailto:debounce@hackaday.com)

以下是一些需要遵循的准则:

*   **请仅包含去抖代码。**去掉其他不相关的功能/等。
*   你应该发送 C 代码。如果你想发送一个汇编代码版本也可以，但是它必须是 C 代码的补充。
*   请评论你的代码。这样有助于他人理解和使用。你可能想在邮件中解释代码，但是这些信息最好放在代码注释中
*   引用你的消息来源。如果您改编了其他人的代码，请在代码注释中注明。

作为一个例子，我们在休息后加入了一组我们最喜欢的去抖代码。请注意它是如何遵循上面列出的准则的。

```
/*--------------------------------------------------------------------------
10/13/2010: Button debounce code by Mike Szczys

based on &quot;danni debounce&quot; code by Peter Dannegger:
http://www.avrfreaks.net/index.php?name=PNphpBB2&file=viewtopic&p=189356#189356

This code detects and debounces button presses. It is tailored for use with
AVR microcontrollers but I've adapted it for other architectures easily and
successfully. It can be modified to use all eight bits on the same port
for up to eight buttons.

The interrupt service routine (ISR) at the bottom uses binary counter
variables (ct0 and ct1) to check the buttons once every 10ms until 40ms has
passed. If the button registeres the first and last times it reads it as
a keypress. There is no functionality in this code for detecting a held
button.
--------------------------------------------------------------------------*/

// F_CPU used by debounce to calculate 10ms interrupts
#define F_CPU 1200000

#include &lt;avr/io.h&gt;
#include &lt;avr/interrupt.h&gt;

//define pins used by buttons
#define KEY_DDR		DDRB
#define KEY_PORT	PORTB
#define KEY_PIN		PINB
#define KEY0		1	//Button on PB1
#define KEY1		2	//Button on PB2

//Debounce variables
unsigned char debounce_cnt = 0;
volatile unsigned char key_press;
unsigned char key_state;

/*--------------------------------------------------------------------------
  Prototypes
--------------------------------------------------------------------------*/
unsigned char get_key_press( unsigned char key_mask );
void init_timers(void);
void init_io(void);

/*--------------------------------------------------------------------------
  FUNC: 10/13/10 - Used to read debounced button presses
  PARAMS: A keymask corresponding to the pin for the button you with to poll
  RETURNS: A keymask where any high bits represent a button press
--------------------------------------------------------------------------*/
unsigned char get_key_press( unsigned char key_mask )
{
  cli();			// read and clear atomic !
  key_mask &amp;= key_press;	// read key(s)
  key_press ^= key_mask;	// clear key(s)
  sei();			// enable interrupts
  return key_mask;
}

/*--------------------------------------------------------------------------
  FUNC: 10/13/10 - Sets and starts a system timer
  PARAMS: NONE
  RETURNS: NONE
--------------------------------------------------------------------------*/
void init_timers(void)
{
  cli();			// read and clear atomic !
  //Timer0 for buttons
  TCCR0B |= 1&lt;&lt;CS02 | 1&lt;&lt;CS00;	//Divide by 1024
  TIMSK0 |= 1&lt;&lt;TOIE0;		//enable timer overflow interrupt
  sei();			// enable interrupts
}

/*--------------------------------------------------------------------------
  FUNC: 10/13/10 - Initialize input and output registers
  PARAMS: NONE
  RETURNS: NONE
--------------------------------------------------------------------------*/
void init_io(void)
{
  //Setup Buttons
  KEY_DDR &amp;= ~((1&lt;&lt;KEY0) | (1&lt;&lt;KEY1));	//Set pins as input
  KEY_PORT |= (1&lt;&lt;KEY0) | (1&lt;&lt;KEY1);	//enable pull-up resistors
}

/*--------------------------------------------------------------------------
  FUNC: 10/13/10 - Main
--------------------------------------------------------------------------*/
int main(void)
{
  init_timers();	//start the timer
  init_io();		//setup the buttons

  for (;;) //loop forever
  {
    if( get_key_press( 1&lt;&lt;KEY0 ))
    {
      //KEY0 press detected. Do something here
    }

    if (get_key_press( 1&lt;&lt;KEY1 ))
    {
      //KEY1 press detected. Do something here
    }
  }
}

//--------------------------------------------------------------------------
ISR(TIM0_OVF_vect)           // interrupt every 10ms
{
  static unsigned char ct0, ct1;
  unsigned char i;

  //TCNT0 is where TIMER0 starts counting. This calculates a value based on
  //the system clock speed that will cause the timer to reach an overflow
  //after exactly 10ms
  TCNT0 = (unsigned char)(signed short)-(((F_CPU / 1024) * .01) + 0.5);   // preload for 10ms interrupts

  i = key_state ^ ~KEY_PIN;    // key changed ?
  ct0 = ~( ct0 &amp; i );          // reset or count ct0
  ct1 = ct0 ^ (ct1 &amp; i);       // reset or count ct1
  i &amp;= ct0 &amp; ct1;              // count until roll over ?
  key_state ^= i;              // then toggle debounced state
  key_press |= key_state &amp; i;  // 0-&gt;1: key press detect
}
```

[图片来源:[杰克·甘斯勒](http://www.ganssle.com/debouncing.htm)
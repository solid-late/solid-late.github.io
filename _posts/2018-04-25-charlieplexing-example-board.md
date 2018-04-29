---
layout: post
title: Example for charlieplexing using 12 LEDs
date: 2018-04-25
category: electronics
authors: aleks
---

 The next step is to check the SMD LEDs' multiplexed intensity.

Based on our experience from our previous experiment, which is explained in more detail in [this post](), we wanted to apply the principle to SMD LEDs. We hoped that the LEDs would seem much brighter with this approach.
We created a board with 3 pins and 12 LEDs. We wanted to find out if the connections crossing could be milled clean enough. Furthermore, the elements had to be soldered by hand. The aim was to find out how well this works in terms of charlieplexing, the distribution and the size of the elements.

## Circuit design
![charlieplexing circuit with 4 pins](/static/img/charlieplexing/charlieplexing_circuit_4pin.jpg)


Soldering instructions:

![charlieplexing circuit with 4 pins](/static/img/charlieplexing/solder_instr.png)


[The code can be found in the repository.](https://github.com/solid-late/circuit-main)

***

## Board production and soldering

The production worked fine.
We used 6 orange and 6 blue LEDs on the board assemblied in a row. 
Except only one connection to a LED the soldering went without any problems. The connection could be easily repared by using slighly more solder.

![boards 12 LEDs soldering](/static/img/charlieplexing/board-12LEDs.jpg)

***

## Arduino
The simple animation in the video above is based on the following program on the Arduino:

{% highlight c %}
#define NUM_LEDS 12
#define DELAY 200

#define A 2
#define B 3
#define C 4
#define D 5

const int LED_MAP[NUM_LEDS][2] = {
  /*  0 */  {D, A},
  /*  1 */  {B, D},
  /*  2 */  {A, B},
  /*  3 */  {D, C},
  /*  4 */  {B, C},
  /*  5 */  {C, B},
  /*  6 */  {A, C},
  /*  7 */  {C, D},
  /*  8 */  {C, A},
  /*  9 */  {A, D},
  /* 10 */  {D, B},
  /* 11 */  {B, A}
};

void setup() {
  pinMode(A, INPUT);
  pinMode(B, INPUT);
  pinMode(C, INPUT);
  pinMode(D, INPUT);
}

void ledOn(int index) {
  pinMode(LED_MAP[index][0], OUTPUT);
  digitalWrite(LED_MAP[index][0], HIGH);
  pinMode(LED_MAP[index][1], OUTPUT);
  digitalWrite(LED_MAP[index][1], LOW);
}

void loop() {
  for(int i = 1; i < NUM_LEDS; ++i) {
    setup();
    ledOn(i);
    delay(DELAY);
  }
  for(int i = NUM_LEDS - 2; i >= 0; --i) {
    setup();
    ledOn(i);
    delay(DELAY);
  }
}
{% endhighlight %}



![charlieplexing-example-board-in-action](/static/img/charlieplexing/board_12LEDs.gif)

[The code can be found in the repository.](https://github.com/solid-late/reindeer-code)

***

## Conclusion
Everything worked great. The next step is to create the final board containing (probably) 20 LEDs in a shape that will fit in the reindeer body and to write some more nice looking animations. A very nice thing is that we got more options which color we want to choose for the SMD LEDs.


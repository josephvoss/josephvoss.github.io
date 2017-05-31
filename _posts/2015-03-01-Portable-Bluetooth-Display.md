---

layout: post
title: Portable Bluetooth Display
group: posts
catagories: old electrical peripherial

---
{% include JB/setup %}

March 2015 to April 2015

Text-only serial display operating wirelessly over bluetooth
<!--excerpt-->

In a similar vein to the LED projector I attempted to build earlier, I wanted to 
create a portable text-only display. This time instead of creating a display from 
scratch, a small TFT display driven by an Arduino Nano was used to easily display 
the text. The data was sent to the display over a bluetooth connection from a 
Raspberry Pi. This Raspberry Pi was configured to connect to a bluetooth keyboard on 
start up, and run a small script which captured all input and piped it into a serial 
console hosted on a second bluetooth connection. This second connection was attached 
to the Arduino, and sent all output to the microcontroller which displayed it on the 
TFT screen. The initial proof of concept worked as shown in the image, but several 
issues prevented this from becoming a usable device. The screen used was too small to 
do any productive work, and most of the screen control characters like "clear" didn't 
work out of the box, meaning that the Arduino display library used would have to be 
rewritten. Additionally, the bluetooth connection was maxed at 57600 bits/s, 
meaning that even if the screen control commands worked it would take a while to do 
anything productive. This would be a nonstarter for even editing text using an editor 
like vim which clears the screen constantly. Since I attempted this project I've 
realized that these issues could be solved by using a FGPA to drive a larger LCD 
display much faster than a microcontroller could, and a 2.4 GHz transmitter could 
increase the transfer rate to 2 Mb/s. In the Summer of 2016 I attempted to program a 
FPGA to handle this serial communication and LCD driving, but was unable to see it to 
fruition.

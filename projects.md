---
layout: page
title : Projects
header : Personal Projects
group: navigation
---
{% include JB/setup %}

## Student Cluster Competition

#### February 2016 to November 2016

During my parallel programming class I heard of an opportunity for students to build a 
configure a high performance computing cluster. I applied to join the team and 
(surprisingly) got in. Over the next few months we practiced running applications on 
Texas Advanced Computing Center (TACC)'s systems, designed the hardware configuration 
of our cluster, and learned about Linux system management and control. My main tasks 
were running and tuning High Performance Linpack, writing scripts to automatically 
build, run, and generate matplotlib graphs analyzing the performance of several 
applications, and creating a power monitor system using SNMP communication, stored in 
a graphite database and visualized with grafana. In the Fall our hardware came in, and 
we assembled and configured our cluster of 12 nodes by using Open HPC to bootstrap a 
few representative nodes, then cloned out their images to the rest of the cluster. On 
November 11th, we will fly out to Salt Lake City for the Super Computing Conference 
to test our cluster against other students' machines from around the globe.

[Link to the SCC Competition's website](http://www.studentclustercompetition.us/).

## Automated Two Factor

#### September 2016

In the Fall of 2016, Texas Advanced Computing Center (TACC) began to require users to 
use two factor authentication to access their systems. Realistically for me, I usually 
opened several terminals on their clusters multiple times a day, and with ssh-keys 
set up this was never a problem. However, now having to use input a two factor code from 
my phone for every terminal got really annoying really quickly. Using [Twilio] (https://www.twilio.com/) 
I configured the two-factor codes to be send to a Flask web server I set up on 
a Raspberry Pi, encrypted and stored. Whenever I needed to login to TACC systems, a 
script on my local machine would send a login request, wait for the access code to be 
received and encrypted on the server, retrieve it, decrypt it, and send it to TACC.

The server and the login script are both on github [here](https://github.com/josephvoss/AutomatedTwoFactor). 

## Fluid Flow Simulation

#### April 2016 to May 2016

For the final project in my Parallel Programming class we were tasked with solving 
some problem using MPI on the HPC systems at Texas Advanced Computing Center (TACC). 
I was taking Fluid Mechanics at the same time, and chose to replicated one of the labs 
we had completed about the development of laminar flow. With the MPI C++ bindings I 
wrote a basic simulation which depicted the flow of fluid through a two dimensional 
channel in the terms of the pressure and velocity of the fluid elements in a mesh. 
This data was then exported to python to generate a matplotlib animation which shows 
how successive iterations changed the result of the simulation.

[Link to report](assets/img/FluidFlowWriteup.pdf).

[Link to github repo](https://github.com/josephvoss/FluidFlow).

## Vindicator CPU

#### August 2015 to December 2015

During my Mechanical Engineering Computational Methods class the professor explained 
the basic operation of a processor, which re-ignited my interest in the function of 
low level logic gate operations. Initially I used logic-gate modeling software to 
try and design basic components like an Arithmetic Logic Unit, but after making some 
progress I moved to designing these components in Verilog so it could be ported to 
actual hardware on an FPGA board. After designing a basic adder and instruction set, 
and defining a simple assembly language to use to perform basic operations, I started 
bread-boarding the FPGA with small static RAM chips to serve as external memory. While 
I was able to manually set the bits in the RAM, there was an error with the Verilog 
memory handler I wrote which prevented writing any data out to memory. After several 
weeks at a standstill I resolved to wait to finish this project until I had more 
experience working with FPGAs

[Link to github repo](https://github.com/josephvoss/the-vindicator-cpu)

## Portable Bluetooth Display

#### March 2015 to April 2015

In a similar vein to the LED projector I attempted to build earlier, I wanted to 
create a portable text-only display. This time instead of creating a display from 
scratch, a small TFT display driven by an Arduino Nano was used to easily display 
the text. The data was sent to the display over a bluetooth connection from a 
Raspberry Pi. This Raspberry Pi was configured to connect to a bluetooth keyboard on 
start up, and run a small script which captured all input and piped it into a serial 
console hosted on a second bluetooth connection. This second connection was attached 
to the Arduino, and send all output to the microcontroller which displayed it on the 
TFT screen. The initial proof of concept worked as shown in the image, but several 
issues prevented this from becoming a usable device. The screen used was to small to 
do any productive work, and most of the screen control characters like clear didn't 
work out of the box, meaning that Arduino display library used would have to be 
rewritten. Additionally, the bluetooth connection was maxed at 57600 bits/s, 
meaning that even if the screen control commands worked it would take a while to do 
anything productive. This would be a nonstarter for even editing text using an editor 
like vim which clears the screen constantly. Since I attempted this project I've 
realized that these issues could be solved by using a FGPA to drive a larger LCD 
display much faster than a microcontroller could, and a 2.4 GHz transmitter could 
increase the transfer rate to 2 Mb/s. In the Summer of 2016 I attempted to program a 
FPGA to handle this serial communication and LCD driving, but was unable to see it to 
fruition.

## Single LED Rotating Disk Projector

#### October 2014 to December 2014

After initially getting experience with the Linux command line, I realized how much 
work could be done with a simple text-user-interface. Simultaneously, I wanted to have 
an ultra-portable PC, and realized that computing hardware was able to be minimized 
easily. The largest components of portable systems were the interfaces: the display 
and keyboard. Several portable keyboard options exist, but there's no inexpensive 
portable display. I thought that by reducing the resolution of the display to the 
absolute minimum to produce readable text, a portable text-user-interface could be 
added to a small computer like a Raspberry Pi. As a proof of concept I laser-cut a 
disk with several small holes, which when rotated would create an 8x5 persistence of 
vision display. Using an ATTINY microcontroller and a hall effect sensor, a single LED 
was programmed to blink in series with the rotation of the disk, which would 
selectively turn a single pixel on or off. This proof of concept ultimately failed to 
do the low clock speed of the microcontroller and the instability of the brushed DC 
motor. A distinct varying pattern could be seen during the test runs, but a steady 
image was never formed. I intend to re-attempt this project with a brushless motor to 
enable more speed control, but I would like to have more electronics experience 
through my coursework before I pick it back up again.

## Vandium Dioxide Logic Gates

#### June 2013 to April 2014

In high school I became fascinated with the operation of logic gates, and wanted to 
build a basic adder circuit, but in a new and innovative way. From my chemistry 
experience, I had learned about the metamaterial Vanadium Dioxide and it's 
thermo-chromatic triggering properties. By following the manufacturing procedure 
outlined in [Deki, Aoi, & Kajinami's paper](https://dx.doi.org/10.1023/A:1018603402586), I designed a set of optical logic gates using the Vanadium Dioxide thin films that 
would produce binary levels of infrared light. This infrared light needed to be 
powerful enough to heat these Vi-O<sub>2</sub> thin films, so I set about constructing 
a flowing-air Carbon Dioxide laser. I was able to obtain several initial lases with 
this resonator, but eventually retired this project due to the difficulty of keeping a 
low vacuum, dangers of working with high voltage, and shear impracticability of it.


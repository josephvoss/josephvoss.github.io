---

layout: post
title: Rotating Disk Projector
group: posts
categories: old electrical peripheral
description: |
  October to December 2014:
  Prototype of compact and inexpensive display using a rotating disk and a single LED

---
{% include JB/setup %}


After initially getting experience with the Linux command line through my 
experience working at Applied Research Laboratories over the Summer of 2014, I realized how much 
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

---

layout: post
title: Vindicator CPU 
group: posts
categories: old electrical FPGA
description: |
 August to December 2015: Attempt to write an 8 bit core from scratch in Verilog

---
{% include JB/setup %}

During my Mechanical Engineering Computational Methods class, the professor explained 
the basic operation of a processor. This  re-ignited my interest in the function of 
low level logic gate operations. Initially I used logic-gate modeling software to 
try and design basic components like an Arithmetic Logic Unit, but after making some 
progress I moved to designing these components in Verilog so it could be ported to 
actual hardware on an FPGA board. After designing a basic adder and instruction set, 
and defining a simple assembly language to use to perform basic operations, I started 
bread-boarding the FPGA with small static RAM chips to serve as external memory. While 
I was able to manually set the bits in the RAM, there was an error with the Verilog 
memory handler I wrote which prevented writing any data out to memory. After several 
weeks at a standstill I resolved to wait to finish this project until I had more 
experience working with FPGAs.

[Link to github repo](https://github.com/josephvoss/the-vindicator-cpu).

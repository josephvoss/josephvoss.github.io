---
layout: page
title : Projects
header : Personal Projects
group: navigation
---
{% include JB/setup %}

## SCC

#### February 2016 to November 2016



## Two Factor is Annoying

#### September 2016

In the Fall of 2016, Texas Advanced Computing Center (TACC) began to require users to 
use two factor authentication to access their systems. Realistically for me, I usually 
opened several terminals on their clusters multiple times a day, and with ssh-keys set up this was never a problem. However, now having to use input a two factor code from 
my phone for every terminal got really annoying really quickly. Using Twilio 
[link] I configured the two-factor codes to be send to a Flask web server I set up on 
a Raspberry Pi, encrypted and stored. Whenever I needed to login to TACC systems, a 
script on my local machine would send a login request, wait for the access code to be 
received and encrypted on the server, retreive it, decrypt it, and send it to TACC.

The server and the login script are both on github [here]. 

## Fluid Flow Simulation

#### April 2016 to May 2016

## Vindicator CPU

#### August 2015 to December 2015

## Portable Bluetooth Display

#### March 2015 to April 2015

## Single LED Rotating Disk Projector

#### October 2014 to December 2014

## DIY Carbon Dioxide Laser/Vandium Dioxide Logic Gates

#### June 2012 to April 2014


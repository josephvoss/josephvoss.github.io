---
layout: page
title : Projects
header : Personal Projects
group: navigation
---
{% include JB/setup %}

## Student Cluster Competition

#### February 2016 to November 2016

During my parallel programming class I heard of an opprotunity for students to build a 
configure a high performance computing cluster. I applied to join the team and 
(surprisingly) got in. Over the next few months we practiced running applications on 
TACC's systems, designed the hardware configuration of our cluster, and learned about 
Linux system management and control. My main tasks were running and tuning High 
Performance Linpack, writing scripts to automatically build, run, and generate 
matplotlib graphs analysing the performance of several applications, and creating a 
power monitor system using SNMP communication, stored in a graphite database and 
visualized with grafana. In the Fall our hardware came in, and we assembled and 
configured our cluster of 12 nodes by using Open HPC to bootstrap a few representative 
nodes, then cloned out their images to the rest of the cluster. On Novemeber 11th, we 
will fly out to Salt Lake City for the Super Computing Conference to test our cluster 
against other students' machines from around the globe.

Link to the SCC Competition's website.

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

For the final project in my Parallel Programming class we were tasked with solving 
some problem using MPI on the HPC systems at TACC. I was taking Fluid Mechanics at the
same time, and chose to replicated one of the labs we had completed about the 
development of laminar flow. With the MPI C++ bindings I wrote a basic simulation 
which depicted the flow of fluid through a 2 Dimensional pipe in the terms of the 
pressure and velocity of the fluid elements in a mesh. This data was then exported to 
python to generate a matplotlib animation which shows how successive iterations 
changed the result of the simulation.

Link to Report.
Link to github repo.

## Vindicator CPU

#### August 2015 to December 2015

## Portable Bluetooth Display

#### March 2015 to April 2015

## Single LED Rotating Disk Projector

#### October 2014 to December 2014

## DIY Carbon Dioxide Laser/Vandium Dioxide Logic Gates

#### June 2012 to April 2014


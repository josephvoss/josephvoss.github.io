---

layout: post
title: Student Cluster Competition
group: posts
catagories: old high-performance-computing

---
{% include JB/setup %}

February 2016 to November 2016

International competition where students design, built, and test a
high-performance cluster at the SC16 conference at Salt Lake City.  
<!--excerpt-->

During my parallel programming class I heard of an opportunity for students to build 
and configure a high performance computing cluster. I applied to join the six-person 
team and (surprisingly) was accepted. Over the next few months we practiced 
running applications on 
Texas Advanced Computing Center (TACC)'s systems, designed the hardware configuration 
of our cluster, and learned about Linux system management and control. My main tasks 
were running and tuning High Performance Linpack, writing scripts to automatically 
build, run, and generate matplotlib graphs that analyzed the performance of several 
applications. I also created a power monitor system using SNMP communication, which 
stores data in a graphite database and visualized with grafana. In the Fall our 
hardware came in, and 
we assembled and configured our cluster of 12 nodes by using Open HPC to bootstrap a 
few representative nodes, then cloned out their images to the rest of the cluster. On 
November 11th, we will fly out to Salt Lake City for the Super Computing Conference 
to test our cluster against other students' machines from around the globe.

[Link to the SCC Competition's website](http://www.studentclustercompetition.us/2016/index.html).

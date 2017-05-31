---

layout: post
title: Student Cluster Competition
group: posts
categories: old high-performance-computing
description: |
 February 2016 to November 2016:
 International competition where students design, built, and test a
 high-performance cluster at the SC16 conference at Salt Lake City

---
{% include JB/setup %}

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
few representative nodes, then cloned out their images to the rest of the
cluster. On November 11th we flew out to Salt Lake City to the SC16 Conference
where we competed against teams from across the world for 48-hours straight. My
primary task during this time was learning to build and use the molecular
dynamics application GROMACS, which was the 'mystery application', so we didn't
know about it until the start of the application. We placed 4th out of 14 teams
overall, which given that our team was made up entirelly of new competitors I
was very pleased with.


[Link to the SCC Competition's website](http://www.studentclustercompetition.us/2016/index.html).

---

layout: post
title: Fluid Flow Simulation
group: posts
categories: old high-performance-computing academic pure-software
description: |
 April to May 2016: Navier-Stokes solver in C++ using MPI on TACC systems

---
{% include JB/setup %}

For the final project in my Parallel Programming class we were tasked with solving 
some problem using MPI on the HPC systems at Texas Advanced Computing Center (TACC). 
I was taking Fluid Mechanics at the same time, and chose to replicate one of the labs 
we had completed about the development of laminar flow. With the MPI C++ bindings, I 
wrote a basic simulation which depicted the flow of fluid through a two dimensional 
channel in the terms of pressure and velocity of the fluid elements in a mesh. 
This data was then exported to python to generate a matplotlib animation which shows 
how successive iterations changed the result of the simulation.

[Link to report](/assets/img/FluidFlowWriteup.pdf).

[Link to github repo](https://github.com/josephvoss/FluidFlow).

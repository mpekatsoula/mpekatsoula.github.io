---
layout: post
title:  "Runtime support for approximate computing in heterogeneous systems"
date:   2017-01-27
excerpt: "MSc thesis"
tag:
- projects
comments: true
---
Recently I finished my MSc Thesis, titled “Runtime support for approximate computing in heterogeneous systems”. I developed a run-time system in C programming language that supports approximate  computations using OpenCL. You can download my thesis <a href="{{site.url}}assets/files/msc_thesis.pdf">here</a>.

Source code will be available in a few weeks.

### Abstract

Energy efficiency is the most important aspect in nowadays systems, ranging from embedded devices to high performance computers. However, the end of Dennard scaling limits expectations for energy efficiency improvements in future devices, despite manufacturing processors in lower geometries and lowering supply voltage. Many recent systems use a wide range of power managing techniques, such as DFS and DVFS, in order to balance the demanding needs for higher performance/throughput with the impact of aggressive power consumption and negative thermal effects. However these techniques have their limitations when it comes to CPU intensive workloads.

Heterogeneous systems appeared as a promising alternative to multicores and multiprocessors. They offer unprecedented performance
and energy efficiency for certain classes of workloads, however at significantly increased development effort: programmers have to spend significant effort reasoning on code mapping and optimization, synchronization, and data transfers among different devices and address
spaces. One contributing factor to the energy footprint of current software is that all parts of the program are considered equally important for the quality of the final result, thus all are executed at full accuracy. Some application domains, such as big-data, video and image processing etc., are amenable to approximations, meaning that some portions of the application can be executed with less accuracy, without having a big impact on the output result.

In this MSc thesis we designed and implemented a runtime system, which serves as the back-end for the compilation and profiling infrastructure of a task-based meta-programming model on top of OpenCL. We give the opportunity to the programmer to provide approximate functions that require less energy and also give her the freedom to express the relative  importance of different computations for the quality of the output, thus facilitating the dynamic exploration of energy / quality trade-offs in a disciplined way. Also we simplify the development of parallel algorithms on heterogeneous systems, relieving the programmer from tasks such as work scheduling and data manipulation across address spaces. We evaluate our approach using a number of real-world applications, from domains such as finance, computer vision, iterative equation solvers and computer simulation.

Our results indicate that significant energy savings can be achieved by combining the execution on heterogeneous systems with approximations, with graceful degradation of output quality. Also, hiding the underlying memory hierarchy from the programmer, performing data dependency analysis and scheduling work transparently, results in faster development without sacrificing the performance of the applications.
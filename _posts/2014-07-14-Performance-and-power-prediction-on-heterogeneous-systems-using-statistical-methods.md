---
layout: post
title:  "Performance and power prediction on heterogeneous systems using statistical methods"
date:   2014-07-14
excerpt: "BSc thesis"
tag:
- projects
comments: true
---

<a href="{{site.url}}/assets/files/bsc_thesis.pdf">Here</a> you can download my BSc thesis.

### Abstract
{: style="text-align: center"}
 
Heterogeneous systems provide high computing performance, combining low cost
and low power consumption. These systems include various computational resources
with different architectures, such as CPUs, GPUs, DSPs or FPGAs. It is crucial
to have full knowledge of these architectures, but also of the programming models
used in order to increase the performance on a heterogeneous system.

One way to achieve this goal, is the prediction of the execution time on the different
computational resources, using statistical values which we collect with the use of
hardware counters. The purpose of this thesis is to increase the performance of a
heterogeneous system using the data we collected by training a statistical model
which will predict the execution time. Further goal is to use this prediction model
inside a run-time scheduler which will migrate the running application in order to
decrease the execution time and increase the overall performance.

We used various statistical models, such as linear regression, neural networks and
random forests and we predicted the execution time to Intel CPUs and NVIDIA
GPUs, with different levels of success.
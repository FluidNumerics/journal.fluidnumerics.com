# Profiling PyTorch applications on AMD GPU systems

When running complex AI/ML applications, built on Pytorch, you may be wondering how you might go about improving performance. Answering this question can be done in many ways. We suggest a workflow that involves determining where there are bottlenecks, why there are bottlenecks, and what the potential performance their might be left on the table. Answering these questions can be done through three types of profiling

1. Hotspot profiling - Determines what kernels your code spends the most time on
2. Trace profiling - Provides the timeline of execution and can relate kernels that are interdependent
3. Events profiling - Determines the kinds of activities on the hardware that your kernels are actually doing.

This article focuses on what tools you have available for various types of profiling for Pytorch applications on AMD GPU hardware.


## `torchprofiler`
* What kind of profiles can you create with `torchprofiler`


## `rocprof`
* How to do hotspot, trace, and events profiling
* Lead into why AMD leans on `rocmprof-compute` and `rocprof-systems` now; formerly AMD research tools ( `--sys-trace` only does GPU kernel profiling. events profiling with rocprof directly is time consuming to get any meaningful data from.)


## `rocprof-compute` (formerly `omniperf`)
### Installation & Usage tips for conda environments
* Describe what happens when you follow AMD's instructions directly when using conda environments
* Describe how to install within a conda environment
* Using the `#!/usr/bin/env python` sh'bang

## `rocprof-system` (formerly `omnitrace`)
### Installation & Usage tips for conda environments



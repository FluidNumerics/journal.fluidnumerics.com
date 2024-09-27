# The F Word : Multi-GPU computing with MPI and ROCm

## Video Outline

* Introduce SELF project
  * Describe approach for using spectral element methods to solve conservation laws (weak form, separating interior element operations and element edge operations)
  * Discuss strategies for parallelism (briefly)
    * do concurrent (multithreading, shared memory, single process)
    * GPU acceleration
    * Distributed memory parallelism (introduce domain decomposition.. lead to next point)
* Describe domain decomposition - 
  * Split physical domain into multiple subdomains
  * Assign a single process to each subdomain
  * Motivate the need for sharing solution on element edges/faces between neighboring process
  * Explain how MPI is used to implement distributed memory parallelism (and explain why we call it distributed memory parallelism)
* Discuss GPU-Aware MPI
  * When working on GPUs, there are "host" and "device" copies of data
  * For simplicity, we'll assume that each MPI rank "owns" a single distinct GPU
  * For performance reasons, we want to send messages directly between GPUs, and avoid going through a host buffer
  * This requires
    * Hardware that is capable of doing this (AMD Instinct GPUs are capable of handling this)
    * MPI implementation and communication framework that supports device pointers - for this, we'll look at OpenMPI with libfabric and ucx
* Compare and contrast libfabric and ucx
  * libfabric uses host buffers
  * ?? how does ucx route messages with device pointers ??
  * Introduce how we will compare performance
    * rocm-bandwidth-test (provide baseline of expected peak one-way bandwidth)
    * OSU pt2pt bandwidth test - compare openmpi+libfabric and openmpi+ucx
* How to install ...
  * libfabric with ROCm aware support
  * ucx with ROCm aware support
  * OpenMPI 
    * with rocm and libfabric
    * with rocm and ucx
  * OSU
    * What we found missing in AMD's documentation (C-flags need `hipconfig -C`)
* Running osu benchmarks
  * with libfabric
  * with ucx
* Performance results
* Summary and what comes next
  * How we implement CPU and GPU "backends" using OO Fortran classes and inheritance
  * Explanations of the software design for SELF, including how MPI exchange is implemented through "SideExchange" methods
  * Stay tuned, subscribe, and hit like!
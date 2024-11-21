# Maximizing Performance, Minimizing Costs: Energy Savings from GPU Optimization

In today's world of high-performance computing, every millisecond and every watt counts. That’s why software porting and optimization aren’t just about achieving faster runtimes—they’re about reducing operational costs and improving sustainability. At Fluid Numerics, we specialize in delivering measurable improvements by porting and optimizing applications for modern hardware like AMD GPUs.

## The Problem: Inefficient GPU Utilization
A recent project highlights just how impactful optimization can be. Pawsey Supercomputing Centre engaged Fluid Numerics' mentored sprint service to support the porting an optimization of [PaCER projects](https://pawsey.org.au/pacer/) from V100 to MI250X GPUs. One of the ten applications we supported, a quantum chromodynamics application (EmPRISM) was initially designed for Nvidia V100 GPUs. 

The most expensive kernel, a matrix free elliptic equation inversion with preconditioned conjugate gradient, was achieving approximately **85% of peak memory bandwidth** V100s. However, when first ported to AMD MI100 and MI250X GPUs, the application struggled, achieving just **36.8% of peak bandwidth** and leaving a significant amount of performance on the table. This inefficiency led to longer runtimes, higher energy consumption, and substantial over-consumption of the awarded allocation on [Pawsey's Setonix](https://pawsey.org.au/systems/setonix/)

## The Solution: Strategic Optimizations
Through targeted optimization efforts, including:
- Replacing shared memory usage with vector registers,
- Reordering operations to reduce L2 cache misses,
- Fine-tuning kernel configurations (e.g., launch bounds),
- Implementing subdomain memory layouts,

We achieved dramatic improvements. On AMD MI100 GPUs, performance increased by **1.91x**, bringing memory bandwidth utilization to **85.5% of its peak**. 

## The Hidden Win: Energy Savings
Performance improvements often lead to significant energy cost savings, particularly in GPU-heavy workloads. Consider the following:

- **Baseline Energy Consumption**: We found that each iteration of the preconditioned conjugate gradient on MI100 GPUs was 2.71 milliseconds per iteration. With each GPU consuming around **300 watts** (estimate), that’s **0.813 watt-seconds per iteration**.
- **Optimized Energy Consumption**: After optimizations, the runtime dropped to 1.72 milliseconds per iteration, reducing energy consumption to **0.516 watt-seconds per iteration**.
- **Total Savings**: This represents a **36.5% reduction in energy consumption per iteration**. Over millions of iterations—common in HPC workloads—these savings add up to significant reductions in electricity costs and carbon emissions. 


## Why It Matters for Your Business
If your organization runs GPU-intensive workloads, these kinds of savings can scale dramatically across clusters or cloud environments. By optimizing applications to run efficiently on the latest GPU architectures, you not only gain faster results but also reduce your operational costs and environmental footprint.

## Let’s Optimize Together
Our team at Fluid Numerics specializes in software porting and optimization services for HPC and AI workloads. Whether you're transitioning to AMD GPUs or looking to maximize performance on your existing hardware, we can help you achieve faster runtimes and lower energy costs.

Reach out to us to learn how our solutions can optimize your workloads, cut costs, and help your organization stay ahead in an increasingly competitive landscape.

* [Learn about mentored sprints](../what-is-a-mentored-sprint/README.md)
* [Read the full mentored sprint report here](../emprism-mentored-sprint-report/README.md)
* [Contact us for a consultation](https://www.fluidnumerics.com/contact)
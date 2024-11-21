### Accelerating Science with Software Optimization: Lessons from the EXESS Mentored Sprint

**What if your application could run faster, more efficiently, and on cutting-edge hardware—all while saving you time and money?** That’s exactly what we achieved for the developers of the EXtreme-scale Electronic Structure System (EXESS) during a recent mentored sprint. By working together, we optimized performance, tackled inefficiencies, and unlocked new possibilities for quantum chemistry simulations.

Here’s how our software porting and optimization services can deliver the same transformative results for your projects.

---

#### The Challenge: Porting and Optimizing for New GPU Architectures
EXESS, a state-of-the-art quantum chemistry application, needed to transition from Nvidia’s CUDA to a hardware-agnostic HIP framework to support both Nvidia and AMD GPUs. The goal wasn’t just compatibility—it was achieving comparable or better performance on AMD GPUs like the MI100 and MI250x. 

At the same time, the team faced inefficiencies in the application’s CPU and GPU workflows, particularly in memory access and kernel performance. They needed expert guidance to resolve these issues while building their skills with new tools and platforms.

---

#### The Solution: Our Mentored Sprint
Through our **Mentored Sprint service**, we guided the EXESS team through a 5-day focused effort, supported by three weeks of preparation and post-sprint analysis. This tailored approach allowed us to achieve the following:

1. **Ported to HIP for Multi-GPU Compatibility**  
   The EXESS team successfully transitioned their application from CUDA to HIP, enabling seamless performance on both Nvidia and AMD GPUs. The port ensured EXESS is now hardware-agnostic, a key step for long-term sustainability and flexibility.

2. **Boosted GPU Performance**  
   We optimized critical kernels, helping AMD MI100 GPUs match the performance of Nvidia V100 GPUs for key benchmarks. Additionally, the MI250x outperformed the MI100 by **2.6x**, demonstrating the power of AMD’s latest architecture.

3. **Identified Major Efficiency Gains**  
   By switching from ROCSolver to MAGMA for eigenvalue decomposition, we reduced runtime for critical benchmarks by over **390x**. This change dramatically improved the efficiency of the workflow and set a clear path for future optimizations.

4. **Enabled Comprehensive Profiling Across Platforms**  
   Using tools like `rocprof`, `Perfetto`, and `ARM Forge`, the team developed a deeper understanding of where time and resources were spent in their application. This led to actionable insights, including:
   - Reducing memory transfer overhead by overlapping operations with GPU streams.
   - Improving kernel memory access patterns to boost DRAM bandwidth utilization.

5. **Equipped the Team for Future Success**  
   Beyond code improvements, the sprint provided valuable hands-on training. The EXESS developers gained expertise in GPU profiling, debugging, and optimization on both Nvidia and AMD platforms, setting them up for long-term success.

---

#### The Results: Faster, Smarter, and More Efficient Science
The optimizations achieved during this sprint didn’t just improve runtime—they paved the way for significant cost savings. By improving GPU efficiency and reducing runtime overhead, the EXESS team can now run more simulations in less time, saving energy and accelerating scientific discovery.

For organizations running large-scale simulations or high-performance applications, the benefits are clear:
- **Performance Gains:** Reduced runtimes and optimized hardware utilization.
- **Cost Savings:** Lower energy usage translates to reduced operational costs.
- **Sustainability:** Efficient computing aligns with green initiatives and reduces carbon footprints.

---

#### Why Choose a Mentored Sprint?
Our Mentored Sprint service is designed to deliver results in just five days. With expert guidance, hands-on training, and proven methodologies, we help your team:
- Transition applications to new hardware platforms seamlessly.
- Identify and resolve performance bottlenecks.
- Build the skills needed to optimize and future-proof your software.

Whether you’re porting to new GPUs, optimizing for cloud environments, or improving the scalability of your application, we’re here to help.

---
### Let Your Software Reach New Heights

The results speak for themselves: [**the EXESS team’s work during and after our Mentored Sprint propelled them to become a 2024 Gordon Bell Prize finalist**](https://arxiv.org/html/2410.21888v1), one of the most prestigious honors in high-performance computing. Their success underscores the transformative potential of expert-led software porting and optimization.

Ready to take your application to the next level? Let’s work together to optimize your software, accelerate your performance, and help you achieve your boldest ambitions. Contact us today to start your journey toward breakthrough results!

#### Let’s Accelerate Your Success
If you’re ready to make your software faster, more efficient, and ready for the future, our Mentored Sprint service is the perfect starting point. Let’s work together to unlock the full potential of your applications and achieve groundbreaking results.

* [Learn about mentored sprints](../what-is-a-mentored-sprint/README.md)
* [Read the full mentored sprint report here](../exess-mentored-sprint-report/README.md)
* [**Contact us for a consultation**](https://www.fluidnumerics.com/contact)
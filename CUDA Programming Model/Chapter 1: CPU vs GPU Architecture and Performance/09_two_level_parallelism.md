## 8. Two-Level Parallelism in GPUs

CPUs typically have a single level of parallelism with thread IDs. In contrast, GPUs have **two levels of parallelism**:

1. A grid of thread blocks, where each block is assigned to an SM.
2. Inside each thread block, there are warps of 32 threads, executing in parallel.

[Previous: GPU Programming vs OpenMP](08_gpu_vs_openmp.md) | [Next: Synchronization in GPU Threads](10_synchronization.md)

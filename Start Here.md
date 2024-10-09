# Introduction to Parallel Programming for GPUs with CUDA
The goals for this CUDA tutorial are to ensure that participants gain a comprehensive understanding of the CUDA programming model, including SIMT threading, kernel structure, and GPU memory hierarchy, as well as practical knowledge of memory optimization techniques like global memory coalescing and shared memory bank conflicts.

## Topics
### CUDA Programming Model
1. **[Chapter 1: CPU vs GPU Architecture and Performance](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/01_introduction.md)**
   - [1. Introduction](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/01_introduction.md)
   - [2. CPU vs GPU Architecture](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/02_cpu_vs_gpu_architecture.md)
   - [3. CPU Structure vs GPU Structure](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/03_cpu_vs_gpu_structure.md)
   - [4. Streaming Multiprocessors (SMs) in GPUs](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/04_smp_in_gpus.md)
   - [5. SIMT vs SIMD](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/05_simt_vs_simd.md)
   - [6. Data Parallelism in GPUs](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/06_data_parallelism.md)
   - [7. Thread Partitioning](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/07_thread_partitioning.md)
   - [8. Two-Level Parallelism in GPUs](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/08_two_level_parallelism.md)
   - [9. Synchronization in GPU Threads](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/09_synchronization.md)
   - [10. Occupancy vs Register Usage](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/10_occupancy.md)

2. **[Chapter 2: CUDA Programming In Practice]()**
   1. Basic GPU Kernel Code Example
   2. SIMT Threading
   3. Kernel Structure
### GPU memory hierarchy
1. memory optimization techniques, 
   - global memory coalescing, 
   - shared memory bank conflicts, 
2. and a brief discussion on Warp Occupancy. 





---
By Omid Asudeh
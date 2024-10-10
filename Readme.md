# Introduction to Parallel Programming for GPUs with CUDA
The goals for this CUDA tutorial are to gain a comprehensive understanding of the CUDA programming model, including SIMT threading, kernel structure, and GPU memory hierarchy, as well as practical knowledge of memory optimization techniques like global memory coalescing and shared memory bank conflicts.

## Topics
### CUDA Programming Model
1. **[Chapter 1: CPU vs GPU Architecture and Performance](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/1.introduction.md)**
   - [1. Introduction](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/1.introduction.md)
   - [2. Efficiency of GPUs over CPUs](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/2.efficiency.md)
   - [3. Structural Differences: CPU vs GPU](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/3.structural_differences.md)
   - [4. Streaming Multiprocessors (SMs) in GPUs](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/4.streaming_multiprocessors.md)
   - [5. Thread Hierarchy Organization in GPUs](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/5.GPU_Thread_Hierarchy.md)

   - [6. Two-Level Parallelism in GPUs](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/6.two_level_parallelism.md)
   - [7. Synchronization in GPU Threads](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/7.synchronization.md)
   - [8. Work Division: CPUs vs GPUs](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/8.work_division.md)
   - [9. SIMT vs SIMD](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/9.simt_vs_simd.md)
   - [10. Limitations of GPUs](/CUDA%20Programming%20Model/Chapter%201:%20CPU%20vs%20GPU%20Architecture%20and%20Performance/10.limitations_of_gpus.md)

2. **[Chapter 2: CUDA Programming In Practice](/CUDA%20Programming%20Model/Chapter%202:%20CUDA%20Programming%20In%20Practice/1.introduction.md)**
   - [1. Introduction](/CUDA%20Programming%20Model/Chapter%202:%20CUDA%20Programming%20In%20Practice/1.introduction.md)
   - [2. Host-Device Heterogeneous Programming Model](/CUDA%20Programming%20Model/Chapter%202:%20CUDA%20Programming%20In%20Practice/2.Host-Device-Model.md)
   - [3. Increment Array Example](/CUDA%20Programming%20Model/Chapter%202:%20CUDA%20Programming%20In%20Practice/3.incrementArrayExp.md)
   - [4. Necessary Steps for Host-Device Heterogeneous Code](/CUDA%20Programming%20Model/Chapter%202:%20CUDA%20Programming%20In%20Practice/4.steps_Host_Device_Code.md)
   - [5. CUDA Syntax](/CUDA%20Programming%20Model/Chapter%202:%20CUDA%20Programming%20In%20Practice/5.cuda_syntax.md)

### GPU memory hierarchy
1. memory optimization techniques, 
   - global memory coalescing, 
   - shared memory bank conflicts, 
2. and a brief discussion on Warp Occupancy. 



# References:
- [Nvidia Cuda Programming Guide](https://docs.nvidia.com/cuda/cuda-c-programming-guide)
- CS 4230/6230 (Parallel and High-Performance Computing) Lectures by Professor P. Sadayappan, The University of Utah

---
By Omid Asudeh
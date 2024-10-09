# Chapter 1: CPU vs GPU Architecture and Performance

## 1. Efficiency of GPUs over CPUs

CPUs and GPUs both use the same transistor technology. However, GPUs are an order of magnitude more efficient in terms of energy per instruction. This efficiency allows GPUs to run significantly more instructions, even with basic air cooling (around 300W dissipation rate). As a result, GPUs have an order of magnitude higher peak performance compared to CPUs.

## 2. Structural Differences: CPU vs GPU

The structure of CPUs and GPUs varies greatly:

- **CPU**: CPUs have few Arithmetic Logic Units (ALUs), with most of their transistors dedicated to caching (almost half the space). They also have sophisticated control units capable of complex operations such as scoreboarding (reordering instructions based on when their operands are available) and branch prediction.
  
- **GPU**: GPUs, in contrast, have many simple in-order cores (ALUs) and basic control units. This allows GPUs to prioritize parallel execution over complex control logic.

## 3. Streaming Multiprocessors (SMs) in GPUs

GPUs typically have fewer than 100 Streaming Multiprocessors (SMs), each with its own scheduler. Each thread block is assigned to only one SM, but an SM may have multiple thread blocks assigned to it. 

Each SM has many registers and a small control unit, scheduling a single instruction for an array of 32 cores (known as SIMT - Single Instruction, Multiple Threads). Each SM also has shared memory (shared among the cores) and private registers dedicated to each core.

## 4. SIMT vs SIMD: A Key Difference

- **SIMD (Single Instruction, Multiple Data)**: Executes a single instruction on multiple data elements in lockstep, with no divergence.
  
- **SIMT (Single Instruction, Multiple Threads)**: Executes a single instruction across multiple threads, but allows divergence within a group (like a warp). If threads in a warp need to follow different paths, some threads are temporarily disabled (masked) while others complete their execution. The hardware synchronizes the threads when possible.

## 5. Work Division: CPUs vs GPUs

CPUs typically divide work into a few large chunks, with the number of threads being a small multiple of the number of cores. GPUs, however, employ **data parallel programming**, meaning there is a 1-to-1 relation between threads and data elements. 

GPUs achieve their high parallelism by having incredibly fast context switches between warps (each warp has dedicated registers, so there is no need to save and load contexts).

## 6. Limitations of GPUs

While GPUs excel at highly parallel tasks, they struggle with **irregular access patterns** such as those found in graph or sparse matrix operations. In these cases, where SIMT is not possible and branches are frequent, CPUs tend to outperform GPUs.

## 7. GPU Programming vs OpenMP

GPU programming models are similar to OpenMP's "thread-ID partitioning," where each thread knows its responsibilities based on its ID. (However, OpenMP also uses another model called **work-sharing model**, automatically dividing loops among threads, which is different from GPU's explicit thread management.)

## 8. Two-Level Parallelism in GPUs

CPUs typically have a single level of parallelism with thread IDs. In contrast, GPUs have **two levels of parallelism**:

1. A grid of thread blocks, where each block is assigned to an SM.
2. Inside each thread block, there are warps of 32 threads, executing in parallel.

## 9. Synchronization in GPU Threads

Threads within a thread block can synchronize using **shared memory** or a synchronization barrier (`_syncthreads`). However, there is no synchronization between threads from different thread blocks.

Each warp has dedicated hardware (registers) for its context, allowing **1-cycle context switches**. Synchronizing threads across thread blocks would require saving the SM's context in global memory, which would negate the benefits of fast context switching.

## 10. Occupancy vs Register Usage

High register usage in warps can reduce the number of active warps in an SM, limiting its ability to hide memory latency. On the other hand, using very few registers increases memory access, which may lead to excessive memory calls. Balancing register usage and memory calls is key to maximizing GPU performance, ensuring that the SM can effectively hide memory latency and maintain high occupancy.

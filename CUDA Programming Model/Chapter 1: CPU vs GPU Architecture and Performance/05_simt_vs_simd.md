## 4. SIMT vs SIMD: A Key Difference

- **SIMD (Single Instruction, Multiple Data)**: Executes a single instruction on multiple data elements in lockstep, with no divergence.
  
- **SIMT (Single Instruction, Multiple Threads)**: Executes a single instruction across multiple threads, but allows divergence within a group (like a warp). If threads in a warp need to follow different paths, some threads are temporarily disabled (masked) while others complete their execution. The hardware synchronizes the threads when possible.

[Previous: Streaming Multiprocessors (SMs) in GPUs](04_streaming_multiprocessors.md) | [Next: Work Division: CPUs vs GPUs](06_work_division.md)

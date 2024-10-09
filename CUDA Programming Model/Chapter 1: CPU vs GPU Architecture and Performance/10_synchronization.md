## 9. Synchronization in GPU Threads
[Back to Table of Content](../../Readme.md) | [Previous: Two-Level Parallelism in GPUs](09_two_level_parallelism.md) | **[Next: Register Usage](11_registerUsage.md)**

Threads within a thread block can synchronize using **shared memory** or a synchronization barrier (`_syncthreads`). However, there is no synchronization between threads from different thread blocks.

Each warp has dedicated hardware (registers) for its context, allowing **1-cycle context switches**. Synchronizing threads across thread blocks would require saving the SM's context in global memory, which would negate the benefits of fast context switching.

[Back to Table of Content](../../Readme.md) | [Previous: Two-Level Parallelism in GPUs](09_two_level_parallelism.md) | **[Next: Register Usage](11_registerUsage.md)**

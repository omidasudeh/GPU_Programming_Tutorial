## 7. GPU Programming vs OpenMP

GPU programming models are similar to OpenMP's "thread-ID partitioning," where each thread knows its responsibilities based on its ID. However, OpenMP uses a **work-sharing model**, automatically dividing loops among threads, which is different from GPU's explicit thread management.

[Previous: Limitations of GPUs](07_limitations_of_gpus.md) | [Next: Two-Level Parallelism in GPUs](09_two_level_parallelism.md)

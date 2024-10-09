## 10. Occupancy vs Register Usage

High register usage in warps can reduce the number of active warps in an SM, limiting its ability to hide memory latency. On the other hand, using very few registers increases memory access, which may lead to excessive memory calls. Balancing register usage and memory calls is key to maximizing GPU performance, ensuring that the SM can effectively hide memory latency and maintain high occupancy.

[Previous: Synchronization in GPU Threads](09_synchronization.md) | [Back to the beginning](01_introduction.md)

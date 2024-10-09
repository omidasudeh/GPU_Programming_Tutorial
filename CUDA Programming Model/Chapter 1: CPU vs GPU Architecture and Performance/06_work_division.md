## 5. Work Division: CPUs vs GPUs
[Back to Table of Content](../../Readme.md) | [Previous: SIMT vs SIMD](05_simt_vs_simd.md) | **[Next: Limitations of GPUs](07_limitations_of_gpus.md)**

CPUs typically divide work into a few large chunks, with the number of threads being a small multiple of the number of cores. GPUs, however, employ **data parallel programming**, meaning there is a 1-to-1 relation between threads and data elements. 

GPUs achieve their high parallelism by having incredibly fast context switches between warps (each warp has dedicated registers, so there is no need to save and load contexts).


[Back to Table of Content](../../Readme.md) | [Previous: SIMT vs SIMD](05_simt_vs_simd.md) | **[Next: Limitations of GPUs](07_limitations_of_gpus.md)**


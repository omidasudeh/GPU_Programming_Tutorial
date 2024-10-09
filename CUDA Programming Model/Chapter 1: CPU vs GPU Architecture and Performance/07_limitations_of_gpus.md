## 6. Limitations of GPUs
[Back to Table of Content](../../Readme.md) | [Previous: Work Division: CPUs vs GPUs](06_work_division.md) | **[Next: GPU Programming vs OpenMP](08_gpu_vs_openmp.md)**

While GPUs excel at highly parallel tasks, they struggle with **irregular access patterns** such as those found in graph or sparse matrix operations. In these cases, where SIMT is not possible and branches are frequent, CPUs tend to outperform GPUs.

[Back to Table of Content](../../Readme.md) | [Previous: Work Division: CPUs vs GPUs](06_work_division.md) | **[Next: GPU Programming vs OpenMP](08_gpu_vs_openmp.md)**

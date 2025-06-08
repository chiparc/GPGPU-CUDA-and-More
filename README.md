# GPGPU-CUDA-and-More


# === 1. 涵义和范畴

### Why Nvidia GPGPU+CUDA
- 在灵活性+性能+应用生态三个维度，GPGPU+CUDA是行业标准
- AI建立在PyTorch基础之上，GPGPU+CUDA占据了90%市场，其他follow和兼容GPGPU+CUDA

### GPGPU硬件
- host-device, warp+simt是基础架构特征，并长期稳定
- 随着AI的发展，逐步加入Tensor Core, TMA, Async and memory bypass等

### GPGPU软件
一般的C编程考虑对上层应用的开发效率，用CUDA和优化CUDA为了运行效率，所以并行思维和硬件感知是不可避免的
所以，CUDA编程容易上手，但是做好不易；近期大火的DeepSeek核心技术就是面向硬件特性的算法重构和软件优化

### 学习与应用
- 学习GPGPU+CUDA一方面是用好做应用，进一步理解和编程自研架构，对比GPGPU+CUDA
- 建议的方法：浏览，形成体系；按目标推进和即时补充

### 本文下一步
- 对范畴拓展、提炼
- 文献介绍

# === 2. 参考

### 2.1 GPU软件

经典教材及其代码参考：Professional CUDA C Programming
- https://github.com/mapengfei-nwpu/ProfessionalCUDACProgramming/tree/master

CUDA官方参考：基础
- https://docs.nvidia.com/cuda/cuda-c-programming-guide/index.html#id1

CUDA官方参考：最佳实践
- https://docs.nvidia.com/cuda/cuda-c-best-practices-guide/index.html#abstract

对于面向AI的Tensor编程效率和运行性能：Triton和CuTe是简化CUDA编程的努力
- https://zhuanlan.zhihu.com/p/695846421

经典的reduce优化例子
- https://seanwangjs.github.io/2023/11/30/cuda07-parallel-reduce.html


### 2.2 开发环境，最新热点

搜索'开源周'关键字，里面有DeepSeek-V3/R1的优化github地址
- https://zhuanlan.zhihu.com/p/28989216660

### 2.3 Vector CPU设计、向量化编程在业界也有使用、编程和CUDA类似

The ARM Scalable Vector Extension
- https://alastairreid.github.io/papers/sve-ieee-micro-2017.pdf

RISC-V向量指令集定义
- https://github.com/riscvarchive/riscv-v-spec
- https://arxiv.org/pdf/2210.08882

RISC-V编译器向量化Evaluation
- https://neiladit.com/papers/Performance_Left_on_the_Table_An_Evaluation_of_Compiler_Autovectorization_for_RISC-V.pdf

### 2.4 GPU硬件

经典教材：GPU架构
- https://picture.iczhiku.com/resource/eetop/WHKdgQhRWGRojBxB.pdf

针对了解Hopper
- https://arxiv.org/pdf/2402.13499v1#S1

破解硬件细节，Volta
- https://arxiv.org/pdf/1804.06826

### 2.5 GPU性能测试

面上：Altis: Modernizing GPGPU Benchmarks
- https://arxiv.org/pdf/1906.10347

### 2.6 CPU和GPU单核测试

ABC: Agile Benchmark for Cores
- https://github.com/chiparc/benchmark/tree/main

